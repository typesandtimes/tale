---
layout: post-with-image
title: "Daylight Saving in the Time of Corona"
excerpt: "Daylight saving time is good for public health—except during a pandemic."
image:
  filename: "dst-coronavirus.png"
  alt:      "This clock is too happy given what's happening."
date: 2020-03-24
---

It's the early days of the global coronavirus pandemic. What strange times! And in the news we have a reminder that _time_ is oriented around _society_... until people remember what a pain _computers_ can be about it.
 
On Sunday, March 22nd, Israel's Interior Minister requested that daylight saving time in Israel, which was to begin the subsequent Friday, actually be [_delayed_ due to the coronavirus](https://mail.google.com/mail/?tab=mm1).
 
> Israel could delay switching to daylight saving time to discourage public traffic in the streets in the evening hours and promote social distancing, as part of the fight against the coronavirus, Interior Minister Aryeh Deri said Sunday. [...]
>
> However, authorities fear that having the sun set an hour later would increase the number of people venturing outside their homes at a time when Israelis are being encouraged to stay indoors as much as possible.
 
Traditionally, the argument for DST is that it promotes public health and commerce by allowing people more time in the evenings, after the work day ends, to leisurely go about town. But now the coronavirus pandemic presents the exact opposite public health outcome of DST.
 
The emergency measure to delay DST seemed to have the government's approval. Time would bend --- or in this case, not bend --- according to the whims of society and its designated authorities. But one authority outranks the elected government on such matters: computers!
 
Israel's National Security Council [determined this morning](https://www.jpost.com/HEALTH-SCIENCE/Coronavirus-Netanyahu-considers-upping-restrictions-as-patients-hit-1238-621986) that "the implementation of the summer clock cannot be postponed and it will begin on Friday." Now what could be so important that a public health concern is overruled, and by the National Security Council no less?
 
> It was determined based on the advice of the Israel Digital Authority that the date of transition between the winter and summer clocks is structurally defined in the operating systems of servers, computers, communications equipment and cellular phones. The authority said that to change such a system would take longer than the time available.
 
In other words, because the prospective DST delay would have to percolate through computer timekeeping, there's simply not enough lead time to make the change without disruption to computers, phones, and all sorts of other devices that help us structure and monitor our days.
 
Virtually all such devices base their civil timekeeping practices --- their [notions](https://data.iana.org/time-zones/tz-link.html) of time zones and DST rules across the world --- on the [IANA time zone database (tzdb)](https://www.iana.org/time-zones). The tzdb editor-in-chief, a CS professor at UCLA, [Paul Eggert](https://samueli.ucla.edu/people/paul-eggert/), issues a handful of releases of the database every year. Those tzdb releases then percolate through the operating systems of computers and phones; in the case of phones, that sometimes requires service updates issued by phone service providers. (There's a reason 99% of people don't think about this: it's a responsibility that falls entirely on some intermediary.) For that percolation to reach enough computers and personal devices in time for a clock change, the tzdb [recommends](https://data.iana.org/time-zones/tz-link.html#changes) such changes take place at least a year before they're announced.
 
Effectively, there's simply not enough time to encode the prospective DST delay for the [`Asia/Jerusalem`](https://github.com/eggert/tz/blob/b7adcf175ccead5827da62b2e37ee8e916778140/asia#L1832) time zone, release it, and get it into the operating systems of enough computers and personal devices by Friday. Thinking in terms of the clock on one's own phone, that might not seem like a big deal; but in terms of all the clocks in computers used for commercial, administrative, or even military activity, that starts to sound like a [problem](https://codeofmatt.com/on-the-timing-of-time-zone-changes/) that a National Security Council might worry about.
 
The coronavirus presents a threat to public health worldwide, requiring governments to take extreme measures. But we still can't rush the computers.
