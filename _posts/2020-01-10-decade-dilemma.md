---
layout: post-with-image
title: "How to Periodize History: 2020 and the Decade Dilemma"
excerpt: "Does 2020 begin a new decade? To answer this question we must consult the Pope, the Kaiser, the census, a hockey player, and ISO 8601."
image:
  filename:  "decade/new-century-cartoon-boomer.jpg"
  alt:       "Illustration on the front page of the 1 January 1901 issue of The Washington Times, altered."
  caption:   "Illustration on the front page of the 1 January 1901 issue of The Washington Times, altered."

date: 2020-01-10
---

A new year in the Common Era has arrived, surely to inundate us all with visual acuity puns. But has _a new decade_ also arrived?

The question has percolated through the loud void of social media, reverberating across [digital content mills and respectable media outlets alike](https://duckduckgo.com/?q=is+2020+a+new+decade&t=h_&ia=news). We all find ourselves burning with new intensity, searching for any authoritative voice to make sense of this quandary. _[The New York Times](https://www.nytimes.com/2019/11/28/us/what-is-decade.html)_, _[The Irish Times](https://www.irishtimes.com/opinion/go-ahead-celebrate-the-new-decade-a-year-early-just-count-me-out-1.4127481)_, _[India Today](https://www.indiatoday.in/trending-news/story/when-does-the-new-decade-start-are-you-team-january-1-2020-or-team-january-1-2021-1624530-2019-12-02)_, _[Farmer's Almanac](https://www.farmersalmanac.com/new-decade-2020-or-2021-100900), [Timeanddate.com](https://www.timeanddate.com/calendar/decade.html), please somebody tell us!_

Others resort to the nihilistic view that decades never begin or end, or rather, begin and end always and forever --- they're just ten-year spans of time without any defined order between them.[^justspans] This perspective was [introduced into the public mind](https://sports.yahoo.com/leafs-rielly-on-the-arrival-of-2020-i-dont-think-its-even-the-end-of-a-decade-174009256.html) recently by Morgan Rielly, a player for the Toronto Maple Leafs hockey team:

> I don’t think it’s even the end of a decade. Every new year is the end of a decade.
> 2008 to 2018 [sic] is a decade. 2009 to 2019 [sic] is a decade. Every f---ing one is the end of
> a decade. So all these people saying the decade's come to an end --- that happens
> every new year.
> 
> So, it's the end of the century, it's the end of you-name-it.



# The Two Camps of Counting

When asked whether 2020 marks a new decade, people fall into two camps, which I'll call the _Cardinals_ and the _Ordinals_.

* The Cardinals answer _yes, for decades are identified by their digit representations_. The previous decade, the 2010s, included the years 2010 through 2019, while the new decade, the 2020s, includes the years 2020 through 2029.

* The Ordinals, on the other hand, answer _no, for decades are identified by ordinal numbers counted in sequence from the beginning_. The current decade, the 202nd (or the 2nd of the 21st century), includes the years 2011 through 2020, while the next decade, the 203rd, will include the years 2021 through 2030.

These two camps are both so rational and natural that a person in one camp might deny the very existence of the other. Not since "[the dress](https://en.wikipedia.org/wiki/The_dress)" of 2015 --- is that still this decade? --- have two camps formed so resolutely online. Are they not both completely legitimate ways to count off the decades? If only some authoritative source could lend its weight to either camp.

{% include two_images.html
	id="fig:cartoonresponse"
	filename1="decade/chicago-tribune-1929-cartoon-naming-decades.jpg"
	filename2="decade/chicago-tribune-1930-response-to-cartoon-naming-decades.jpg"
	img2_style="height: 284px;"
	caption="Naming the next decade in the 29 December 1929 _Chicago Tribune_, followed by an angry letter to the editor disputing the cartoon in the 4 January 1930 issue." %}

In an earlier time, the Pope himself might have served as just such an authority. After all, our calendar isn't called "[Gregorian](https://en.wikipedia.org/wiki/Gregorian_calendar)" for nothing; [Pope Gregory XIII]((https://en.wikipedia.org/wiki/Pope_Gregory_XIII)) commissioned it in the 16th century. Recent articles on the subject have consulted [meteorological associations](https://www.forbes.com/sites/marshallshepherd/2020/01/01/is-2020-the-start-of-a-new-decadea-human-technical-and-climate-perspective/#18ed2fd3ee2f), [philosophy professors](https://www.usatoday.com/story/news/nation/2019/12/10/2020-start-new-decade-some-say-thats-not-until-2021/4366467002/), and [the United States Naval Observatory](https://www.nytimes.com/2019/11/28/us/what-is-decade.html).

I will put forward two potential authoritative sources on whether decades should be counted according to Cardinals or to Ordinals: ISO 8601 and decennial census legislation. And unfortunately, they lead us into different camps.

# In One Corner, the Geeks

[ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) is the specification of (representations of) dates, times, and other calendar entities for use in computing. The International Organization for Standardization defines new versions every so often, the most recent one in 2019. It's the closest thing we've got to a gold standard for dates and times in software. _What's the right way to represent dates? Local times of day? Local times of day for some time zone? Time scales? Leap seconds?_

ISO 8601 even defines a new standard calendar adapted from the Gregorian calendar.[^iso8601calendar] Just as Common Era was a secular substitution for Anno Domini, the ISO 8601 calendar supplants the Gregorian calendar. No more pesky Year 1 C.E. preceded by Year 1 B.C.E.; ISO 8601 has _Year Zero_,[^yearzero] and negative years. That essentially makes the Ordinal thinking moot, as the first ISO 8601 decade includes the years 0 through 9, not 1 through 10.

Indeed, decades, as defined in ISO 8601, are the years `XXX0` through `XXX9`.[^iso8601decade] For example, using `J` to denote decades, "the 2020s" are represented as `202J`; the "zero decade" is represented as `0J`; and "the negative zero decade," meaning years -9 through 0, is represented as `-0J`. Somewhat strangely, the latter two decades both include year 0. As a consequence, ISO 8601 _really_ rejects the Ordinals since decades no longer describe an ordered, mutually exclusive sequence of spans of ten years.

ISO 8601 is firmly in the camp of the Cardinals.


{% include image.html
	filename="decade/boston-herald-1899-when-new-century-begins.png"
	description="Headline of the [10 December 1899 _Boston Herald_](#fn:colleges) that sought input from collegiate experts." %}

# In the Other Corner, the Wonks

Not everyone finds ISO 8601 to be all that authoritative. But what about nation states? Although they don't generally have reason to weigh in on the exact definitions of time, they do tend to institutionalize the decade in particular --- as the period in which the government conducts a census. For those governments that conduct them decennially, surely they must spell out the precise formal interpretation of decades, right?

Recent legislation in the European Union does exactly that. In its [standardization of population and housing census methodology](https://ec.europa.eu/eurostat/documents/3859598/9670557/KS-GQ-18-010-EN-N.pdf/c3df7fcb-f134-4398-94c8-4be0b7ec0494) for member states, the EU specifies that member nations run a census "every decade" on a "reference date" of their choosing. "The first reference year shall be 2011. [...] Reference years shall fall during the beginning of every decade."[^eucensus] In other words, the `1` years begin the decades and therefore the EU implicitly takes up the Ordinal position.

For the United States in particular, it's even [in our Constitution](https://www.census.gov/history/pdf/Article_1_Section_2.pdf) to apportion Congressional representatives according to state populations counted "every subsequent Term of ten Years," though the period of "decade" is not used. In [the New York state constitution](https://www.dos.ny.gov/info/constitution.htm), however, not only is "decade" mentioned (also for apportionment of representatives), but its exact year bounds are explicitly clarified:

> ... if, in any decade, counting from and including that which begins with the year
> nineteen hundred thirty-one, such a readjustment or alteration is not made at the time
> above prescribed, it shall be made at a subsequent session occurring not later than the
> sixth year of such decade, meaning not later than nineteen hundred thirty-six,
> nineteen hundred forty-six, nineteen hundred fifty-six, and so on ...[^ny]

Between the mention of 1931 as the beginning of a decade and the mention of 1936 as the sixth year of the decade, the New York constitution clearly takes the Ordinal position.

Back to the whole US, the legal language around the decennial census itself does not seem to mention "decade" anywhere, not in any [historic iteration of the Census Act](https://www.census.gov/history/www/reference/legislation/) and, surprisingly, not in the [US Code Title 13](https://www.law.cornell.edu/uscode/text/13) that codifies the census bureaucracy. Our census occurs in the `0` years but there's no qualification that these _begin_ each decade. A 1908 American Statistical Association [survey of census methodology across the Americas](https://www.jstor.org/stable/2275965), however, sheds some light on the counting in this field:

> The most generally accepted dates for a decennial census are those that begin or end decades. The tenth year of the decade has been accepted in the United States and in several European countries, and in Brazil. England and most of her colonies accept the first year of the decade.[^censusarticle]

The US census occurs in the `0` years, referred to as the tenth (last) years of the decades, while the UK census occurs in the `1` years, referred to as the first years.

Altogether it seems that governments, at least those conducting decennial censuses in the anglophone world, take up the Ordinal position on decades.

# The Historical Record

With the geek and wonk authorities taking contradictory positions on the decade question, what about popular usage in the archives of major newspapers and other such publications? A scattershot of archival records, generally by searching for `"new decade"`, suggests that both counting styles have been used over the past century or so---and sometimes inconsistently in the same place. Such evidence includes:

{% capture label_ordinal %}
<span style="display: inline-block; width: 80px;">Ordinal:</span>
{% endcapture %}
{% capture label_cardinal %}
<span style="display: inline-block; width: 80px;">Cardinal:</span>
{% endcapture %}
{% capture label_both %}
<span style="display: inline-block; width: 80px;">Both:</span>
{% endcapture %}

* {{label_ordinal}} An [article in _Science_](https://books.google.com/books?id=zxxCAQAAMAAJ&pg=PA548&lpg=PA548&dq=lalande+Bibliographie+astronomique+%22decade%22&source=bl&ots=cHM2GTHXZj&sig=ACfU3U0zkocZC4YS7Dxd0ZmV2-gvOu9OXg&hl=en&sa=X&ved=2ahUKEwj5sInnvt7mAhVPhOAKHWn6BKMQ6AEwAHoECAkQAQ#v=onepage&q=lalande%20Bibliographie%20astronomique%20%22decade%22&f=false) tabulating a century-old bibliography of astronomy texts in 1906.[^sciencetab]
* {{label_cardinal}} A [report](https://books.google.com/books?id=cB6gAAAAMAAJ&pg=PA199&dq=%22of+the+new+decade%22&hl=en&newbks=1&newbks_redir=0&sa=X&ved=2ahUKEwiE5frkvtzmAhWhmOAKHY4FASAQ6AEwAHoECAEQAg#v=onepage&q=decade&f=false) on a decennial medical conference in the 1876 _Transactions of the Medical Society of the State of New York_.[^medreport]
* {{label_cardinal}} A [_New York Times_ article](https://timesmachine.nytimes.com/timesmachine/1860/01/02/83214202.html?pageNumber=5) welcoming the new year --- and decade --- in 1860.[^nyt1860]
* {{label_both}} An [editorial](https://timesmachine.nytimes.com/timesmachine/1930/04/27/96111172.html?pageNumber=83) about the state of international politics in 1930, using ordinals to describe the decade but beginning from 1930![^nyt1930]
* {{label_ordinal}} A [swanky fundraiser](https://timesmachine.nytimes.com/timesmachine/1941/01/30/85317887.html?pageNumber=24) called the "New Decade Mardi Gras and Ball" in January 1941, as reported by the _New York Times_.[^nyt1941]
* {{label_cardinal}} A different, possibly [less swanky fundraiser](https://timesmachine.nytimes.com/timesmachine/1949/11/13/93550239.html?pageNumber=87) also called "New Decade" in December 1949, also reported by the _New York Times_.[^nyt1949]
* {{label_cardinal}} A [1960 call](https://timesmachine.nytimes.com/timesmachine/1960/01/02/99282204.html?pageNumber=12) for a new Renaissance of worldly experts, not just invoking "our new decade" but identifying three decades cardinally.[^nyt1960]
* {{label_cardinal}} The [inaugural speech](https://www.nytimes.com/1970/01/01/archives/text-of-the-lindsay-inaugural-speech.html) of New York City Mayor John Lindsay on the last day of 1969.[^nyt1970]
* {{label_cardinal}} A New Year message in the 1880 _New York Tribune_.[^nytrib1880]
* {{label_ordinal}} A look at the plays of "the new decade" in the 1890 _New York Tribune_, ten years later but with a different position.[^nytrib1890]
* {{label_cardinal}} A celebration of "holiday trade" in the 1889 _Boston Globe_.[^bosglobe1889]
* {{label_ordinal}} A chest-beating celebration of the _Chicago Tribune_'s year ahead in 1921.[^ctrib1921]
* {{label_cardinal}} A [cartoon](#fig:cartoonresponse) about historians naming "the dying decade" in the 1929 _Chicago Tribune_.[^ctrib1929]
* {{label_ordinal}} An [angry reader response](#fig:cartoonresponse) to that cartoon's mistake identifying the decade.[^ctrib1930]
* {{label_ordinal}} An [editorial response](/assets/img/decade/New_York_Tribune_Sun__Dec_23__1900.pdf) to a reader's query about the start of the new century in 1900, linking it explicitly to the decade dilemma too, in the _New York Tribune_. The masterful response cites two encyclopedias' entries on "Chronology," explains the frustrated lack of astronomical year zero, provides multiple enumerations of years in decades, concurs with our philosophical Canadian hockey player Rielly on the multitude of decades available, and even cedes territory to the Cardinals on common expressions like "in the [eighteen!] sixties."[^nytrib1900]

Whew. With all the discord around counting decades, how do we resolve the dilemma? To better equip ourselves with the tools to conclusively resolve it, we should first look to _the century dilemma_.

{% include image.html
	filename="decade/nytribune-1900-spread-to-decades.png"
	img_style="width: 60%;"
	description="A humble letter to the editor followed by a masterful response in the _New York Tribune_ ([23 December 1900](#fn:nytrib1900))." %}


# Centuries of History of Centuries

At the level of centuries, this debate has raged for... centuries, most notably the transition from 19th to 20th centuries. _[La fin de siècle](https://en.wikipedia.org/wiki/Fin_de_si%C3%A8cle)_, as it was known in France and in high culture, garnered tremendous attention worldwide. Philosophers, intellectuals, journalists, emperors, and popes all debated and ruled on the exact beginning of the 20th century, their efforts published for mass audiences in the world's newspapers. In response, where today we have social media, back then they had letters to the editor.

{% capture three_articles_caption %}
Three example articles across the centuries. De Laisement's "Dissertation sur le commencement du siècle prochain" ([1699](#fn:delaisement)), _The London Times_ (26 December 1799), and _The Nashville American_ (4 January 1899).
{% endcapture %}
{% include three_images.html
	id="fig:generations"
	filename1="decade/delaisement-dissertation-first-page.png"
	filename2="decade/times-london-1799-the-next-century.png"
	filename3="decade/tennesseean-1900-century-not-ended.png"
	caption=three_articles_caption %}

To count centuries, the Cardinals would say that we're in _the 2000s_, running from 2000 to 2099, and last we were in _the 1900s_, running from 1900 to 1999. Surely one cannot deny the legitimacy of referring to centuries as such. The Ordinals, on the other hand, would say that we're in the _the 21st century_, running from 2001 to 2100, and last we were in _the 20th century_, running from 1901 to 2000.

{% include two_images.html
	filename1="decade/washington-post-1899-12-31-table.png"
	description1=""
	filename2="decade/boston-herald-1899-12-10-enumeration.png"
	description2=""
	caption="A reader's table showing how to count a decade in the 31 December 1899 _Washington Post_, and an enumeration by the Provost of University of Pennsylvania in the 10 December 1899 _Boston Herald_ ([footnote 6](#fn:colleges))." %}


Stephen Jay Gould deemed the debate to be one between "high culture" on one side --- the scholarly mantle of Ordinals --- and "vernacular culture" on the other --- the common-sense laurels of Cardinals, most notably expressed in the 1890s.[^gouldculture]
A century later, he remarks, it would be Arthur C. Clarke's _2001_ vs. Prince's _1999_.

On the side of high culture, insisting that centuries begin in the `01` years, stood [Pope Leo XIII](https://en.wikipedia.org/wiki/Pope_Leo_XIII),[^popeaddress] astronomers going back centuries,[^loc] and many newspaper editors. They even recognized the distinction as one between cardinal and ordinal numbers, going back at least to 1699.[^delaisement]

{% capture german_song %}
Left: Have you wondered whether we've started a new decade as much as this person? "[Wann fängt das XIX. Jahrhundert an?](https://books.google.com/books?id=tRVDAAAAcAAJ&pg=PA857&lpg=PA857&dq=%22Wann+fangt+das+XIX.+Jahrhundert+an?%22&source=bl&ots=rn7HjVD-2F&sig=ACfU3U3D1TvWV04VyzhSD1mx9GH6xczr_Q&hl=en&sa=X&ved=2ahUKEwi44ZLTi-nmAhXjV98KHWmHC2QQ6AEwA3oECAQQAQ#v=onepage&q=%22Wann%20fangt%20das%20XIX.%20Jahrhundert%20an%3F%22&f=false)" ("When Does the 19th Century Begin?") _Allgemeine musikalische Zeitung_, 18 September 1799. Right: Cartoon from the 31 December 1899 _Washington Post_.
{% endcapture %}
{% include two_images.html
	img1_style="max-width: 55%;"
	filename1="decade/german-music.png"
	filename2="decade/washington-post-1899-12-31-cartoon.png"
	caption=german_song %}

On the side of vernacular culture, arguing for the `00` years, stood Kaiser Wilhelm II of Germany,[^kaiser] the Wellesley College president,[^colleges] and --- most importantly --- the common people. One such common person articulated his position on the "great secular event" of the turn of the century as a populist backlash to "the abacists":

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

This difference in the idea of the decade, as compared to centuries, also matches the common language to talk about them. Here, the Cardinals have the advantage: you're far less likely to hear talk of "the 203rd decade" than "the 2020s." The situation is reversed for centuries: "the 21st century" is more common than "the 2000s." While it's not immediately clear how to search for "the `__`s" vs. either "the `__` century" or "the `__` decade," we can at least compare the frequency of the ordinal reference to "centuries" vs. to "decades," shown by [the Google Ngram Viewer results below](https://books.google.com/ngrams/graph?content=_NUM_+st+century+%2B+_NUM_+nd+century+%2B+_NUM_+rd+century+%2B+_NUM_+th+century%2C_NUM_+st+decade+%2B+_NUM_+nd+decade+%2B+_NUM_+rd+decade+%2B+_NUM_+th+decade&case_insensitive=on&year_start=1700&year_end=2020&corpus=15&smoothing=3&share=&direct_url=t1%3B%2C%28_NUM_%20st%20century%20%2B%20%20_NUM_%20nd%20century%20%2B%20%20_NUM_%20rd%20century%20%2B%20%20_NUM_%20th%20century%29%3B%2Cc0%3B.t1%3B%2C%28_NUM_%20st%20decade%20%2B%20%20_NUM_%20nd%20decade%20%2B%20%20_NUM_%20rd%20decade%20%2B%20%20_NUM_%20th%20decade%29%3B%2Cc0).

{% include image.html
	filename="decade/ngram-results-ordinals.png"
	description="Google Ngram [results](https://books.google.com/ngrams/graph?content=_NUM_+st+century+%2B+_NUM_+nd+century+%2B+_NUM_+rd+century+%2B+_NUM_+th+century%2C_NUM_+st+decade+%2B+_NUM_+nd+decade+%2B+_NUM_+rd+decade+%2B+_NUM_+th+decade&case_insensitive=on&year_start=1700&year_end=2020&corpus=15&smoothing=3&share=&direct_url=t1%3B%2C%28_NUM_%20st%20century%20%2B%20%20_NUM_%20nd%20century%20%2B%20%20_NUM_%20rd%20century%20%2B%20%20_NUM_%20th%20century%29%3B%2Cc0%3B.t1%3B%2C%28_NUM_%20st%20decade%20%2B%20%20_NUM_%20nd%20decade%20%2B%20%20_NUM_%20rd%20decade%20%2B%20%20_NUM_%20th%20decade%29%3B%2Cc0) showing frequency of ordinal reference to centuries vs. to decades."
	 %}

Taking the cardinal invocation of decades to be far more common than the ordinal invocation, it seems to me that the Cardinals win the decade debate. And although this is the opposite of century counting, the distinction in the concept of the decade seems to further warrant the distinction in counting.

# Conclusion

In this article I've argued decades begin on `0` but centuries begin on `01`. (How sorry I am to disagree with the ISO 8601 standard in the latter case.) Of course, disregarding a chronological epoch like the year 1 C.E., decades are _also_ just arbitrary spans of ten years of time.

Have we now begun a new decade, the 2020s? I argue yes, while others would argue no. The only certainty is that, like the century debate, the question will never quite die; it will circle back around every decade. "DISCUSSION ALWAYS RECURS," one 1900 headline reminds us.[^nashville1900] But if each time we can piece together a bit more perspective, culturally and historically, we might finally be equipped to solve it for good.

Or maybe the common people will simply overpower the abacists.







---




[^gouldculture]:
    Stephen Jay Gould, [_Questioning the Millennium_](https://www.hup.harvard.edu/catalog.php?isbn=9780674061644), 1997, Part 2. 

[^popeaddress]:
	The scholarly Pope Leo XIII issued [an address on 13 November 1899](https://books.google.com/books?id=JvrNAAAAMAAJ&pg=PA79&lpg=PA79&dq=%22cum+insuper+media+nocte+postremae+diei+mensis+Decembris%22&source=bl&ots=0mgwgee0Pc&sig=ACfU3U1EVivZRspzcdE8ODg6UelALL4faQ&hl=en&sa=X&ved=2ahUKEwj76JbWuOPmAhXExVkKHb68CAgQ6AEwAHoECAkQAQ#v=onepage&q=%22cum%20insuper%20media%20nocte%20postremae%20diei%20mensis%20Decembris%22&f=false) clarifying that "at midnight of the last day of December of the coming year [1900] the present century will come to an end." It was reported in various US newspapers, notably cited in "[Is the Twentieth Century Here, Or Is It Not?](https://archive.org/details/literarydigest19newy/page/798)", _Literary Digest_, Vol 19, No 27, p. 798.

[^loc]:
	For an extensive list of scholarly debate about when centuries begin and end, see "[The Battle of the Centuries](https://www.loc.gov/rr/scitech/battle.html)," an extensive bibliography compiled by Senior Science Specialist Ruth Freitag at the Library of Congress.

[^delaisement]:
	De Laisement, "[Dissertation sur le commencement du siècle prochain et de la solution du problème scavoir laquelle des deux années 1700 ou 1701 et la première du siècle](https://books.google.com/books?id=GmbIH1WTuTUC&pg=PP1&lpg=PP1&dq=%22Dissertation+sur+le+commencement+du+siecle+prochain%22&source=bl&ots=u-CigPTsTL&sig=ACfU3U0I1bJ0HGhVtqEd-xhAG9o85yXXnQ&hl=en&sa=X&ved=2ahUKEwiin6epzOfmAhXBqlkKHYSTCBwQ6AEwAHoECAgQAQ#v=onepage&q&f=false)," 1699. On page 9 he introduces the distinction between cardinal and ordinal numbers.

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
	
[^censusarticle]:
    S. N. D. North, "[Uniformity and Co-Operation in the Census Methods of the Republics of the American Continent](https://www.jstor.org/stable/2275965)." _Publications of the American Statistical Association_, Vol. 11, No. 84, December 1908, pp. 301.
    
[^eucensus]:
    "[Regulation (EC) No. 763/2008 of the European Parliament and of the Council of 9 July 2008 on population and housing censuses](https://ec.europa.eu/eurostat/documents/3859598/9670557/KS-GQ-18-010-EN-N.pdf/c3df7fcb-f134-4398-94c8-4be0b7ec0494)," Article 5, Paragraph 1 ("Data transmission"), pp. 115 of linked document.

[^sciencetab]:
	Edward S. Holden, "[A Summary of the Bibliographie Astronomique of Lalande for the Years A.D. 130 to 1473, the Epoch at Which Scientific Books Began To Be Printed](https://books.google.com/books?id=zxxCAQAAMAAJ&pg=PA548&lpg=PA548&dq=lalande+Bibliographie+astronomique+%22decade%22&source=bl&ots=cHM2GTHXZj&sig=ACfU3U0zkocZC4YS7Dxd0ZmV2-gvOu9OXg&hl=en&sa=X&ved=2ahUKEwj5sInnvt7mAhVPhOAKHWn6BKMQ6AEwAHoECAkQAQ#v=onepage&q=lalande%20Bibliographie%20astronomique%20%22decade%22&f=false)," _Science_, New Series Vol. 23, No. 588, pp. 548. Holden tabulates the bibliographic data from Lalande, reproducing Lalande's (conventional) usage of ordinals for centuries; he also appears to give his own ordinal description of the decades within each century.

[^medreport]:
	E. R. Squibb, "[Report of Dr ER Squibb as Delegate to The American Medical Association on the US Pharmacopoeia](https://books.google.com/books?id=cB6gAAAAMAAJ&pg=PA199&dq=%22of+the+new+decade%22&hl=en&newbks=1&newbks_redir=0&sa=X&ved=2ahUKEwiE5frkvtzmAhWhmOAKHY4FASAQ6AEwAHoECAEQAg#v=onepage&q=decade&f=false)," _Transactions of the Medical Society of the State of New York_, 1876, pp. 199. The US Pharmacopoeia is a decennial conference occuring in the `0` years. Squibb mentions that the conventions are held on "the first year of the new decade."

[^nyt1860]:
	"[A Happy New Year](https://timesmachine.nytimes.com/timesmachine/1860/01/02/83214202.html?pageNumber=5)," _New York Times_, 2 January 1860, pp. 5. "The birthday of 1860, the commencement of a new decade, will not, we may fully anticipate, fall behind those of previous years, which have now joined the antediluvian era, to which the poet makes reference."

[^nyt1930]:
	"[Towering Problems of the New Decade](https://timesmachine.nytimes.com/timesmachine/1930/04/27/96111172.html?pageNumber=83)," _New York Times_, 27 April 1930, pp. 83. "As the fourth decade of the twentieth century opens [...] What are likely to be the dominant trends of the decade just beginning?"

[^nyt1941]:
	"[New Decade Dance to be Held Tonight](https://timesmachine.nytimes.com/timesmachine/1941/01/30/85317887.html?pageNumber=24)," _New York Times_, 30 January 1941, pp. 24.

[^nyt1949]:
	"[New Decade Dance to be Held Dec. 11](https://timesmachine.nytimes.com/timesmachine/1949/11/13/93550239.html?pageNumber=87)," _New York Times_, 13 November 1949, pp. 87.


[^nyt1960]:
	"[The Kind of Expert Our New Decade Needs](https://timesmachine.nytimes.com/timesmachine/1960/01/02/99282204.html?pageNumber=12)," _New York Times_, 2 January 1960, pp. 12. The article invokes "the Forties" as "the Atomic Decade," "the Fifties" as "[the] Lunik [decade]," and "the Sixties" as "the Decade of the Experts."


[^nyt1970]:
	"[Text of the Lindsay Inaugural Speech](https://www.nytimes.com/1970/01/01/archives/text-of-the-lindsay-inaugural-speech.html)," _New York Times_, 1 January 1970, pp. 15. The speech was delivered on 31 December 1969 opens with the statement that "[t]his is the last day of the decade."

[^nytrib1880]:
	"[Progress](https://www.newspapers.com/image/79198785/?terms=%22new%2Bdecade%22)," _New York Tribune_, 1 January 1880, pp. 4. "A new decade begins."

[^nytrib1890]:
	"[Plays of Ninety-One](https://www.newspapers.com/image/85504863/?terms=%22new%2Bdecade%22)," _New York Tribune_, 28 December 1890, pp. 19. The dek: "How the New Decade Will Begin at the Theatres."

[^bosglobe1889]:
	"[The Holiday Month](https://www.newspapers.com/image/430769476/?terms=%22new%2Bdecade%22)," _Boston Globe_, 1 December 1889, pp. 12. Mentions "the new decade that starts with 1890."

[^ctrib1921]:
	"[1921 Will Reward Fighters](https://www.newspapers.com/image/355137895/?terms=%22new%2Bdecade%22)," _Chicago Tribune_, 3 January 1921, pp. 34. "A new year, a new decade, a new epoch open before us."

[^ctrib1929]:
	"[When the Historians Meets to Name the Dying Decade](https://www.newspapers.com/image/349805303/?terms=decade)," _Chicago Tribune_, 29 December 1929, pp. 1. See the [embedded image](#fig:cartoonresponse) in this article.

[^ctrib1930]:
	"[The End of the Decade](https://www.newspapers.com/image/349171819/?terms=%22new%2Bdecade%22)," _Chicago Tribune_, 4 January 1930, pp. 10. A reader's frustrated rejection of the political cartoon published a week before. "Even your leading cartoonist appears to make this mistake. The year 1930 is the last of the third decade, and the fourth decade will not begin until Jan. 1, 1931." See the [embedded image](#fig:cartoonresponse) in this article.

[^nytrib1900]:
	"[The End of the Century](https://www.newspapers.com/image/206535133/?terms=%22new%2Bdecade%22)," _New York Tribune_, 23 December 1900, p. 16. Saved to pdf for posterity [here](/assets/img/decade/New_York_Tribune_Sun__Dec_23__1900.pdf). This article is dear to me because of its detail, clear language, and scholarly aspirations. The editor begins by praising the letter, which is "truly a comfort"; it's "plain, straightforward, candid, modest and honest." "If [the letter's author] could see the letters on this subject which have been received at this office in the last week, the most of them stupid and silly, some of them abusive and all of them except his anonymous, he would blush for his side of the case." Regarding the Cardinal approach to naming and counting decades: "But it is merely a loose and conversational mode of speech, like many another. It has no historic or mathematical significance, and has nothing to do with the question." Regarding the decade as a mere time span: "It must be borne of mind, however, that the word 'decade' means merely a period of ten years, regardless of when it begins or ends. The period from July 4, 1876, to July 4, 1886, is just as much a decade as any other period of ten years."

[^justspans]:
	In terms of the ISO 8601 standard, introduced later in this article, the decade as a mere span of ten years is a _[time interval](https://en.wikipedia.org/wiki/ISO_8601#Time_intervals) of duration ten years_. Above, Rielly gives two examples of such time intervals: `2008/2017` and `2009/2018`, both valid time intervals of year precision according to ISO 8601, and also expressible as `2008/P10Y` and `2019/P10Y` respectively. Or they could be ten-year time intervals at minute granularity, e.g., `2009-12-31T14:30/P10Y` as the decade beginning at 2:30 pm on 31 December 2009 and ending at 2:30 pm on 31 December 2019.

[^nashville1900]:
	"[Century Not Ended Says Flammarion](https://www.newspapers.com/image/604225670/)," _The Nashville American_, 4 January 1900. Headline and dek reproduced in third image [embedded above](#fig:generations). A reasonably authoritative account of the Ordinal position on centuries, from a French astronomer [Camille Flammarion](https://en.wikipedia.org/wiki/Camille_Flammarion), loaded with history and even literal French citations.