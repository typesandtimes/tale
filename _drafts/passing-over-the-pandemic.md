---
layout: post-with-image
title: "Passing Over the Pandemic in the Hebrew Calendar"
excerpt: "In an Israeli Supreme Court case, the coronavirus presents an opportunity to revive an ancient practice and add a leap month for the sake of a healthy Passover holiday."
image:
  filename: "sanhedrin-calendar.jpg"
  alt:      "An 1883 illustration of the ancient Jewish Sanhedrin council, figuring out the calendar."
  caption:  "An 1883 illustration of the ancient Jewish Sanhedrin council, figuring out the calendar."
date: 2020-04-20
---

Happy [Passover](https://www.chabad.org/holidays/passover/pesach_cdo/aid/871715/jewish/What-Is-Passover-Pesach.htm)! _Chag Pesach samech!_ The Jewish holiday of emancipation lasted from April 8th to the 16th --- the 15th to the 22nd of Nissan in the Hebrew calendar.[^count] Unfortunately, the coronavirus pandemic presented some obstacles for Jewish people's Passover seders around the world. How exactly should one gather together with family and recall the emancipation of the Jewish people from slavery when so many would-be participants are under lockdown orders and separated from family?

Surely a great many Passover seders were held over the internet the past couple weeks. Indeed, Orthodox rabbis in Israel deemed the situation an emergency that required extreme measures --- [the use of Zoom](https://www.jpost.com/Israel-News/Raabis-approve-the-use-of-ZOOM-to-celebrate-passover-due-to-coronavirus-622221) and other video conferencing technology to carry out the sacred duty.

Last month one Israeli saw a potential solution to the problem of quarantine seders: just insert a leap month into the (Hebrew) calendar and thereby postpone Passover by a month when, hopefully, the lockdown has eased up a bit! _Deus ex machina!_

Yedidiah Efraim Meshulami [petitioned Israeli authorities](https://www.jewishpress.com/news/israel/religious-secular-in-israel-israel/jewish-farmer-suing-rabbis-declare-a-leap-year-to-save-our-passover/2020/03/20/) to declare the current Hebrew year, 5780, a _leap year_. In a leap year, instead of intercalating a leap day as we do in the Gregorian calendar, the Hebrew calendar intercalates _an entire leap month_, inserted just before the month of Nissan. The result of this leap year declaration, of this intercalation, would be the postponement of Passover by 30 days.

Due to "the severity of the situation in our country regarding individual freedom as well as public stability on issues of health, the economy, society, the courts, government and on and on," Meshulami argued, "pushing off the Nissan holidays would constitute 'first aid' for the Israeli society."

But what empowers the Israeli authorities to _alter the calendar_ at will? As justification for this calendrical power, Meshulami turned to the history books --- the _real ancient_ ones. In order to understand that _power_, however, we need a primer on the _mechanism_ of leap months in the Hebrew calendar.

{::comment}
court decision, march 22nd: https://versa.cardozo.yu.edu/opinions/meshulami-v-chief-rabbinate-israel
{:/comment}


# One Giant Leap

The Hebrew calendar, like other ancient calendars, is _lunisolar_: the months are lunar but the years are solar. To make these two constraints work, we need two distinct ways of _tweaking_ the years in the Hebrew calendar, two knobs to adjust.

* The first knob controls the durations of _months_ in terms of _days_. Each of the 12 months in the Hebrew calendar begins the day of the new moon --- which day exactly? we'll return to that point! --- and lasts the whole lunar cycle, about 29 and a half days. Because the lunar cycle doesn't match a whole number of days, we have to trade off month lengths by alternating, at first approximation, 29 days one month, 30 the next, 29 after that, and so on.

* The second knob controls the durations of _years_ in terms of _months_. As we know in the Gregorian calendar, a solar year is not equal to a whole number of days; it's more like 365 and a quarter. Thus the leap! In our calendar we insert a leap day every now and then, totaling 97 days every 400-year cycle. Likewise in the Hebrew calendar, we can't make a year --- which consists of a whole number of months, each consisting of a whole number of days --- evenly match a solar cycle. But instead of inserting _days_ we insert _a whole month_.[^adar]

Let's think of the calendar in terms of programming language compilers: we have a _specification_ of the Hebrew calendar --- the two lunisolar constraints it should adhere to --- and we wish to _implement_ the calendar --- to map the calendar's days, months, and years onto the days as we experience them (and also going backwards and forwards in time).

The lunisolar constraint forms the specification of the calendar, while the two knobs are like the


# From Empiricism to Algorithm


---

[^count]:
    In the Hebrew calendar, days begin at sundown. Passover officially began on the 15th of Nissan in that calendar and that day would be April 9th in the Gregorian calendar. Except Passover _really_ begins at sundown, when the 14th becomes the 15th, and that transition falls squarely on the evening of April 8th.

[^adar]:
    The leap month is called Adar, but there's already a month called Adar, so the leap month has the distinction of being Adar I and the real one is Adar II. Adar I is always 30 days and Adar II is always 29.

{::comment}


* Zoom: https://www.jpost.com/Israel-News/Raabis-approve-the-use-of-ZOOM-to-celebrate-passover-due-to-coronavirus-622221


* article that discusses the rise of computing in babylon: https://jewishweek.timesofisrael.com/ancient-jewish-computers/

* 161. The discussion of the court and the reasons for intercalation

* 172. "the calendar was no longer dependent on an empirical procedure, but rather on calculations;587 and that the calendar was no longer set by a rabbinic court, but rather by ‘those who made calculations’, i.e. experts in calendrical calculation."
  * in the Palestinian Talmud?
  * different for Alexandrian jews: "R. Ami assumed that the Jews of Alexandria had taken the lulav on the Sabbath on the first day of the festival on the strength of R. Abbahu's visit, who would have told them (p.174) the exact dates of the festival, as had been set by the rabbinic court in Palestine. R. Ami remarked that they could not rely on such visits every year.593"
  * categories:
    * palestinian jews: rabbinic court sets the months and festival dates
    * babylonian jews: two day festivals because we can't be sure when the rabbinic court set the dates
    * egyptian jews: calendar was determined independently (sec 3.2.1)
  * re the two days, sec 3.2.1:
    * "As we shall later see, the rabbinic concept of two Diaspora festival days was predicated on the assumption that Diaspora communities had to follow the calendar that was set by the Palestinian rabbinic court. Since they could not obtain the Palestinian dates in time for the festivals, two days had to be observed in doubt (see section 5.3.1). In practice, however, few communities are likely to have observed this custom. Diaspora communities, as we have already seen, were not dependent on the Palestinian rabbinic calendar; they reckoned their own calendar independently and in their own specific ways.399 In this context, Diaspora Jews had no reason to be ‘uncertain’ about the dates of festivals. To Jews such as Philo [Alexandrian, died 50 CE] or Josephus [Roman?, died 100 CE], the observance of two festival days would have been completely unnecessary."
    * "If Jewish communities such as in Alexandria were able to set their own calendar on the basis of their own sightings of the new moon, this would have led to tremendous calendrical diversity. As we have seen, visibility of the new moon would have varied considerably from place to place because of different geographical co‐ordinates, weather conditions, and human observational accuracy. As a result, different Jewish communities are likely to have observed the festivals at slightly different times. This would reinforce our conclusions of the previous chapter, that Jewish calendar reckoning in Antiquity was characterized by its diversity."


*  180. "The absence of any information in rabbinic sources from before the tenth or the
eleventh centuries regarding the institution of the fixed calendar casts considerable doubt on the historical reliability of the Hillel and other traditions. Not only is it uncertain who instituted the calendar, but also, I would suggest, whether such an institution was ever made at all. [...] The gradual nature of such a process would thus explain why the ‘institution’ of a fixed calendar is not mentioned at all in early rabbinic literature." [C&C, pp. 180-181]

* p. 185: mention of al-Khwarizmi!

* 188. the calendrical court

* 205. "The earliest datable reference to the present‐day molad calculation is in the work of the Muslim astronomer al‐Khwarizmi on the Jewish calendar, dating from 823/4 CE, where the lunation of 29 days, 12 hours, and 793 parts, is explicitly given.714 As stated above, all this indicates is that the present‐day lunation would have been known, if al‐Khwarizmi is to be believed, by the Jews in his period; but it does not necessarily prove that it was used for calendrical purposes in practice."

* 208. "More recent scholars have drawn attention to the fact—largely unnoticed by Bornstein and Jaffe—that the Babylonian astronomers employed exactly the same mean lunation as Ptolemy, centuries before Ptolemy composed his work.729 It is most likely, indeed, that Ptolemy's lunation was borrowed from Babylonian astronomy.730 This raises the possibility that the rabbinic calendar‐makers may have taken their lunation directly from the Babylonians, without resorting to Ptolemy's Almagest. If so, the rabbinic lunation could have been adopted long before the early ninth century.731"

* 211. "In the course of the Geonic period, rabbinic Judaism was to expand further afield to Egypt, North Africa, and southern and western Europe, and eventually to dominate the whole of world Jewry. Throughout this period of expansion, the question of solidarity, cohesion, and communitas between the various rabbinic communities became increasingly pressing. In this context, I shall argue, the calendar came to play a decisive role. The institution of a standard, fixed calendar was a significant contributor to the unity of the rabbinic community or—as the rabbis saw it—of the Jewish people."

== POWER of calendrical authority ==

* 228. "Because the intercalation was largely unpredictable, Tannaitic sources consider the possibility of a house being let for ‘one year’ without anyone knowing whether that year would last for 12 or 13 months.793 "
  * 229. "... Indeed, the Palestinian Talmud reports that R. Hoshaya used to warn the witnesses at Ein Tav (where the calendrical court was at one time located) as follows: ‘be aware of the weight of your testimony—how house rents will be affected by it’.801"

* 229. "Because it took a few days for people to find out whether the previous month had been of 29 or 30 days, witnesses could not be expected to know if the date of an incident was the 2nd or the 3rd of the month (M. Sanhedrin 5:3)"

* 230. "More importantly, the empirical calendar system was an effective way of imposing and maintaining rabbinic authority upon the Jewish community. In this respect, it would have been politically expedient for the rabbinic class to maintain the status quo, and to resist any change in the way the calendar was reckoned."

* 230. "The Mishnaic system had also intrinsic ideological value. By controlling the dates of the calendar from month to month, the rabbis perceived themselves as exerting control over the entire cosmos, and even over the Divine order. Thus we are told in a number of sources that God and his angelic court would not sit in judgement at the New Year (1 Tishre) until the rabbinic court had sanctified it and declared it the first day of the month.803"
 * "When all the ministering angels gather before the Holy One and ask Him, ‘Master of the universes, when does the New Year begin?’ He replies: ‘Are you asking Me? Let us, you and me, ask the court on earth.’"
   * cf Midrash Tehillim 81:6. "As a testimony for Jehoseph, He ordained it, when he went forth over the land of Egypt, [when] I understood a language that I had not known." https://www.chabad.org/library/bible_cdo/aid/16302/jewish/Chapter-81.htm

* "In spite of its functional disadvantages, this calendar was the basis of an entire ideology and world‐view. On the one hand, it meant that man—or more specifically, Israel, and more specifically still, the rabbinic court—was empowered over time and the cosmic order. On the other hand, it implied a concept of time that was flexible, man‐made, and in a sense, sacred. This ideology was not merely theoretical: it would have affected, in practice, the daily experience of time and of its flow.

"After the institution of a calculated calendar, this experience of time would have been radically redefined. Because the calendar was now governed by fixed, mathematical rules, time was eventually to be experienced as rigid, objective, and ‘desacralized’."

== Calendrical Unanimity vs Diversity ==

* 241, on calendrical unanimity. "The notion of calendrical unanimity is easy for us to take for granted. Nowadays, we are used to the fact that there is only one Jewish calendar all over world; in the secular domain, likewise, the Gregorian calendar has become lingua franca across the globe.
In the ancient world, by contrast, calendrical diversity—Jewish and non‐Jewish— was completely the norm.838 Since new months and inter‐calations were reckoned independently by various Jewish communities, festivals could often be observed on totally different dates. This situation would not have been perceived as divisive or schismatic. There is no suggestion, in any of the Jewish non‐ rabbinic sources we have examined in Chs. 2–3, that calendrical diversity was regarded by the Jews as ‘problematic’. Everyone was aware that a calendar based on empirical data, such as sightings of the new moon, was bound to differ from one locality to the next. If one community observed Passover one month later than the others, this was not necessarily perceived as an expression of sectarianism, disagreement, or rift.839"

* 242. "Not so, however, in rabbinic Judaism, where the assumption was that new moons and festivals should be observed by everyone on the same dates. This assumption is not explicit in rabbinic sources, nor is it clearly substantiated or justified. But it is implicit in the rules that inter‐calations can only be made in Judaea or in Galilee,840 only by a single, appointed rabbinic court,841 and only with the approval of the Patriarch.842 The setting of the new months, likewise, is assumed to be the prerogative of a single rabbinic court.843 This implies that the same calendar must be followed by all Jews. "

* 244-245. Anecdote about calendar info not reaching Egyptian Jews: "But no envoys are known to have been sent to Egypt, even though it was closer to Palestine than Babylonia and Asia, and comprised among the largest Jewish communities in this period.
A number of rabbinic sources confirm that calendrical information was never sent to Egypt, in spite of its considerable Jewish population;854 this point is also noted by Maimonides (Sanctification of the New Month, 5:10). Most revealing is Y. Eruvin 3:9 (21c), which has already been cited and discussed in section 4.2.3 When R. Abbahu visited Alexandria during the festival of Tabernacles, he apparently informed the Alexandrians of the ‘correct’ date of the festival. R. Ami (p.245) heard about this and exclaimed: ‘who will bring them R. Abbahu every year?’, which clearly implies that calendrical information was not normally sent to the Jews of Egypt.855"

* 256. "The shift to a fixed calendar was more radical than any other change, such as the institution of fixed rules, that had preceded. But it did not represent a fundamental change of direction or policy. As I have argued in Ch. 4, the transition from empirical calendar to calculated system may have been quite gradual. Ever‐multiplying calendrical rules, including eventually the alternation of full and defective months from Adar to Tishre, may have simply overrun the old Mishnaic system. This would have brought the empirical observation of the moon to an effective end, and ushered in a fixed calendar that was eventually to be based entirely on the calculation of the mean conjunction. The fixed calendar was thus the culmination of a process, in which the Mishnaic calendar was gradually adapted to enable Diaspora communities to predict and follow the same calendar as in the Land of Israel."

* 256. "As soon as the rabbinic community of Babylonia began to grow and expand, at the beginning of the Amoraic period, the problem of rabbinic solidarity and, more precisely, of Babylonian rabbinic loyalty to its Palestinian motherland, needed urgently to be addressed. The earlier episode of Ḥananiah nephew of R. Yehoshua—if indeed historical—could not be allowed to be repeated. What was at stake, besides political considerations, was the very cohesion of rabbinic Judaism; and this, it was felt, depended largely on homogeneity of calendrical observance."

* 263. "The purpose of adopting a fixed calendar in the fourth century was, as I have
suggested, to secure Babylonian loyalty by enabling Babylonians, or anyone elsewhere, to observe the same calendar as in Palestine. But this policy turned out to be a double‐edged sword. For the fixed calendar had the inevitable effect, at the same time, of increasing Babylonia's autonomy, and hence, of diminishing its dependence on the Palestinian court."



* petition decision:
  * https://versa.cardozo.yu.edu/opinions/meshulami-v-chief-rabbinate-israel
  * https://versa.cardozo.yu.edu/sites/default/files/upload/opinions/Meshulami%20v.%20Chief%20Rabbinate%20of%20Israel.pdf
* article: https://www.jewishpress.com/news/israel/religious-secular-in-israel-israel/jewish-farmer-suing-rabbis-declare-a-leap-year-to-save-our-passover/2020/03/20/
* another: https://www.breakingisraelnews.com/147365/man-petitions-high-court-to-delay-passover-by-month-due-to-coronavirus/
* quote from judgment about importance of calendar unanimty: "In addition to the lack of authority, it is also worth noting in this regard the words of the author of the Lekakh Tov midrash (Tuvia ben Eliezer, 11th cent.) on Parashat Hohodesh [the additional Scriptural reading for the Sabbath before the beginning of the month of Nissan – ed.], according to which “it is proper to rely upon the rules for intercalating the year, so as not to divide Israel into sects such that one violates the holy day of the other”"

* sanhedrin: https://www.toseftaonline.org/seforim/tractate_sanhedrin_mishna_and_tosefta_1919.pdf
  * alt? https://www.sacred-texts.com/jud/tsa/tsa03.htm
  * 32: "And to our brethren, the exiles of Babylon, and those in exile in Media, and all the other Israelites in exile, 'May your peace be increased! We make known to you that the pigeons are still tender and the lambs thin, and that the season of spring is not yet come. It seems fitting to me and to my colleagues that we add to this year thirty days.'"
  * just after that, explanation that it must be intercalated on or before 16 days before Passover ... later, it can be done throughout month of Adar
  * "And was not that year fitted to be intercalated? And why did not Elisha
intercalate it? Because it was a year of famine, and all the people were running to the threshing floors."
  * "but they may intercalate because of real cases of need"
    * footnote: B. II a reads "paths" i.e. when they are impassable for those
coming from a distance to celebrate the Passover at Jerusalem and also adds "bridges."
  * pic: https://en.wikipedia.org/wiki/Sanhedrin#/media/File:Sanhedrin1.jpg

* example from talmud explaining confusion about not knowing whether the next day is the beginning of a new month, especially right before rosh hashana: https://www.sefaria.org/English_Explanation_of_Mishnah_Eruvin.3.7?lang=bi


* talmud beitzah 4b, talking about the second day feast in diaspora: https://www.sefaria.org/Beitzah.4b.7?lang=bi&with=all&lang2=en
  * "In earlier generations, they observed the second day of the Diaspora because they were unaware when the court sanctified the New Moon to mark the beginning of the month. Today, that determination is accomplished by means of calculations known to all, and the second day is observed as the custom of our fathers, not due to any uncertainty."
  * "Rav Asi was uncertain whether the Sages’ ordinance that the second day is to be observed as a Festival was a fixed ordinance that applies even when the calculations determining the New Moon are known to all; or whether the ordinance was based strictly on the uncertainty stemming from their lack of awareness."
  * "Rabbi Zeira said: It is reasonable to say in accordance with the opinion of Rav Asi that the Sages considered the two days as one and it is not a practice instituted due to uncertainty, as today we know the determination of the first day of the new month based on a fixed calendar and the precise dates of the Festivals are known by all, and nevertheless we observe the two Festival days of the Diaspora."
  * Samaritans fuck up the protocol: "Abaye said: On the contrary, It is reasonable to say in accordance with the opinion of Rav that the second day is observed as a Festival due to uncertainty, as we learned in a mishna (Rosh HaShana 22b): Initially, after the court sanctified the new month, they would light torches on the mountain tops, from one peak to another, to signal that the New Moon had been sanctified. After the Samaritans [Kutim] disrupted this method by lighting torches at the wrong times, the Sages instituted that messengers should depart to inform the people of the start of the month. Since the messengers could not reach all Diaspora communities before the beginning of the Festival, the Sages instituted that an additional Festival day should be observed there, due to the resultant uncertainty with regard to which day was the actual Festival day."
  * "Abaye continues his argument: And this indicates that if the Samaritans had desisted from their interference, the Sages would have restored the earlier custom and we would observe only one day. And, similarly, in a place where the messengers arrived from Jerusalem on time, we observe only one Festival day."
  * "The Gemara asks: And now that we know the determination of the first day of the new month, what is the reason that we observe two Festival days in the Diaspora? Because they sent a warning from there, from Eretz Yisrael: Although now there is a fixed calendar and there is no uncertainty, be careful to observe the custom of your fathers that you received, because at times the monarchy will issue decrees of persecution restricting Torah study and the fixed calendar may be forgotten. And the people will come to have their proper observance of the Festivals be disrupted again. However, the fundamental halakha is that the observance of two Festival days is based on uncertainty."


 * "A Short History of the Jewish Fixed Calendar: The Origin of the Molad" by Ajdler - http://www.ajdler.com/jjajdler/fichiers/Substitution/Vol20Ajdler%20-%20Copy.pdf



 * Ajdler, "The Future of the Jewish Calendar"
   * 36. "It was important to find a theoretical justification that could be acceptable to all streams of Judaism, even the most conservative. It is clear that the implementation of any slight improvement of the Jewish calendar requires the existence of a central and authoritative rabbinical council. The Jewish people cannot afford a new schism. Hopefully, in the not too distant future, we will see the emergence of an authoritative and respected chief rabbinate, independent of the political streams, in accordance with the hopes raised by the first chief rabbis of Israel."



   * sources on gregorian calendar!
		- Gordon Moyer, “The Gregorian calendar,” Scientific American (1982).
		- J.Denoyelle,“Les400ansdelaréformegrégorienne,”Cieletterre,98(1982),pp.271-
		82.
		- NoelSwerdlow,“TheOriginoftheGregorianCivilCalendar,”TheJournalfortheHistory
		of Astronomy (1974), pp. 48-49.

{:/comment}
