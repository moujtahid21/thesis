# Featureentwicklung in Web Browsern - eine Analyse aktueller Browser im Bezug auf die Umsetzungsvorgehen der Web Spezifikationen

## Problemfeld und Kontext

Webentwicklung ist ein sehr schnellebiges und dynamisches Entwicklungsfeld, dass gerade in den letzten Jahren durch neue Features wie die sogenannten "Fugu"-APIs oder die Einführung von Progressive Web Apps (PWAs) sich stark gewandelt hat, wie sich auch in der Übersicht der [zuletzt abgeschlossenen Proposals im ECMAScript Standard zeigt][ecmascript-finished-proposals]. Leider ist allerdings die Unterstützung der Features in gerade den großen Browser Engines Blink, WebKit und Gecko weder einheitlich, noch vollständig ([caniuse-major-browser-support]) und selbst eingeführte oder getestete Features finden unter Umständen keine weite verbreitung oder langfristigen Support ([custom-elements-v0], [jpegxl]).
Als WebentwicklerIn gibt dies das Problem auf, dass man sich nicht darauf verlassen kann, dass nur weil etwas standardisiert ist, man es nutzen kann. Sollte man mit potentiell neuen Technologien explorativ arbeiten wollen, so ist es zudem interessant welche Browser bestimmte Features tendenziell zuerst unterstützen und bei welchen der Support neuer (möglicherweise noch nicht endgültig spezifizierter) Features am besten ist ("besten" kann hier unter mehreren Gesichtspunkten bewertet werden, wie zum Beispiel Stabilität, Umsetzungsgeschwindigkeit, Performance, ...).

## Ziel

Das Ziel dieser Arbeit soll sein analytisch die Umsetzung neuer Features in den drei großen Browserengines Blink, Gecko und WebKit basierend auf historischen Daten zu betrachten und hierbei herauszuarbeiten ob es basierend auf der Art der Features Auffälligkeiten gibt und welche Herangehensweise die Hersteller bei der Umsetzung neuer Spezifikationen verfolgen.

## Aufgabenstellung

Anhand des Kontexts, der Problemstellung und der Zielsetzung steht die Arbeit unter folgenden Kernfragen:

1. Welcher Browser ist allgemein am nächsten an einer vollständigen, korrekten Umsetzung des Standards?
2. Gibt es bei Frage 1. Abweichung je nach "Bereich" eines Features?

Um diese Fragen beantworten zu können sind folgende Zusatzfragen ebenfalls zu betrachten:

3. Wie schnell nach Standardisierung werden Features in einem/allen Browser(n) umgesetzt?
4. Wie stabil sind Vorabumsetzungen von Standards in einem/allen Browser(n)?
5. Welche Möglichkeiten werden von den Herstellern ergriffen um auf inkompatible Standardänderungen während des Standardisierungsprozesses zu reagieren?
6. Wie funktionieren die Standardisierungsprozesse?
7. Ist es möglich als außenstehender die Standardisierung eines Features zu beeinflussen?
8. Wie lassen sich Features sinnvoll in "Bereiche" unterteilen und gibt es solche Unterteilungen bereits?

## Lösungansätze und Ressourcen

Um die in der Aufgabenstellung beschriebenen Fragen zu beantworten ist es nötig eine Reihe an Datenquellen heranzuziehen.

Glücklicherweise existieren bereits einige sehr umfassende Datenquellen mit historischem Browsersupport für jedes Feature wie [wpt.fyi], [caniuse] oder [mdn-browser-compat-data]. Diese Quellen können herangezogen und verglichen werden um eine gegenseitige Validierung zu erreichen und potentielle Lücken zu füllen.

Gleichzeitig ist es möglich die Veröffentlichungen der Standards mit zum Beispiel GitHub Repositories heranzuziehen um nachzuvollziehen wann Features standardisiert wurden und wie sie sich entwickelt haben.

Gerade anhand der Browsersupport Daten sollte es möglich sein diese in eine Datenbank (z.B. SQLite) zu überführen, auf welche man Abfragen ausführen kann um die Fragen aus der Aufgabenstellung zu beantworten.

## Chancen und Risiken

Wie zuvor erwähnt halten die mehreren, unabhängigen Quellen die Chance bereit die Quellen gegeneinander zu validieren, dies birgt jedoch auch das Risiko die Daten in ein einheitliches Format bringen zu müssen.
Zudem können gerade die Daten aus den Standardrepositories schwer verarbeitbar sein, da diese noch nicht für eine solche Aufarbeitung gedacht sind. Hier besteht jedoch nach Titel und Kern der Arbeit die Möglichkeit, diese Frage in den Hintergrund zu rücken.

## Motivation

Der Autor hat als Webentwickler eine intrinsische Motivation den hier aufgeführten Forschungsfragen nachzugehen, da er selbst regelmäßig in der Entwicklung auf Features stößt, die entweder trotz Standardisierung nicht in allen Browsern unterstützt werden, oder noch während des Standardisierungsprozess ausprobiert werden sollen.
Zudem haben auch alle Browserhersteller eine Problematik der Interoperabilität erkannt und haben seit einigen Jahren das [Interop] Projekt ins Leben gerufen. Diese Arbeit kann dazu beitragen hier ebenfalls einen tieferen Einblick zu erhalten.

## Durchführungskontext und zeitliche Planung

### Setup

Die Arbeit soll ohne eine Beteiligung von außerhalb der TH Köln durchgeführt werden.

### Abhängigkeiten

Das Projekt ist lediglich von den in "Lösungsansätze und Ressourcen" genannten Quellen als Datenbasis abhängig.

### Meilensteine und Zeitrahmen

Basierend auf den voranstehenden Kapiteln lassen sich folgende Meilensteine benennen:

* Sammlung von Datenquellen zur Browserkompatibilität
* Definition von Featurebereichen
* Erstellung eines Datenmodells für Kompatibilitätsdaten
* Normalisierung der Datenquellen und Einpflegen der Daten in eine Datenbank nach Datenmodell
* Ausarbeitung von möglichen Abfragen zur Beantwortung der Forschungsfragen
* Vergleichende Analyse der Abfrageergebnisse nach Featurebereich und Browserengine
* Begleitende Recherche zu Standardisierungsprozessen und Browservorgehen abschließen
* Ergebnisse dokumentieren

Basierend auf Umfang und möglicher Zeitaufwändung sollte das Projekt in 7-9 Wochen umsetzbar sein.

## Arbeitsergebnis

Das angestrebte Arbeitsergebnis ist vor allem die abgegebene Arbeit in der die oben aufgeführte Zielsetzung erreicht wird und die gestellten Forschungsfragen beantwortet werden. Zudem sollen die Prozesse beschrieben werden, wie die Forschungsfragen bearbeitet wurden.
Zudem gehören zum Arbeitsergebnis der Arbeit alle möglicherweise erstellte Software inklusive ihrer Dokumentation als Git Repository und eine Kopie der Datenbank, welche zur Analyse genutzt wurde.

[ecmascript-finished-proposals]: https://github.com/tc39/proposals/blob/main/finished-proposals.md
[caniuse-major-browser-support]: https://caniuse.com/?compare=chrome+109,edge+109,safari+16.3,firefox+109,and_chr+109,ios_saf+16.3&compareCats=all
[custom-elements-v0]: https://caniuse.com/?search=Custom%20Elements%20V0
[jpegxl]: https://caniuse.com/jpegxl
[wpt.fyi]: https://wpt.fyi
[caniuse]: https://caniuse.com
[mdn-browser-compat-data]: https://github.com/mdn/browser-compat-data
[Interop]: https://wpt.fyi/interop-2023
