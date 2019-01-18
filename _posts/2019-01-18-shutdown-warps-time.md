---
layout: post-with-image
title: "How the Government Shutdown Warps Time Itself!"
excerpt: "The curious causal chain connecting the federal government shutdown to computer timekeeping and leap seconds."
image:
  filename: "trump_groundhog_day2.jpg"
  alt:      "Trump driving Punxsutawney Phil into madness."
  caption:  "Trump driving Punxsutawney Phil into madness."
date: 2019-01-18
author: "Scott"
---


"The government shutdown is warping time itself!" Now there's a clickbait headline.
Fortunately it's not quite true, although there's a curious causal chain
linking the proper functioning of the US federal government on one end and the
ability for computers to accurately keep time on the other. Even better, this
chain of dependency concerns ["the centuries-long quest to measure one second."](https://www.popularmechanics.com/technology/a25785/quest-measure-second-nist/)

# Measures of time

Many people might know about Coordinated Universal Time (UTC), the preeminent
standard for civil timekeeping in virtually all of the world since the early 1970s.
What's less commonly known is that this is one of several competing "universal times" (UT)
used for measuring time in relation to the rotation of the Earth; after all, one
rotation of the earth on its axis is basically the length of one day, which is 24 hours,
which is 86,400 seconds, etc. But since the rotation of the Earth is irregular -- it's
gradually slowing down as time marches forward -- the definition of time based on that
rotation, i.e., of _seconds_, starts to become less of a fixed standard of measure and
more of a changing variable.

To correct for that changing variable, modern science relies on atomic time, which today is based on the [behavior of cesium atoms](https://www.popularmechanics.com/technology/a25785/quest-measure-second-nist/). Like there are multiple methods of measuring the age of the Earth -- astronomical and geological -- there are multiple ways of measuring time -- astronomical and atomic. In particular, as yet another example of institutional definitions of physical phenomenon, International Atomic Time (TAI) is [defined as](http://www.stjarnhimlen.se/comp/time.html) "the weighted average of the time kept by about 200 atomic clocks in over 50 national laboratories worldwide." Because TAI is not based on the Earth's rotation, it's not ever-so-slowly changing. It's the measure of time against which UTC's watch is occasionally correct. That correction is called a _leap second_: a 61st second that is sometimes added to particular minutes in UTC, like the very last minute of December 31, 2016. As of January 2019 there have been 27 such leap seconds inserted.

As an aside, this method of _ex-post-facto_ correction to UTC by adding leap seconds is analogous to pre-modern methods of _ex-post-facto_ correction to the calendar by adding leap days. Before Julius Caesar ushered in the Julian calendar, leap days were sporadically added to the calendar, sometimes for highly political reasons, thereby stretching out or cutting short certain political reigns. With the Julian calendar came a _predictable_ method of correcting the number of days in a year, a method that was slightly modified to be even more accurate in the 1500s with the Gregorian calendar.

# Inserting leap seconds

Now back to those leap seconds. If UTC is intended to be a highly regular, fixed standard, its need to be occasionally corrected begs the question, _who sets the watch of the watchman?_ TAI is the atomic time that acts as a frame of reference, but some entity must actually judge when UTC needs correcting. Moreover, that entity needs to be authoritative enough that it's followed by all observers of UTC -- which is essentially the entire world.

The International Earth Rotation and Reference Systems Service (IERS) based at the Paris Observatory is the organization that [authoritatively adjusts UTC](https://www.iers.org/SharedDocs/Publikationen/EN/IERS/Documents/IERS_Leap_Seconds.pdf?__blob=publicationFile&v=1). Every six months, like [Punxsutawney Phil](https://en.wikipedia.org/wiki/Punxsutawney_Phil), scientists at IERS emerge from their labs, look at their shadow, i.e., recent astronomical measurements of Earth's Rotation Angle, and determine whether a second will be added in the following six months, only ever at the end of June 30th and December 31st each year. Six more months of winter, six more months of 86,400 seconds each day.

Whereas Punxsutawney Phil announces his ruling in Punxsutawney, Pennsylvania and then news networks rebroadcast it, the IERS disseminates announces their leap seconds ruling in a self-published [bulletin](https://datacenter.iers.org/data/latestVersion/16_BULLETIN_C16.txt) and then national laboratories around the world publish the updated leap seconds file. One such republisher is the US National Institute of Standards and Technology (NIST), which maintains a copy of the leap seconds file [on an FTP server](http://support.ntp.org/bin/view/Support/ConfiguringNTP#Section_6.14.) -- at least when NIST, an agency of the US federal government, is staffed and functional. That's not currently the case.

# Computing with leap seconds

Leap seconds are the result of a Paris-based lab correcting UTC time to more accurately match atomic time. Pedantic scientists want to observe them of course, and they can do so by following the IERS bulletin. But what's an even more pedantic observer than scientists? One that needs to be told how to access the IERS bulletin? Computers!

Computers generally keep UTC time as part of low-level mechanisms based on the cyclical behavior or their CPUs. They count seconds in a deterministic way. But leap seconds are anything but deterministic; they're determined by human authorities, _deus ex humana_. In order for computers to know that counting N seconds lands not on Jan 1, 2017 at midnight but actually the 61st second of the last minute of Dec 31, 2016, it needs to know the IERS decisions about leap seconds.

Computers learn about leap seconds in two ways. The first way, the one used by your smartphone and just about any device connected to the internet, relies on a service called the Network Time Protocol (NTP). This protocol allows a device to ask a trusted authority over the network what the current UTC time is. (Note that time zones aren't involved; it's just UTC time.) Major NTP providers, like Google, build elaborate mechanisms for handling leap seconds, like [smearing a leap second](https://developers.google.com/time/smear?hl=en) across a period of 24 hours so that each second in that period lasts 11.6 microseconds longer than an atomic second.

The second way computers learn about leap seconds, the way a computer without a steady internet connection learns about it, is to periodically download and process the leap seconds file hosted by some institution. A primary institution that computers and maintainers trust is the [IANA time zone database](https://www.iana.org/time-zones) (tzdb or tzdata for short), an edited repository of the world's geographical and political decisions about timekeeping, time zones, and daylight saving throughout modern history. (There'll be plenty more about tzdata on this blog.) In fact, sources from the Internet Engineering Task Force (IETF), a trusted standards body which [hosts a leap seconds file](https://www.ietf.org/timezones/data/leap-seconds.list), to programming language platforms like Java, each release of which [comes packaged](https://www.oracle.com/technetwork/java/javase/tzdata-versions-138805.html) with a (manually updatable) release of tzdata in order to make sense of local times around the world, copy or retrieve the leap seconds file that comes with each release of tzdata.

Unfortunately, tzdata's republication of leap seconds hits a snag when the US federal government isn't operating.

# Government shutdown and copyright

The editors and maintainers of tzdata were [fully aware](https://mm.icann.org/pipermail/tz/2019-January/027379.html) when the IERS announced the [most recent leap seconds bulletin](https://datacenter.iers.org/data/latestVersion/16_BULLETIN_C16.txt) on January 7, 2019. They were also fully aware of the [IERS's own updated leap seconds file](https://hpiers.obspm.fr/iers/bul/bulc/ntp/leap-seconds.list) that was subsequently updated. But because of uncertainties about international copyright laws and what counts as public domain, they could not simply copy that file into tzdata. There have been past efforts to rectify that legal situation by requesting that the IERS add clearer language about ownership to the file, but [the last time this came up](https://mm.icann.org/pipermail/tz/2019-January/027379.html) a couple years ago, the IERS seems to have [bungled](https://mm.icann.org/pipermail/tz/2019-January/027384.html) the precise [legal language](https://mm.icann.org/pipermail/tz/2017-April/024990.html) necessary in the right places of the files.

How do the tzdata editors normally republish the leap seconds file then? They copy it from the NIST republication, which is bound to US laws about public domain ownership of federal agencies' work. NIST avoids legal trouble maintaining their file because they're not adhering to the same [software license that binds tzdata](https://mm.icann.org/pipermail/tz/2019-January/027385.html).

When NIST isn't operating -- say, because the federal government shuts down non-essential services -- they're not updating their leap seconds file. And when they're not updating their leap seconds file, the up-to-date knowledge about leap seconds isn't available to tzdata for strictly legal reasons. And when tzdata doesn't have the up-to-date knowledge about leap seconds, many software systems that rely on it won't have an accurate understanding of UTC time.

All those consequences form a chain of dependency from the proper functioning of the federal government all the way to the correct timekeeping of many computers.

## * * *

Time is not in such a dire state at the moment. That's because on January 7, 2019, scientists in Paris decided there'd be no leap second in summer 2019, and therefore computers can keep on counting seconds without going out of step with official UTC.

But if there's another federal shutdown, one that lasts more than six months, one that happens while the IERS decides there will be a leap second, time itself would truly be warped, at least according to many computers.
