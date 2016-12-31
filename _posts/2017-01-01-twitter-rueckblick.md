---
layout: post
title: Ein kurzer Jahresrückblick via Twitter
published: true
featured_image: /images/2017-twitter/tweets_pro_stunde.png
---
Der Rest der Familie liegt dank Grippe krank im Bett, somit entfiel gestern die Silvesterfeier. Da ich mir eh schon länger anschauen wollte, was man mit den Twitter-Daten so alles machen kann, war rasch die Idee eines Jahresrückblicks via Twitter geboren.

Allerdings folgte recht bald eine Enttäuschung - Twitter erlaubt es nur die letzten 3.200 Tweets abzufragen. Somit fiel der Jahressrückblick etwas kurz aus. Als Newsquellen, die auch fleißig twittern, habe ich mit [@derStandardat](https://twitter.com/derStandard){:target="_blank"} und [@KURIERat](https://twitter.com/KURIERat){:target="_blank"} zwei österrichische Medien gewählt, die ungefähr gleich viel twittern. Beim Standard bin ich mit den 3.200 Tweets bis Ende Oktober zurückgekommen. Daher habe ich mich in der Analyse auf November und Dezember 2016 beschränkt. Dazu habe ich dann noch aus Deutschland [@SPIEGEL_Top](https://twitter.com/SPIEGEL_Top){:target="_blank"} mitaufgenommen und [@ArminWolf](https://twitter.com/ArminWolf){:target="_blank"} als *die* twitternde Privatperson in Österreich. Zeitpunkt der Datenabfrage war der 31.12.2016, gegen 22:30.

Die Analyse unten ist recht kurz und rudimentär, freue mich schon, wenn ich mal Zeit habe da tiefer zu gehen, z.B. Analyse der Hashtags und Followers.

## Wer twittert wie viel?

Schauen wir uns zuerst einmal die Anzahl der Followers an. Hier führt Armin Wolf, Spiegel Online Top und der Standard sind recht gleich auf, Kurier deutlich abgeschlagen. Es gibt übrigens auch das populärere Spiegel Online, ohne Top - hier wurde aber im Vergleich zu den anderen Quellen deutlich häufiger getwittert, sodass ein Vergleich nicht wirklich funktioniert hätte.

{: .center}
| **User**                 | **Followers** |
|:--------                 |------:|
| Armin Wolf               | 324k  |
| SPIEGEL ONLINE Top       | 281k  |
| derStandard.at           | 246k  |
| KURIER                   | 70k   |

Im betrachteten Zeitraum November und Dezember 2016 haben die einzelnen User rund zwei- bis dreitausend Mal getwittert, inkl. Retweets. In den folgenden Analysen ignoriere ich Tweets der Nachrichtenquellen, wenn es sich um Retweets handelt. Zusätzlich sieht man in der Tabelle, wie oft die Originaltweets der 4 User selbst reteeted wurden. Hier liegt Armin Wolf klar in Führung.

{: .center}
| **User**                 | **Tweets inkl. Retweets** |  &nbsp; **Tweets exkl. Retweets** | &nbsp; **Retweets dieser Tweets** |
|:--------                 |---------------:           | ------:                           |  ------:                          |
| derStandard.at           | 2.981                     | 2.957                             | 6.109                             |
| KURIER                   | 2.583                     | 2.520                             | 4.712                             |
| Armin Wolf               | 2.272                     | 1.961                             | 11.436                            |
| SPIEGEL ONLINE Top       | 1.791                     | 1.791                             | 3.839                             |

## Wann wird getwittert?

Wenn man sich anschaut, wann getittert wird, erkennt man zum Beispiel die Präsidentenwahl in den USA sehr gut. An den anderen Tagen ging es kaum vor 5 Uhr los.

![Tweets pro Tag](/images/2017-twitter/tweets_pro_tag.png)
{: .center}

Bezüglich besonders populärer Tweets, sprich Tweets mit einer hohen Anzahl an Retweets, sticht ein Tweet mit rund 1.300 Retweets heraus. Die meisten Tweets haben keinen Retweet.

![Retweets bis](/images/2017-twitter/retweets_hist_bis_50.png)
{: .center}

![Retweets ab 50](/images/2017-twitter/retweets_hist_ab_50.png)
{: .center}

Der Tweet mit den meisten Retweets ist der folgende von Armin Wolf:
<blockquote class="twitter-tweet" data-lang="en"><p lang="de" dir="ltr">Fidel Castros US-Präsidenten:<br>Eisenhower<br>Kennedy<br>Johnson<br>Nixon<br>Ford<br>Carter<br>Reagan<br>Bush sr.<br>Clinton<br>Bush jr.<br>Obama.<br>Trump war zu viel.</p>&mdash; Armin Wolf (@ArminWolf) <a href="https://twitter.com/ArminWolf/status/802434099990462464">November 26, 2016</a></blockquote>
<script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

## Wer twittert am meisten am Wochenende?

Wie zu erwarten, wird am Wochenende weniger getwittert. Armin Wolf twittert am Sonntag recht fleißig, macht dafür am Samstag am konsequentesten Pause. Dafür ist bei ihm der Mittwoch der klare Twitter-Favorit. Spiegel Online Top ist am Freitag, vor dem Start ins Wochenende, besoners eifrig.

![Tweets pro Wochentag](/images/2017-twitter/tweets_pro_wochentag.png)
{: .center}

Ein Blick auf die Uhrzeit der Tweets zeigt, dass man beim Kurier und beim Standard recht klare 'Arbeitszeiten' des Twitter-Accounts sieht. Beim Kurier von 5 bis 21 Uhr, beim Standard von 7 bis 23 Uhr. Armin Wolf's 'Twitter-Arbeitstag' beginnt noch später, dauert aber auch am längsten.

![Tweets pro Stunde](/images/2017-twitter/tweets_pro_stunde.png)
{: .center}


## Das IPython Notebook

{% include notebook-links.md notebook="2017-twitter/twitter.ipynb" %}
