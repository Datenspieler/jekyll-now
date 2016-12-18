---
layout: post
title: "Gewinnt meine Tochter oder der Rabe?"
published: true
featured_image: /images/2016-obstgarten/featured_image.jpg
---
Ich habe eine kleine Tochter, die mit Begeisterung das Spiel Obstgarten von HABA spielt. Das Ergbenis ist entweder große Freude, wenn das Obst schnell genug geerntet wird, oder auch Tränen, wenn der böse Rabe gewinnt. Als besorgter Vater habe ich mich gefragt, wie wahrscheinlich es ist, dass das Kind nach dem Spiel glücklich ist.

## Das Spiel Obstgarten

Von [HABA](https://www.haba.de) gibt es das tolle Spiel [Obstgarten](https://www.haba.de/de_DE/spielzeug/obstgarten/p/1000017). [![Bild Spiel Obstgarten, (C) Haba](/images/2016-obstgarten/obstgarten.jpg "Copyright HABA")](https://www.haba.de/de_DE/spielzeug/obstgarten/p/1000017) Dabei versucht man gemeinsam Obst von Bäumen zu ernten, und das schneller als der böse Rabe. Konkreter -- die Spielanleitung findet man [hier](http://www.haba.de/medias/sys_master/hcd/hdb/8802231812126.pdf) -- gibt es vier Obstbäume (Apfel, Birne, Kirsche, Zwetschke) mit je zehn Früchten. Zeigt der Würfel eine der vier Obstsorten, wird eine Frucht vom entsprechenden Baum geerntet, vorausgesetzt es hängen noch Früchte am Baum. Aber wehe, es wird der Rabe gewürfelt. Dann wird Schritt für Schritt ein Rabe zusammengepuzzelt. Insgesamt sind es neun Puzzleteile, die den Raben ergeben.

Auf den ersten Blick sieht es also schlecht aus für die Spieler -- 4 x 10 Früchte versus nur 9 Rabenteile. Aber zum Glück gibt es noch die sechste Würfelseite, ein Korb. Wird der gewürfelt, darf man zwei beliebige Früchte ernten. Aber reicht das, damit die spielenden Kinder, oder auch die Erwachsenen, eine gute Chance haben, als Sieger aus dem Spiel hervorzugehen?

Pro Wurf werden im Durchschnitt 4 x 1/6 (ein Obst wird gewürfelt) + 2 x 1/6 (Korb wird gewürfelt) = 1 Obst entfernt und 1/6 Rabenteil aufgelegt. Somit hätte man im Durchschnitt also nach 40 Würfen die 40 Früchte geerntet und gleichzeitig 40/6 = 6.7 < 9 Rabenteile aufgelegt. Sieht also gut aus.

Aber halt, hier hat sich ein Denkfehler eingeschlichen. Je länger das Spiel dauert, sprich je mehr Früchte geerntet sind, umso schwieriger wird es, weitere zu ernten. Sind zum Beispiel schon alle Äpfel geerntet, nützt ein gewürfelter Apfel nichts. So leicht, ist es also doch nicht.

Was tun? Warum nicht den Computer fragen?

## Computersimulation

Ich habe ein IPython Notebook erstellt, in dem die einzelnen Komponenten der Simulation Schritt für Schritt aufgebaut werden. Der komplizierteste Teil ist die Würfelseite Korb. Hier ist nämlich die einzige Stelle im Spiel, in dem der Spieler eine Entscheidung treffen muss, welche zwei Früchte er ernten möchte.

Die offensichtlichste Strategie ist es, diejenigen Früchte zu ernten, von denen es noch am meisten gibt. Wenn man kurz darüber nachdenkt, erkennt man, dass das auch die optimale Strategie ist, unter der Annahme, dass der Würfel fair ist, sprich alle 6 Seiten gleich häufig auftreten. Dann ist nämlich zu erwarten, dass bei den kommenden Würfen im Durchschnitt die Früchte gleich oft gewürfelt werden. Ich nenne diese Strategie im folgenden *max*.

Praktische Erfahrung zeigt, dass meine Tochter oft eine andere Strategie verfolgt, und genau die Früchte erntet, von denen es nur mehr wenige gibt. Hier scheint der Wunsch doch noch einen Apfel zu erntet im Vordergrund zu stehen. Diese Strategie ist leider, wenn man vor dem Raben die Früchte ernten will, die schlechteste, deshalb *min* im weiteren genannt. Als dritte Strategie habe ich noch die Zufallsstrategie *rnd* implementiert, hier wird rein zufällig eine Obstsorte ausgewählt.

## Das IPython Notebook

{% include notebook-links.md notebook="2016-obstgarten/Haba-Obstgarten.ipynb" %}

## Ergebnisse

Die wichtigste Frage ist natürlich, wie wahrscheinlich gewinnen die Spieler gegen den Raben.
![Gewinnwahrscheinlichkeit](/images/2016-obstgarten/01_gewinnwahrscheinlichkeit.svg) Wie man sieht, hängt das deutlich von der Strategie ab. Wenn man die optimale Strategie *max* wählt, gewinnt man mit rund 69%. Wählt man hingehgen die schlechteste Strategie *min*, gewinnt man nur mit rund 53%. Die Zufallsstrategie liegt wie erwartet dazwischen.

Die nächste Frage, wie viele Runden spielt man.
![Anzahl gespielter Runden](/images/2016-obstgarten/02_gespielte_runden.svg)
Auch das hängt von der Strategie ab, zwischen rund 40 und 44 Runden. Wenn man eine schlechtere Strategie wählt, spielt man länger.

Interessant auch, wenn man unterscheidet, wie das Spiel ausgeht. Hier sieht man, dass die gewonnenen Spiele im Schnitt etwas länger dauern. Für die Strategie *max* spielt man zum Beispiel nur 37 Runden, wenn der Rabe gewinnt, gegenüber 41 Runden, wenn die Spieler gewinnen.
![](/images/2016-obstgarten/03_gespielte_runden_je_ergebnis.svg)

Wie sehr muss man zittern, wenn man gewinnt, sprich wird es knapp, sind zum Beispiel schon 8 Rabenteile ausgelegt? Wenn man mit der Strategie *max* gewinnt, ist es am wahrscheinlichsten, dass 6 Rabenteile ausgelegt sind.
![Details Ergebnis](/images/2016-obstgarten/04_verteilung_punkte_strategie_max.svg)
Die Zahlen auf der horizontalen Achse sind wie folgt zu verstehen: eine positive Zahl gibt an, wieviele Rabenteile noch fehlen, bis der Rabe fertig ist. 4 bedeutet also, dass noch 4 Rabenteile fehlen und folglich 5 Teile ausgelegt sind. Eine negative Zahl gibt an, wieviele Früchte noch zu ernten sind.

Hier noch die Details der Ergebnisse je Strategie.
![Details Ergebnis pro Strategie](/images/2016-obstgarten/05_verteilung_punkte_je_strategie.svg)
