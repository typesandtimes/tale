—
layout: post-with-image
title: "What the 1884 Royal Astronomical Society Tells Us About Python Today"
excerpt: "The plainly wrong behavior of a ubiquitous Python library echoes a British astronomical report from 1884."
image:
  filename: "astronomy-jupyter-pytz.png"
  alt:      "A mash-up of the Monthly Notices of the Royal Astronomical Society report and a Jupyter notebook."
  caption:  "A mash-up of the Monthly Notices of the Royal Astronomical Society report containing the history of New York City local mean time along with a Jupyter notebook revealing the buggy Python behavior."
date: 2019-05-23
author: "Scott"
draft: true
—


[pytz](http://pytz.sourceforge.net/) is a ubiquitous library in the Python
ecosystem for supporting localized datetimes in Python. Without using pytz or
something like it, there's no way to program around localized datetimes whose
offset from UTC _varies over time_. More concretely, there's no way to write
daylight saving time-aware programs in Python without a third-party library 
like pytz.

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
That `-04:56` is the UTC offset of the localized time; it says that the
constructed `datetime` object represents 12:30pm on 2019 May 21, which is
correct, but that this time is 4 hours and 56 minutes behind UTC, which is
incorrect.

Naturally, we'd expect that offset to be `-4:00`, i.e., Eastern Daylight Time, which is
the offset governing the `'America/New_York'` zone at `2019-05-21 12:30`.
Failing that, we might expect it to be `-5:00`, i.e., Eastern Standard (Winter)
Time. But `-04:56`? _What the heck is that??_


Why, that's the longitudinally derived local time of New York City Hall as reported to the Royal Astronomical Society in 1884![^ref]

{% capture astrotext %}
Excerpt from a Royal Astronomical Society report discussing a then-recent conference on standardizing time and longitude. See footnote.
{% endcapture %}
{% include image.html filename="royal-astronomy-nyc-time.png" description=astrotext %}

The first sentence in the report excerpt above gives the context: the establishment of standard times across the US and Canada for the railway companies to use (though not yet enshrined in US federal policy, that would be in 1918). The newly christened Eastern Time was five hours west of the Greenwich Mean Time that would be agreed upon as the international standard at a conference in DC later in 1884. The local time at New York City Hall was reported to be 3m 58.4s fast (i.e., _east_) of Eastern Time, and therefore -5h for Eastern Time plus 3m 58.4s to correct for NYC yields a UTC offset for NYC of -4h 56m.

You can see the assignment of this offset to the `America/New_York` time zone in the IANA tzdb [here](https://github.com/eggert/tz/blob/2019a/northamerica#L321-L335):

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
```

The last line above says that the offset for this zone is -4h 56m 02s, called the "local mean time" (LMT), up until 1883 Nov 18 12:03:58, which is the NYC local time of when GMT was standardized by US railways (though not yet officially by the federal government). Note that the local time of the change is 3m 58s after noon.[^change]
 
That helpful comment from the tzdb editor-in-chief above the time zone definition is how I derived the historical context above. 

[^ref]: Citation

[^change]: The switch to the new standard time zones happened throughout the US at noon local standard time. Then the switch occurred in New York at noon Eastern Standard Time, which, due to the slight time difference, worked out to be 12:03:58 local time. Or at least that's the story we tell (to computers) today.