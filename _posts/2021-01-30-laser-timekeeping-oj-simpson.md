---
layout: post-with-image
title: "Lasers, Timekeeping, and the OJ Simpson Trial"
excerpt: "New laser technology might enable more accurate timekeeping and revised definitions of measurements of time. Somehow, there's a connection to an infamous murder trial."
image:
  filename: "cbc-time-signal.jpg"
  alt:      "Reproduction of advertisement for Canadian Broadcasting Company's National Research Council Time Signal, Canada's 'longest running radio program.'"
  caption:  "Reproduction of advertisement for Canadian Broadcasting Company's National Research Council Time Signal, Canada's 'longest running radio program.'"
date: 2021-01-30
---


The [IANA time zone database](https://www.iana.org/time-zones) ("tzdata") [mailing list](https://mm.icann.org/mailman/listinfo/tz) has an active discussion right now on [an upcoming international meeting](https://mm.icann.org/pipermail/tz/2021-January/029692.html) about _possibly changing the international definition about what time means_ on account of new laser technology. I think I speak for all of us when I say _WHAAAAA???_

> The last time the definition of the SI second was changed was in 1967 when Caesium atom hyperfine frequency transition was chosen as the reference value.
> 
> Since then first the primary thermal beam caesium clocks and then caesium fountains have been providing the SI second realization values to steer the International Atomic Timescale. The current fountain uncertainties are at the low 1E-16 level.
> 
> The frequency metrology research in recent years has surpassed the microwave clocks, and optical frequency standards based on trapped ions and atoms now provide frequency measurements with evaluated uncertainties at the level 1E-18.
> 
> The frequency comparisons have also been advancing both through improved techniques in Global Navigation Satellite Systems signal analysis and the Two Way satellite Time and Frequency transfer as well as with fibre based frequency links and portable optical clocks. [...]
> 
> These factors now provide a solid foundation to prepare for the redefinition of SI second based on the optical frequency standard.

That escalation of timekeeping precision is interesting itself, but even more interesting, in my opinion, is the amusing message from tzdata editor-in-chief (and UCLA CS professor) [Paul Eggert](https://samueli.ucla.edu/people/paul-eggert/), reproduced below. On the subject of broadcast time signals --- a key aspect of timekeeping, whether it's [radio](https://en.wikipedia.org/wiki/Time_signal#Radio_time_sources) in the 19th and 20th centuries or [cesium](https://www.nist.gov/pml/time-and-frequency-division/time-realization/primary-standard-nist-f1) and lasers in the 21st --- he recalls an example of how radio time signal broadcasts came up in _the 1995 OJ Simpson trial_.

Here's how Eggert connects these two entirely disparate subjects:

> This topic came up during the famous trial of OJ Simpson in the 1990s, when they were trying to establish a timeline of events. Here's a section from the 1995-07-11 trial transcript:
>
> MR. DARDEN: Miss Harman, the times that you've given us today, those--the accuracy of those times depend on the accuracy of someone else's kitchen clock; is that correct?
>
> MS. HARMAN: And--
>
> MR. SHAPIRO: Objection.
>
> THE COURT: Overruled.
>
> MS. HARMAN: And desk clock. Yes, it would.
>
> MR. DARDEN: Okay. And as well as the accuracy of the digital clock in your vehicle; is that correct?
>
> MS. HARMAN: Yes, it would.
>
> MR. DARDEN: And so if those clocks are one or two or more or less minutes off, then your time would be off, wouldn't it?
>
> MS. HARMAN: It would, except I usually set the clock to KFWB. So I feel confident that the clock in my car was accurate.
>
> Afterwards, I remember reports that KFWB's time signal was more accurate than that of KNX, their main news rival, and that KFWB's marketing tried to make hay of this.  In the long run it was all for naught, though: KFWB's corporate owner bought the much more powerful KNX and then eventually sold KFWB, which is now airs classic regional Mexican music. And as far as I know, KNX's audio time signal is no more accurate now than it was in the 1990s.



Eggert's appreciation for random cultural and historical notes can be found all over tzdata. That's part of what makes it so interesting to peruse and to keep up with! And I'm far from the first to proselytize tzdata as such; [here's a 2009 blog post](https://blog.jonudell.net/2009/10/23/a-literary-appreciation-of-the-olsonzoneinfotz-database/) from software engineer [Jon Udell](https://jonudell.net) articulating "a literary appreciation" of tzdata. Go take a stroll through [the data files](https://github.com/eggert/tz/blob/master/africa) or [the mailing list](https://www.google.com/search?q=site%3Amm.icann.org%2Fpipermail%2Ftz%2F+morocco&oq=site%3Amm.icann.org%2Fpipermail%2Ftz%2F+morocco) yourself.
