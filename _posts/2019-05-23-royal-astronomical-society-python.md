---
layout: post-with-image
title: "What the Royal Astronomical Society in 1884 Tells Us About Python Today"
excerpt: "The plainly wrong behavior of a ubiquitous Python library echoes a British astronomical report from 1884."
image:
  filename: "astronomy-jupyter-pytz.png"
  alt:      "A mash-up of the Monthly Notices of the Royal Astronomical Society report and a Jupyter notebook."
  caption:  "A mash-up of the Monthly Notices of the Royal Astronomical Society report and a Jupyter notebook."
date: 2019-05-23
---


[pytz](http://pytz.sourceforge.net/) is a ubiquitous library in the Python
ecosystem for supporting localized datetimes in Python. Without using pytz or
something like it, there's no way to program around localized datetimes whose
offset from GMT _varies over time_. More concretely, there's no way to write
daylight saving time-aware programs in Python without a third-party library 
like pytz. (Spoiler alert: you shouldn't use pytz at all though; keep reading.)

To support this functionality, pytz constructs `tzinfo` objects (Python's
weak abstraction for time zones) that load the definitions from the
standard IANA time zone database, [tzdb](https://www.iana.org/time-zones).
These objects can then be used with the standard library's `datetime` object
to create localized datetimes. Here's an example...
```python
from datetime import datetime
import pytz

# the localized datetime for 2019 May 21 12:30pm, NYC/Eastern Time
print(datetime(2019, 5, 21, 12, 30,
               tzinfo=pytz.timezone('America/New_York')))
```
... except that it's actually a buggy program! The printed datetime is
```
2019-05-21 12:30:00-04:56
```
That `-04:56` is the GMT offset of the localized time; it says that the
constructed `datetime` object represents 12:30pm on 2019 May 21, which is
correct, but that this time is 4 hours and 56 minutes behind GMT, which is
incorrect.

Naturally, we'd expect that offset to be `-4:00`, i.e., Eastern Daylight Time, which is
the offset governing the `'America/New_York'` zone at `2019-05-21 12:30`.
Failing that, we might expect it to be `-5:00`, i.e., Eastern Standard (Winter)
Time. But `-04:56`? _What the heck is that??_


Why, that's the longitudinally derived local time of New York City Hall as
reported to the Royal Astronomical Society in 1884![^ref]

{% capture astrotext %}
Excerpt from a Royal Astronomical Society report discussing a then-recent
conference on standardizing time and longitude. See footnote.
{% endcapture %}
{% include image.html filename="astronomy-nyc-time.png" description=astrotext %}

The first sentence in the report excerpt above gives the context: the
establishment of standard times across the US and Canada for the railway
companies to use (though not yet enshrined in US federal policy, that would
be in 1918). The newly christened Eastern Time was five hours west of the
Greenwich Mean Time that would be agreed upon as the international standard
at a conference in DC later in 1884. The local time at New York City Hall was
reported to be 3m 58.4s fast (i.e., _east_) of Eastern Time, and therefore -5h
for Eastern Time plus 3m 58.4s to correct for NYC yields a GMT offset for NYC
of -4h 56m.

You can see the assignment of this offset to the `America/New_York` time zone
in the IANA tzdb [here](https://github.com/eggert/tz/blob/2019a/northamerica#L321-L335):

```
# From Paul Eggert (2014-09-06):
# Monthly Notices of the Royal Astronomical Society 44, 4 (1884-02-08), 208
# says that New York City Hall time was 3 minutes 58.4 seconds fast of
# Eastern time (i.e., -4:56:01.6) just before the 1883 switch.  Round to the
# nearest second.

<...>

# Zone	NAME		GMTOFF	RULES	FORMAT	[UNTIL]
Zone America/New_York	-4:56:02 -	LMT	1883 Nov 18 12:03:58
			-5:00	US	E%sT	1920
      <...>
```

The last line above says that the offset for this zone is -4h 56m 02s, called
the "local mean time" (LMT), up until 1883 Nov 18 12:03:58, which is the NYC
local time of when GMT was standardized by US railways (though not yet
officially by the federal government). Note that the local time of the change
is 3m 58s after noon.[^change]

Back to that buggy pytz code.

It's a fairly common mistake to make. In fact, here's a snapshot of the
[69 results](https://www.google.com/search?q=%22pytz%22+%22datetime%22++%224:56%22+site:stackoverflow.com)
Google returns for `"pytz" "datetime" "4:56"` on Stack Overflow:

{% include image.html filename="pytz-456-google-results.png" %}

The bug is even common enough to warrant [mention](http://pytz.sourceforge.net/#localized-times-and-date-arithmetic)
on the pytz website as
a "gotcha" to avoid. The source of the bug is that the pytz `tzinfo` object passed to the `datetime` constructor is using _the very first_ GMT offset defined for the zone in tzdb, which tends to be some longitudinally-derived LMT from before standardized timekeeping.[^pytzcode]

What should pytz's implementation do instead? The same thing it does when you construct a localized `datetime` in pytz's preferred, albeit non-standard, way: use the local datetime as an index into the tzdb zone definition. For example, this program will do what you expect:
```python
from datetime import datetime
import pytz

# the *correct* localized datetime for 2019 May 21 12:30pm, NYC/Eastern Time
print(pytz.timezone('America/New_York').localize(
        datetime(2019, 5, 21, 12, 30)))
```

Now the local datetime indexes into the `America/New_York` definition by picking out the correct GMT offset, -4h:[^dst]
```
2019-05-21 12:30:00-04:00
```

It's unclear why pytz's developers and maintainers have left this buggy behavior
in pytz for, apparently, almost a decade. But one thing is certain:
_you [should not use pytz](https://blog.ganssle.io/articles/2018/03/pytz-fastest-footgun.html)
for localized datetimes in Python today!_ Instead,
check out the much more reasonable, drop-in behavior of time zone objects in the
[`dateutil`](https://dateutil.readthedocs.io/en/stable/) library. It's also more
actively maintained, now by Paul Ganssle, who has been [advising the
Python community](http://pyfound.blogspot.com/2019/05/paul-ganssle-time-zones-in-standard.html)
on how to integrate time zones into the Python standard library.

* * *

Looking back at the `America/New_York` definition from before, we see helpful commentary from the tzdb editor-in-chief. That's how I derived the historical context above. I'm not the first
person to [appreciate](https://blog.jonudell.net/2009/10/23/a-literary-appreciation-of-the-olsonzoneinfotz-database/)
such commentary in the tzdb.

Along those lines, there's another curious provenance to the LMT that
tzdb assigns to a time zone for 19th century dates. If we replace
`America/New_York` in the Python example with `Europe/London`, we see another
peculiar GMT offset:
```
2019-05-21 12:30:00-00:01
```
Given that Greenwich Mean Time is defined as the local time on the longitude
that passes through the Royal Observatory in Greenwich, a borough of London,
we would expect the LMT of the `Europe/London` time zone to be pretty close,
if not simply approximated as the exact same time. Where does this roughly
-1m offset come from then?

Looking at the commentary in the tzdb, one sees
[the following note](https://github.com/eggert/tz/blob/2019a/europe#L106-L125)
from contributor Peter Ilieve:
> On 17 Jan 1994 the Independent, a UK quality newspaper, had a piece about
> historical vistas along the Thames in west London. There was a photo
> and a sketch map showing some of the sightlines involved. One paragraph
> of the text described [an old stone obelisk marking a forgotten terrestrial
> meridian used as the basis for celestial calculations of local time. ...]
>
> I have a one inch to one mile map of London and my estimate of the stone's
> position is 51° 28' 30" N, 0° 18' 45" W. The longitude should
> be within about ±2". [...]
>
> [This yields [GMTOFF = -0:01:15](https://github.com/eggert/tz/blob/2019a/europe#L504) for London LMT in the 18th century.]
{:.nogray}

Your program could evaluate to a number whose provenance is traced back to
a hobbyist's estimation of the precise location of "an old stone obelisk"
based on an old newspaper photograph and a handy map. I believe that's what
they call in the formal semantics of memory models literature an
[_out-of-thin-air value_](https://www.cl.cam.ac.uk/~pes20/cpp/notes42.html).


[^ref]:
    [Notes on some Points connected with the Progress of Astronomy during the
    past Year](https://academic.oup.com/mnras/article/44/4/177/1030726),
    _Monthly Notices of the Royal Astronomical Society_, Volume 44,
    Issue 4, 8 February 1884, p. 208.

[^change]:
    The switch to the new standard time zones happened throughout the
    US at noon local standard time. Then the switch occurred in New York
    at noon Eastern Standard Time, which, due to the slight time difference,
    worked out to be 12:03:58 local time. Or at least that's the story we
    tell (to computers, via tzdb) today.
    
[^dst]:
    Technically, it picks put the Eastern Standard Time offset of -5h, but
    along with [that offset](https://github.com/eggert/tz/blob/2019a/northamerica#L339)
    comes the `US` daylight saving time rule.
    [That rule](https://github.com/eggert/tz/blob/2019a/northamerica#L162)
    then says that the datetime falls within a DST period and so 1h should
    be added to the offset, resulting in -4h.
    
[^pytzcode]:
    Pytz's `tzinfo` objects are intialized with the very first GMT offset of
    the zone [here](https://github.com/stub42/pytz/blob/release_2019.1/src/pytz/tzinfo.py#L186-L187).
    Then in its [implementation](https://github.com/stub42/pytz/blob/release_2019.1/src/pytz/tzinfo.py#L425)
    of the `utcoffset` method, called by the `print` method, it simply uses
    that same offset rather than indexing into the stored data with the datetime.
