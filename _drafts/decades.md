---
layout: post-with-image
title: "How to Periodize History: 2020 and the Decade Dilemma"
excerpt: "Does 2020 begin a new decade? To answer this question we must consult the pope, the Kaiser, the census, a hockey player, and ISO 8601."
image:
  filename:  "decade/new-century-cartoon-boomer.jpg"
  alt:       "Illustration on the front page of the 1 January 1901 issue of The Washington Times."

date: 2020-01-01
author: "Scott Kilpatrick"
---

A new year in the Common Era has arrived, surely to inundate us all with visual acuity puns. But has _a new decade_ also arrived?

The question has percolated through the loud void of social media, reverberating across [digital content mills and respectable media outlets alike](https://duckduckgo.com/?q=is+2020+a+new+decade&t=h_&ia=news). We all find ourselves burning with new intensity, searching for any authoritative voice to make sense of this quandary. _[The New York Times](https://www.nytimes.com/2019/11/28/us/what-is-decade.html), [Farmer's Almanac](https://www.farmersalmanac.com/new-decade-2020-or-2021-100900), [Timeanddate.com](https://www.timeanddate.com/calendar/decade.html), please somebody tell us!_

{% include image.html filename="decade/when-new-decade-begins.png" description="Altered headline of the December 10, 1899 Boston Herald." %}




# The Two Camps of Counting

When asked whether 2020 marks a new decade, people fall into two camps, which I'll call the _Cardinals_ and the _Ordinals_.

* The Cardinals answer _yes, for decades are identified by their digit representations_. The previous decade, the 2010s, included the years 2010 through 2019, while the new decade, the 2020s, includes the years 2020 through 2029.

* The Ordinals, on the other hand, answer _no, for decades are identified by ordinal numbers counted in sequence from the beginning_. The current decade, the 202nd (or the 2nd of the 21st century), includes the years 2011 through 2020, while the next decade, the 203rd, will include the years 2021 through 2030.

These two camps are both so rational and natural that a person in one camp might deny the very existence of the other. Not since 2015 --- is that still this decade? --- and "[the dress](https://en.wikipedia.org/wiki/The_dress)" have two camps formed so resolutely online. Are they not both completely legitimate ways to count off the decades? If only some authoritative source could lend its weight to either camp.

In an earlier time, the Pope himself might have served as just such an authority. After all, our calendar isn't called "[Gregorian](https://en.wikipedia.org/wiki/Gregorian_calendar)" for nothing; [Pope Gregory XIII]((https://en.wikipedia.org/wiki/Pope_Gregory_XIII)) commissioned it in the 16th century. Recent articles on the subject have consulted [meteorological associations](https://www.forbes.com/sites/marshallshepherd/2020/01/01/is-2020-the-start-of-a-new-decadea-human-technical-and-climate-perspective/#18ed2fd3ee2f), [philosophy professors](https://www.usatoday.com/story/news/nation/2019/12/10/2020-start-new-decade-some-say-thats-not-until-2021/4366467002/), and [the United States Naval Observatory](https://www.nytimes.com/2019/11/28/us/what-is-decade.html).

I will put forward two potential authoritative sources on whether decades should be counted according to Cardinals or to Ordinals: ISO 8601 and decennial census legislation. And unfortunately, they lead us into different camps.

# In One Corner, the Geeks

[ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) is the specification of (representations of) dates, times, and other calendar entities for use in computing. The International Organization for Standardization defines new versions every so often, the most recent one in 2019. It's the closest thing we've got to a gold standard for dates and times in software. _What's the right way to represent dates? Local times of day? Local times of day for some time zone? Time scales? Leap seconds?_

ISO 8601 even defines a new standard calendar adapted from the Gregorian calendar.[^iso8601calendar] Just as Common Era was a secular substitution for Anno Domini, the ISO 8601 calendar supplants the Gregorian calendar. No more pesky Year 1 C.E. preceded by Year 1 B.C.E.; ISO 8601 has _Year Zero_,[^yearzero] and negative years. That essentially makes the Ordinal thinking moot, as the first ISO 8601 decade includes the years 0 through 9, not 1 through 10.

Indeed, decades, as defined in ISO 8601, are the years `XXX0` through `XXX9`.[^iso8601decade] For example, using `J` to denote decades, "the 2020s" are represented as `202J`; the "zero decade" is represented as `0J`; and "the negative zero decade," meaning years -9 through 0, is represented as `-0J`. Somewhat strangely, the latter two decades both include year 0. As a consequence, ISO 8601 _really_ rejects the Ordinals since decades no longer describe an ordered, mutually exclusive sequence of spans of ten years.

ISO 8601 is firmly in the camp of the Cardinals.



# In the Other Corner, the Wonks

Not everyone finds ISO 8601 to be all that authoritative. But what about the European Union? Okay, maybe not the English, but what about their own government as well? And even the Americas? Although governments of nation states don't generally have reason to weigh in on the exact definitions of time, they do tend to institutionalize the decade in particular---as the period in which the government conducts a census.

The practice of conducting a population census by state authorities goes back to ancient times; the decennial period --- once a decade --- became convention more recently. For those states that conduct them decennially, surely they must spell out the precise formal interpretation of decades, right?

Recent legislation in the European Union does exactly that. In its standardization of population and housing census methodology for member states, the EU specifies that member nations run a census "every decade" on a "reference date" of their choosing. "The first reference year shall be 2011. [...] Reference years shall fall during the beginning of every decade." In other words, the `1` years begin the decades and therefore the EU implicitly takes up the Ordinal position.

For the United States in particular, it's even [in our Constitution](https://www.census.gov/history/pdf/Article_1_Section_2.pdf) to apportion Congressional representatives according to state populations counted "every subsequent Term of ten Years," though the period of "decade" is not used. In the New York state constitution, however, not only is "decade" mentioned (also for apportionment of representatives), but its exact year bounds are explicitly clarified:

> ... if, in any decade, counting from and including that which begins with the year
> nineteen hundred thirty-one, such a readjustment or alteration is not made at the time
> above prescribed, it shall be made at a subsequent session occurring not later than the
> sixth year of such decade, meaning not later than nineteen hundred thirty-six,
> nineteen hundred forty-six, nineteen hundred fifty-six, and so on ...[^ny]

Between the mention of 1931 as the beginning of a decade and the mention of 1936 as the sixth year of the decade, the New York constitution clearly takes the Ordinal position.

Elsewhere, back to the whole US, the legal language around the decennial census itself does not seem to mention "decade" anywhere, not in any historic iteration of the Census Act and, surprisingly, not in the [US Code TItle 13](https://www.law.cornell.edu/uscode/text/13) that characterizes the census process.


* Give ISO definition
* Give census definition
* Give historical newspaper evidence
* Arrrrgh so what's the answer??? Connect to historical debate about centuries.


# Centuries of History of Centuries


Some might recall similar questions about the true beginning of the new millennium or new century --- the first of January, but 2000 or 2001? More generally, do centuries begin in years ending with `00` or with `01`? It depends on which camp you're in.

To count centuries, the Cardinals would say that we're in _the 2000s_, running from 2000 to 2099, and last we were in _the 1900s_, running from 1900 to 1999. Surely one cannot deny the legitimacy of referring to centuries as such. The Ordinals, on the other hand, would say that we're in the _the 21st century_, running from 2001 to 2100, and last we were in _the 20th century_, running from 1901 to 2000.

{% include two_images.html
	filename1="decade/washington-post-1899-12-31-table.png"
	description1=""
	filename2="decade/boston-herald-1899-12-10-enumeration.png"
	description2=""
	caption="A reader's table showing how to count a decade in the 31 December 1899 _Washington Post_, and an enumeration by the Provost of University of Pennsylvania in the 10 December 1899 _Boston Herald_ ([footnote 6](#fn:colleges))." %}


At the level of centuries, this debate has raged for... centuries, most notably the transition from 19th to 20th centuries. _[La fin de siècle](https://en.wikipedia.org/wiki/Fin_de_si%C3%A8cle)_, as it was known in France and in high culture, garnered tremendous attention worldwide. Philosophers, intellectuals, journalists, emperors, and popes all debated and ruled on the exact beginning of the 20th century, their efforts published for mass audiences in the world's newspapers. In response, where today we have social media, back then they had letters to the editor.

{% capture three_articles_caption %}
Three example articles across the centuries. De Laisement's "Dissertation sur le commencement du siècle prochain" ([1699](#fn:delaisement)), _The London Times_ (26 December 1799), and _The Nashville American_ (4 January 1899).
{% endcapture %}
{% include three_images.html
	filename1="decade/delaisement-dissertation-first-page.png"
	filename2="decade/times-london-1799-the-next-century.png"
	filename3="decade/tennesseean-1900-century-not-ended.png"
	caption=three_articles_caption %}

Stephen Jay Gould deemed the debate to be one between "high culture" on one side --- the scholarly mantle of Ordinals --- and "vernacular culture" on the other --- the common-sense laurels of Cardinals, most notably expressed in the 1890s.[^gouldculture]
A century later, he remarks, it would be Arthur C. Clarke's _2001_ vs. Prince's _1999_.

On the side of high culture, insisting that centuries begin in the `01` years, stood [Pope Leo XIII](https://en.wikipedia.org/wiki/Pope_Leo_XIII),[^popeaddress] astronomers going back centuries,[^loc] and many newspaper editors. They even recognized the distinction as one between cardinal and ordinal numbers, going back at least to 1699.[^delaisement]

{% capture german_song %}
Have you wondered whether we've started a new decade as much as this person? "[Wann fängt das XIX. Jahrhundert an?](https://books.google.com/books?id=tRVDAAAAcAAJ&pg=PA857&lpg=PA857&dq=%22Wann+fangt+das+XIX.+Jahrhundert+an?%22&source=bl&ots=rn7HjVD-2F&sig=ACfU3U3D1TvWV04VyzhSD1mx9GH6xczr_Q&hl=en&sa=X&ved=2ahUKEwi44ZLTi-nmAhXjV98KHWmHC2QQ6AEwA3oECAQQAQ#v=onepage&q=%22Wann%20fangt%20das%20XIX.%20Jahrhundert%20an%3F%22&f=false)" ("When Does the 19th Century Begin?") _Allgemeine musikalische Zeitung_, 18 September 1799.
{% endcapture %}
{% include image.html
	img_style="width: 50%;"
	filename="decade/german-music.png"
	description=german_song
	figcaption_style="width: 600px;" %}

On the side of vernacular culture, arguing for the `00` years, stood Kaiser Wilhelm II of Germany,[^kaiser] the Wellesley College president,[^colleges] and --- most importantly --- the common man. One such common man articulated his position on the "great secular event" of the turn of the century as a populist backlash to "the abacists":

> Shall we wait now a whole year for 1901, at the behest of the abacists? No, we will not pass over the significant year 1900, which is stamped with the great secular change, but with cheers we will welcome it and the new century. The 1900 men, who compose the vast majority of the people, say to their opponents: "We freely admit that the century you have in your mind, the artificial century, begins in 1901, but the natural century (which we prefer) begins in 1900."[^abacists]

Also in the Cardinals camp on the century question is, again, ISO 8601. It defines centuries analogously to how it defines decades.[^iso8601century]

In the end, with the intelligentsia on their side the Ordinals won the debate on centuries, as long as the ordinally-specified phrase "the `__`th century" remains the common expression for centurial periods of history. Then do they also win the debate on decades?

# What's a Decade Anyway?

A millennium is grandiose. A century is once in a lifetime. But a decade? That's pedestrian. Indeed, among these three periodizations of history, the decade stands alone as being primarily cultural in nature. "Decades are not a function of calendar time," wrote Newsweek journalist Bill Barol. "They are trends, values, and associations, bundled up and tied together in the national memory."[^newsweek]

Without the grandeur of a century, the decade question has prompted far less (serious) debate. The decade, as a periodization of history, is a fairly recent concept. In the 1940s historian Marc Bloch had already warned against the "insidious" practice of periodizing by centuries:
> We no longer name ages after their heroes. We very prudently number them in sequence every hundred years, starting from a point fixed, once and for all, at the year 1 of the Christian era. [...] Unfortunately, no law of history enjoins that only those years whose dates end with the figures '01' coincide with the critical points of human evolution.[^bloch]

If centurial thinking already had "no rational basis," what about the decade? Warren Susman criticized it as "a special and perhaps characteristically American way of seeing the past: as a series of decades that fit neatly into limits imposed by man-made calendars."[^susman] Jason Scott Smith, in his 1997 article "[The Strange History of the Decade](http://www.jstor.org/stable/3789661)," traces the history of the decade in primarily American, primarily cultural thought.[^smith] "The decade contributes to an abbreviated historical attention span---cause and effect are confused, and the record of the past is reduced to a 'progression of cultural styles.'" When did this begin? According to Smith, oweing to the World War, to global revolutions of technology and politics, and to a subsequent decade full of nostalgia, the 1920s were "the first decade truly to legitimate a ten-year span of time as a historic category."




{::comment}
{% capture dialogue %}
A presentation of two year counting methods in <em>Literary Digest</em>, Vol. 19, No. 27, <a href="https://archive.org/details/literarydigest19newy/page/798" title="Literary Digest dialogue about counting years">p. 799</a>.
{% endcapture %}
{% include image.html filename="decade/literary-digest-1899-dialogue.png" description=dialogue %}
{:/comment}



{::comment}
Smith:
* the 1920s was "the first decade truly to legitimate a ten-year span of time as a historic category."
* "Allen employed the decade as a device to organize and to describe culturally shared events, rather than treating it as an arbitrarily strict unit of historic time."
* "A rising sense of generational self-awareness, the perceived acceleration of time, a sense of the new, combined with a growing identification between the forces of youth culture and the phenomenon of cultural rebirth, replaced the linear, progressive conception of time that had dominated the thinking of much of the nineteenth century."
* "Decades are not a function of calendar time," states Newsweek journalist Bill Barol. "They are trends, values, and associations, bundled up and tied together in the national memory."
* "Periodizing history via the decade is just one example of a broader tendency in American culture, the process of 'disremembering the past while historicizing the present.' The decade contributes to an abbreviated historical attention span---cause and effect are confused, and the record of the past is reduced to a 'progression of cultural styles.'"
* NYT article: "What's in a decade, anyway? And how is it that this arbitrary and slim crosscutting of time, a mere 10 years, has grown and flourished to the point that we all walk around in a self-conscious haze about what a new decade represents even before the previous one has tolled its last?"
{:/comment}

This difference in the idea of the decade, as compared to centuries, also matches the common language to talk about them. Here, the Cardinals have the advantage: you're far less likely to hear talk of "the 203rd decade" than "the 2020s." The situation is reversed for centuries: "the 21st century" is more common than "the 2000s." While it's not immediately clear how to search for "the `__`s" vs. either "the `__` century" or "the `__` decade," we can at least compare the frequency of the ordinal reference to "centuries" vs. to "decades," which [the following Google Ngram Viewer results](https://books.google.com/ngrams/graph?content=_NUM_+st+century+%2B+_NUM_+nd+century+%2B+_NUM_+rd+century+%2B+_NUM_+th+century%2C_NUM_+st+decade+%2B+_NUM_+nd+decade+%2B+_NUM_+rd+decade+%2B+_NUM_+th+decade&case_insensitive=on&year_start=1700&year_end=2020&corpus=15&smoothing=3&share=&direct_url=t1%3B%2C%28_NUM_%20st%20century%20%2B%20%20_NUM_%20nd%20century%20%2B%20%20_NUM_%20rd%20century%20%2B%20%20_NUM_%20th%20century%29%3B%2Cc0%3B.t1%3B%2C%28_NUM_%20st%20decade%20%2B%20%20_NUM_%20nd%20decade%20%2B%20%20_NUM_%20rd%20decade%20%2B%20%20_NUM_%20th%20decade%29%3B%2Cc0) show.

{% include image.html
	filename="decade/ngram-results-ordinals.png"
	description="Google Ngram results showing frequency of ordinal reference to centuries vs. to decades."
	 %}

Taking the cardinal invocation of decades to be far more common than the ordinal invocation, it seems to me that the Cardinals win the decade debate; the decades begin on the `00` years. And although this is the opposite of century counting, the distinction in the concept of the decade seems to further warrant the distinction in counting.

An alternative view sees a decade not as a particular sequence of ten-year periods that start either on the `00` or `01` years, but as _any_ ten-year period. This latter view was [introduced into the public consciousness](https://sports.yahoo.com/leafs-rielly-on-the-arrival-of-2020-i-dont-think-its-even-the-end-of-a-decade-174009256.html) recently by Morgan Rielly, a player for the Toronto Maple Leafs hockey team:

> I don’t think it’s even the end of a decade. Every new year is the end of a decade.
> 2008 to 2018 [sic] is a decade. 2009 to 2019 [sic] is a decade. Every f---ing one is the end of
> a decade. So all these people saying the decade's come to an end --- that happens
> every new year.
> 
> So, it's the end of the century, it's the end of you-name-it.

In terms of the ISO 8601 standard, that's the distinction between _decades_ (as introduced earlier) and _[time intervals](https://en.wikipedia.org/wiki/ISO_8601#Time_intervals) of duration ten years_. Rielly gives two examples of such time intervals: `2008/2017` and `2009/2018`, both valid time intervals of year precision according to ISO 8601, and also expressible as `2008/P10Y` and `P10Y/2019` respectively. Or they could be ten-year time intervals at minute granularity, e.g., `2009-12-31T14:30/P10Y` as the decade beginning at 2:30 pm on 31 December 2009 and ending at 2:30 pm on 31 December 2019.








[^gouldculture]:
    Stephen Jay Gould, [_Questioning the Millennium_](https://www.hup.harvard.edu/catalog.php?isbn=9780674061644), 1997, Part 2. 

[^popeaddress]:
	The scholarly Pope Leo XIII issued [an address on 13 November 1899](https://books.google.com/books?id=JvrNAAAAMAAJ&pg=PA79&lpg=PA79&dq=%22cum+insuper+media+nocte+postremae+diei+mensis+Decembris%22&source=bl&ots=0mgwgee0Pc&sig=ACfU3U1EVivZRspzcdE8ODg6UelALL4faQ&hl=en&sa=X&ved=2ahUKEwj76JbWuOPmAhXExVkKHb68CAgQ6AEwAHoECAkQAQ#v=onepage&q=%22cum%20insuper%20media%20nocte%20postremae%20diei%20mensis%20Decembris%22&f=false) clarifying that "at midnight of the last day of December of the coming year [1900] the present century will come to an end." It was reported in various US newspapers, notably cited in "[Is the Twentieth Century Here, Or Is It Not?](https://archive.org/details/literarydigest19newy/page/798)", _Literary Digest_, Vol 19, No 27, p. 798.

[^loc]:
	For an extensive list of scholarly debate about when centuries begin and end, see "[The Battle of the Centuries](https://www.loc.gov/rr/scitech/battle.html)," an extensive bibliography compiled by Senior Science Specialist Ruth Freitag at the Library of Congress.

[^delaisement]:
	De Laisement, "[Dissertation sur le commencement du siècle prochain et de la solution du problème scavoir laquelle des deux années 1700 ou 1701 et la première du siècle](https://books.google.com/books?id=GmbIH1WTuTUC&pg=PP1&lpg=PP1&dq=%22Dissertation+sur+le+commencement+du+siecle+prochain%22&source=bl&ots=u-CigPTsTL&sig=ACfU3U0I1bJ0HGhVtqEd-xhAG9o85yXXnQ&hl=en&sa=X&ved=2ahUKEwiin6epzOfmAhXBqlkKHYSTCBwQ6AEwAHoECAgQAQ#v=onepage&q&f=false)," 1699. On page 9 he introduces the distinction between cardinal and ordinal numbers.

<!-- [^schwartz]:
	Schwartz, Hillel. "Fin-de-Siècle Fantasies." _The New Republic_, 30 July 1990, p. 24. An article featuring an extensive history, going back to biblical times, of cultural emphasis on centuries. -->

[^kaiser]:
	An account of Kaiser Wilhelm II's erroneous declaration of 1900 as the start of the century, from Bode's "[Liminal Projections: Utopian and Apocalyptic Visions, 1790s : 1990s](https://brill.com/view/book/edcoll/9789004333970/B9789004333970-s010.xml)":

	> Reichskanzler Fürst zu Hohenlohe-Schillingfürst asked his majesty Kaiser Wilhelm II in a
	> telegram [dated 4 December 1899] most submissively to decide when the beginning of the new
	> century was to be celebrated, 'allerunterhänigst um Entscheidung' ['wholeheartedly for a
	> decision'], 'wann der Beginn des neuen Jahrhunderts zu feiern ist' ['when to celebrate the
	> beginning of the new century']. The Kaiser declared it should be in 1900 and few of his
	> subjects dared object, though pockets of resistance were reported from Bavaria.
	
	The Kaiser's response: "am 1. Januar 1899," a [telegraphic typo](https://www.faz.net/aktuell/feuilleton/buecher/rezension-sachbuch-der-grosse-fruehjahrsputz-der-welt-11312316.html?printPagedArticle=true#pageIndex_2) according to Richard Kämmerlings in the German FAZ newspaper.

[^colleges]:
    At the end of 1899 the Boston Herald asked an array of college presidents to conclusivey determine the year that begins the 20th century. In [the December 10th issue](/assets/img/decade/Boston_Herald_published_as_THE_SUNDAY_HERALD.___December_10_1899.pdf) they published the results in a huge spread, along with a history of calendar systems. Colleges whose presidents or other professors correctly said 1901: Princeton, Cornell, Columbia, Penn, Vassar, Bowdoin, Dartmouth, Brown, Yale, Harvard, and Chicago. Those who incorrectly answered 1900: Wellesley, Tufts, and Smith. Elsewhere the New York Tribune editor writes of the 1900 error: "This notion has about disappeared, however, before the gaze of calm eyed mathematics. The only persons of prominence who ever held it were the president of Wellesley College and the German Emperor" (12 December 1899, "[La Fin de Siecle](https://www.newspapers.com/image/206532828/?terms=wellesley)," pg. 6).

[^abacists]:
    Neal H. Ewing, quoted in "[The Natural Century](https://books.google.com/books?id=hS1LAQAAMAAJ&pg=PA62&lpg=PA62&dq=%22the+centurial+figures+are+the+symbol%22&source=bl&ots=293RC9I4c9&sig=ACfU3U2_s9Np82aD3fVL_FQps1Sq44ayzw&hl=en&sa=X&ved=2ahUKEwjws8mRre3mAhWIVN8KHTfaBH8Q6AEwAHoECAYQAQ#v=onepage&q=%22the%20centurial%20figures%20are%20the%20symbol%22&f=false)," _The American Architect and Building News_, Volume 65, 1899, pg. 62.

[^newsweek]:
	Bill Barol, "The Eighties Are Over," _Newsweek_, 4 Jan 1988, pp. 40-41.

[^bloch]:
	Marc Bloch, _The Historian's Craft_, 1944, pp. 181-182. Another passage from this book that's particularly relevant for those of us interested in [the time zone database (tzdb)](https://typesandtimes.net/2019/05/royal-astronomical-society-python):
	> Now, the scholar loves close dating. He finds it both an appeasement to his instinctive horror
	> of the vague and a great comfort to the conscience. He wants to have read and to have checked
	> everything which concerns his subject. [...] However, let us beware of worshipping the idol of
	> false precision. The most precise measurement is not necessarily the one which refers to the
	> smallest unit of time---in which case, we should have to prefer not only a year to a decade,
	> but also a second to a day---it is the one which is best adapted to the nature of the events. 

[^susman]:
	Warren Susman, _Culture as History_, 1973.

[^smith]:
	Jason Scott Smith. "[The Strange History of the Decade: Modernity, Nostalgia, and the Perils of Periodization](http://www.jstor.org/stable/3789661)." _Journal of Social History_, vol. 32, no. 2, 1998. All of the discussion about the particularity of the decade above comes from this fascinating article!

[^iso8601decade]:
	For the definition of decades, see ISO 8601-1:2019, Section 4.3.11, and extended definitions in Part 2, ISO 8601-2:2019, Sections 4.3.5 and 4.4.1.7.

[^iso8601calendar]:
	For the reinterpreted definition of the Gregorian calendar, see ISO 8601-1:2019, Section 4.2.1. A [draft copy](https://www.loc.gov/standards/datetime/iso-tc154-wg5_n0038_iso_wd_8601-1_2016-02-16.pdf) of an older version exists on a web server for the Library of Congress; Section 3.2.1 there. The Java library for date and time --- `java.time` or JSR 310, one of my all-time favorite APIs --- [describes](https://docs.oracle.com/javase/8/docs/api/java/time/chrono/IsoChronology.html) the ISO calendar system as "the _de facto_ world calendar."

[^yearzero]:
	Virtually every discussion of the century debate includes mention of the absence of year zero in the Gregorian calendar (often called "the astronomical year zero"). See [Gould](#fn:gouldculture) for a discussion of the creation of Anno Domini by the monk "Dennis." "In short, Dennis did not begin time at zero, thus discombobulating our usual notions of counting. During the year that Jesus was one year old, the time system that supposedly started with his birth was two years old. (Babies are zero years old until their first birthday; modern time was already one year old at its inception.)" There's also a particularly expansive discussion of this history in _[The Boston Herald](#fn:colleges)_.

[^iso8601century]:
	For the definition of centuries, see ISO 8601-1:2019, Section 4.3.12, and extended definitions in Part 2, ISO 8601-2:2019, Sections 4.3.6 and 4.4.1.8. For example, the 21st century, "the 2000s," is represented as `20C`, and like with decades, there are zero (`0C`) and negative zero (`-0C`) centuries that both contain year 0.

[^ny]:
	_[New York State Constitution](https://www.dos.ny.gov/info/constitution.htm)_, Article III, Section 4.