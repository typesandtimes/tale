---
layout: post-with-image
title: "The Social Trumps the Mechanical"
excerpt: "Like the problems with time zones and daylight saving, \"Japan's Y2K bug\" is a problem of society breaking software, not software breaking itself."
image:
  filename: "japanese-calendar.jpg"
  alt:      "The Japanese imperial calendar"
  caption:  "The Japanese imperial calendar uses its own eras and years of eras."
date: 2018-07-26
author: "Scott"
---

In the Japanese imperial calendar there are eras defined by each emperor's reign.
A date in this calendar has the same month and day as our Gregorian calendar but the year
is numbered according to the era. So today is July 26th, Heisei 30: the 30th year of the
Heisei era. (It's the 2019th year or the Common Era in the Gregorian calendar.)

The current era began in 1989, so there have been 30 years worth of software written for
the Japanese calendar that have not tested what happens when there's an era transition.
And now there's about to be such a transition since the emperor will soon abdicate.

To make matters worse, software can't necessarily be patched ahead of time because the
name of the era isn't known until the new emperor declares it! Even worse, the Japanese
character for the era needs to make it into the Unicode standard of symbols in order
for software and OS manufacturers - your friggin keyboard and display - to implement
the proper entry and rendering of that symbol. Again, they can't do this until the
era is announced!

All this is reported in this new article in The Guardian,
["Big tech warns of 'Japan's millennium bug' ahead of Akihito's abdication."](https://amp.theguardian.com/technology/2018/jul/25/big-tech-warns-japan-millennium-bug-y2k-emperor-akihito-abdication)
The article calls this Japan's Y2K problem, but that problem was purely a computing one:
years were stored in software in a limited way. This problem is something else entirely.
Like the problems with time zones and daylight saving, this is a problem of society
breaking software, not software breaking itself.

No matter how much computer scientists try to enforce a rigid and systematic discipline
for codifying global social practices, for the sake of computing, finance, business, and
even government, there's always some aspect of the social world that screws it up. That's
a theme that this blog will focus on.
