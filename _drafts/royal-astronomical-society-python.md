---
layout: post-with-image
title: "What the 1884 Royal Astronomical Society Tells Us About Python Today"
excerpt: "The plainly wrong behavior of a ubiquitous Python library echoes a British astronomical report from 1884."
image:
  filename: "astronomy-jupyter-pytz.png"
  alt:      "A mash-up of the Monthly Notices of the Royal Astronomical Society report and a Jupyter notebook."
  caption:  "A mash-up of the Monthly Notices of the Royal Astronomical Society report containing the history of New York City local mean time along with a Jupyter notebook revealing the buggy Python behavior."
date: 2019-05-22
author: "Scott"
---


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

Naturally, we’d expect that offset to be `-4:00`, i.e., Eastern Daylight Time, which is
the offset governing the `'America/New_York'` zone at `2019-05-21 12:30`.
Failing that, we might expect it to be -5:00, i.e., Eastern Standard (Winter)
Time. But `-04:56`? _What the heck is that??_

