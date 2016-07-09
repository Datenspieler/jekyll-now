---
layout: post
title: "Wie hat sich das Cover vom Magazin Spiegel verändert?"
published: true
featured_image: /images/2016-spiegel/featured_image.jpg
---

Die Idee zu dieser Analyse stammt von einem [Artikel](http://www.pyimagesearch.com/2015/10/19/analyzing-91-years-of-time-magazine-covers-for-visual-trends/){:target="_blank"}, in dem die Cover des Time Magazine analysiert werden. Um das wirklich zu verstehen und etwas dazuzulernen, wollte ich etwas Ähnliches für ein deutschsprachiges Magazine machen. Dafür hat sich der [Spiegel](https://www.spiegel.de){:target="_blank"} angeboten, da es dort Covers aus mehr als 60 Jahren [gibt](http://www.spiegel.de/spiegel/print/index-1947.html){:target="_blank"}. Das Copyright an den Coverbildern liegt somit natürlich beim Spiegel.

## Das IPython Notebook

{% include notebook-links.md notebook="2016-spiegel/Covers.ipynb" %}

## Wie hat sich das Cover vom Spiegel entwickelt?

Hier ein Überblick über die Entwicklung des Covers in Zehnjahres-Schritten.

![Galerie](/images/2016-spiegel/galerie.jpg)
{: .center}

Nun wollen wir uns die Entwicklung etwas genauer anschauen. Die ersten drei Jahre, 1947, 1948 und 1949 hat sich das Cover vom Spiegel kaum verändert. Das Bild unten zeigt die Cover dieser drei Jahre übereinandergelegt und jeweils den durchschnittlichen Wert angezeigt.


![1947_1948_1949](/images/2016-spiegel/avg-1947_1948_1949.jpg)
{: .center}

In den Jahren 1950 bis 1954 ist der Text "DER SPIEGEL" nach links gewandert. Zusätzlich erkennt man ein "Durchschnittsgesicht". Somit wird klar, dass in diesen Jahren wohl fast immer ein Kopf in ziemlich ähnlicher Perspektive abgebildet war.

![1950_1951_1952_1953_1954](/images/2016-spiegel/avg-1950_1951_1952_1953_1954.jpg)
{: .center}

In den darauffolgenden 5 Jahren ist der Titel einzeilig geworden.

![1955_1956_1957_1958_1959](/images/2016-spiegel/avg-1955_1956_1957_1558_1959.jpg)
{: .center}

In den Jahren 1960 bis 1964 hat sich die Schriftart leicht geändert und der weiße Balken am unteren Rand des Titelbildes ist verschwunden. Zusätzlich wird das "Durchschnittsgesicht" weniger deutlich - das bedeutet, es kommen auch Covers, die kein Gesicht zeigen.

![1960_1961_1962_1963_1964](/images/2016-spiegel/avg-1960_1961_1962_1963_1964.jpg)
{: .center}

In den nächsten 5 Jahren (1965 - 1969) verschwindet das "Durchschnittsgesicht" fast ganz.

![1965_1966_1967_1968_1969](/images/2016-spiegel/avg-1965_1966_1967_1968_1969.jpg)
{: .center}

In den darauffolgenden 70er Jahren ändert sich lediglich die Schriftart leicht.

![1970_1971_1972_1973_1974_1975_1976_1977_1978_1979](/images/2016-spiegel/avg-1970_1971_1972_1973_1974_1975_1976_1977_1978_1979.jpg)
{: .center}

Und auch in den 80ern und 90ern gibt es keine merkbaren Änderungen.

![1980_1981_1982_1983_1984_1985_1986_1987_1988_1989_1990_1991_1992_1993_1994_1995_1996_1997_1998_1999](/images/2016-spiegel/avg-1980_1981_1982_1983_1984_1985_1986_1987_1988_1989_1990_1991_1992_1993_1994_1995_1996_1997_1998_1999.jpg)
{: .center}

Mit dem Millennium bekommt das Cover einen etwas anderen Farbton und die Position des Titels und des Rahmens scheint sich zu wandeln (in den Jahren 2000 bis 2016) der Jahre 2000 - 2016. Das kann natürlich auch einfach an den Bildern liegen, nicht am tatsächlichen Cover. Rechts oben sieht man nun recht deutlich einen Strichcode, der im vorigen Bild schon leicht wahrzunehmen war - genau genommen wurde der Strichcode rechts oben im Jahr 1993 eingeführt.

![2000_2001_2002_2003_2004_2005_2006_2007_2008_2009_2010_2011_2012_2013_2014_2015_2016](/images/2016-spiegel/avg-2000_2001_2002_2003_2004_2005_2006_2007_2008_2009_2010_2011_2012_2013_2014_2015_2016.jpg)
{: .center}

## Ein großes Poster mit allen Covers

Statt übereinander kann man die Covers natürlich auch einfach nebeneinander zusammenfügen. Im zugehörigen Notebook sind das nicht mal 20 Zeilen Code. Das Bild unten zeigt die Cover pro Jahr (Zeile) und Woche (Spalte). Das Bild ist recht groß, ein Klick auf das Bild unten, öffnet das Bild in einem extra Fenster, in dem man es dann leicht in voller Größe sehen kann.

[
![Poster](/images/2016-spiegel/strip.jpg)
](/images/2016-spiegel/strip.jpg){:target="_blank"}
{: .center}

## Bewegte Bilder

Natürlich können die Bilder mit wenigen Befehlen, siehe zugehöriges Notebook, auch zu einer Animation zusammengefügt werden. Damit die Animation nicht zu lange dauert, habe ich pro Jahr nur das erste Bild genommen, das kann natürlich leicht angepasst werden. Zusätzlich wird das jeweilige Datum des Covers am unteren Rand angegeben. (In älteren Browsern wird die Animation nicht automatisch unten angezeigt - in dem Fall kann die Datei über den Link unten heruntergeladen und dann angeschaut werden.)

[
![Animation](/images/2016-spiegel/animated.gif)
](/images/2016-spiegel/animated.gif){:target="_blank"}
{: .center}
