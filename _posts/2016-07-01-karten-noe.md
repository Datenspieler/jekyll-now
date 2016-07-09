---
layout: post
title: Wo in Niederösterreich findet man als Mann am ehesten eine Frau?
published: true
featured_image: /images/2016-karten-noe/featured_image.jpg
---
Eine Google-Suche zu *Open Data Austria* hat mich unlängst zu [www.data.gv.at](https://www.data.gv.at){:target="_blank"} gebracht. Die Auswahl an Daten ist zwar nicht gerade umwerfend, man fragt sich z. B. warum es oft Daten pro Bundesland gibt, aber nicht gesamthaft für Österreich -- Statistik Austria scheint nicht vertreten zu sein. Ich fand dann aber doch interessante [Daten](https://www.data.gv.at/katalog/dataset/land-noe-bevolkerung-nach-alter-und-geschlecht){:target="_blank"} zur Bevölkerung in meinem Heimatbundesland Niederösterreich. Da ich sowieso schon seit einiger Zeit mit Landkarten und Darstellung von Daten in Landkarten herumspielen wollte, war das ein perfekter Startpunkt.

Unter Python lässt sich das mit [folium](https://github.com/python-visualization/folium){:target="_blank"} recht einfach bewerkstelligen. Wichtig ist nur noch eine sogenannte GeoJSON Datei, die die Information enthält, welche Gemeinde wo auf der Landkarte ist. So eine Datei gibt es zum Beispiel vom Institut für Strategieanalysen im Zusammenhang mit Wahlanalysen [hier](http://www.strategieanalysen.at/wahlen/geojson/){:target="_blank"}.

## Das IPython Notebook

{% include notebook-links.md notebook="2016-karten-noe/Karten-NOE.ipynb" %}

## Wo leben die meisten Menschen, die meisten Frauen im Verhältnis zu Männer, die Jüngsten, ...?

Zum Einstieg mal eine leichte Frage: In welchem Bezirk wohnen die meisten Menschen? Wie man unten sieht, ist Baden mit rund 140.000 Einwohnern der bevölkerungsreichste Bezirk.
Einwohner pro Bezirk. Das besondere ist, dass hier eigentlich kein statisches Bild erstellt wird, sondern eine interaktive Karte, wie es zum Beispiel von Google Maps bekannt ist. Sprich man kann zoomen und herumfahren. Unter jedem Bild gibt es einen Link, mit dem man die entsprechende interaktive Landkarte in einem eigenen Fenster öffnet.

![Einwohner pro Bezirk](/images/2016-karten-noe/01.png)
[Interaktive Karte](/images/2016-karten-noe/01.html){:target="_blank"}
{: .center}

Die nächste Frage, die man mit den verfügbaren Daten beantworten kann, wo kommen auf 100 Männer die wenigsten, wo die meisten Frauen, bzw. wie viele sind das? Die Tabelle unten zeigt zum Beispiel, dass im Bezirk Mödling auf 100 Männer 108 Frauen kommen.

{: .center}
| **Bezirk**                 | **Frauen** |
|:--------                   |-------:|
| Zwettl                     | 99.5   |
| Scheibbs                   | 100.2  |
| ...                        | ...    |
| Krems a. d. Donau          | 106.2  |
| Mödling                    | 108.1  |

Die Karte zeigt, dass der Frauenanteil um Wien herum beziehungsweise in und um die größeren Städte wie St. Pölten oder Wiener Neustadt am höchsten ist.

![Männer - Frauen](/images/2016-karten-noe/02.png)
[Interaktive Karte](/images/2016-karten-noe/02.html){:target="_blank"}
{: .center}

Nachdem wir nun die Bezirke mit dem höchsten Frauenanteil gefunden haben, schauen wir nun auf das Durchschnittsalter. Hier zeigt die Karte unten, dass in den nördlichen Grenzregionen das Durchschnittsalter mit rund 50 Jahren am höchsten ist. Im Gegensatz dazu ist im Westen das Durchschnittsalter mit rund 38 Jahren am niedrigsten.

![Durchschnittliches Alter](/images/2016-karten-noe/03.png)
[Interaktive Karte](/images/2016-karten-noe/03.html){:target="_blank"}
{: .center}

Wenn man statt des Durchschnittsalter auf den Anteil an Kindern (< 10 Jahre) schaut zeigt sich ein ähnliches Bild, diesmal auf Bezirksebene. Achtung, gelb bedeutet jetzt ein geringer Anteil an Kindern, somit tendenziell ein höheres Durchschnittsalter, was oben durch rot dargestellt wurde.

![Kinder](/images/2016-karten-noe/04.png)
[Interaktive Karte](/images/2016-karten-noe/04.html){:target="_blank"}
{: .center}

Als letztes nun ein Blick auf das Wachstum pro Gemeinde. Die Karte unten zeigt die prozentuelle Änderung der Bevölkerung zwischen 2012 und 2015. Die Farben gehen von dunkelrot (starker Rückgang) über weiß nach dunkelgrün (starkes Wachstum). Wie man sieht, kann man unterschiedliche Kartentypen als Hintergrund auswählen. Ähnlich wie beim Durchschnittsalter, sieht man nun ein Schrumpfen bei den nördlichen Grenzregionen und im Süden. Um Wien herum und östlich beziehungsweise westlich davon, sieht man ein Wachstum.

![Wachstum](/images/2016-karten-noe/05.png)
[Interaktive Karte](/images/2016-karten-noe/05.html){:target="_blank"}
{: .center}

<!---
<div class="video-container">
   <iframe src="/notebooks/2016-karten-noe/01.html" frameborder="0"> </iframe>
</div>
--->
