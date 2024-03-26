## Explorative Konzeption und Implementierung einer Web-basierten Plattform zur musikalischen Echtzeit-Kollaboration an Modular-Synthesizern

### Problemfeld und Kontext
Das synchrone Musizieren mit mehreren Personen ist eine Aktivität,
welche in aller Regel einen örtliche Nähe voraussetzt.
Während es in Band-Kontexten, in welchen jede Person
ein separates Instrument spielt - vor allem vorangetrieben
durch die Covid 19-Pandemie - Software-Lösungen für
Remote-Probesessions gibt (z.B. Jamkazam https://jamkazam.com oder Jamulus https://jamulus.io/de/), stellt die rein elektronische Klangerzeugung
ein abzugrenzendes Problemfeld dar.
Synthesizer und speziell Modular-Synthesizer sind Instrumente,
welche in der Regel nie zwei mal identisch vorhanden sein können.
Durch die Zusammensetzung des Synthesizers durch Module,
welche (innerhalb eines standardisierten Formats wie Eurorack)
frei wählbar sind und nach belieben angeordnet werden können,
ist es nahezu unmöglich, mit mehr als einer Person an einem Modular-Synthesizer zu arbeiten,
wenn nicht beide Personen sich im gleichen Raum befinden.

Selbst wenn zwei Personen an zwei unterschiedlichen Orten
über ein identisch konfiguriertes Modularsynthesizer-System verfügen würden,
besteht eine zentrale Hürde in der Analogität des Systems.
Die in den Modulen verbauten Potentiometer sind in der Regel stufenlos
und können theoretisch unendlich viele Positionen einnehmen (dies ermöglicht unter Anderem Mikrotonalität),
was es praktisch unmöglich macht, dass zwei Personen an zwei Systemen
die exakt gleichen Reglerpositionen einstellen und somit nie einen identischen Klang erzeugen können.


### Ziel
Das Ziel dieses Projekts besteht darin, Möglichkeiten für die Klangerzeugung im Web zu konzipieren
und im Kontext eines Systems zur kollaborativen Nutzung von Modular-Synthesizern zu implementieren.
Neben rein technischen Ansätzen zur Klangerzeugung soll dabei auch untersucht werden,
welche Strategien zur Synchronisierung von mehreren Sessions sinnvoll sein können - hier entstehen vor allem Herausforderungen im Kontext von zu verwendenden Web-Architekturen.

Der Weg zu dem definierten Ziel eines nutzbaren Systems ist dabei
bewusst hinsichtlich der Konzeption und Implementierung explorativ aufgebaut - durch das Projekt sollen vor allem unterschiedliche technische Möglichkeiten
und Implementierungsansätze durch die praktische Anwendung im Entwicklungsprozess untereinander abgewogen werden.


### Aufgabenstellung
Die zentrale Aufgabe besteht darin, eine real nutzbare Plattform zur virtuellen Kollaboration
an Modular-Synthesizern im Web umzusetzen.

Dabei sollen Fragen und Herausforderungen, welche zu Beginn oder während der Implementation
des Systems entstehen, nach wissenschaftlichen Prinzipien erforscht und beantwortet werden.
Die praktische Umsetzung bietet dabei neben der rein theoretischen Abwägung von Handlungsansätzen
eine reale Umsetzung der erforschten Ansätze und beweist oder widerlegt diese durch praktische Anwendung.
Durch die explorative Gestaltung dieses Prozesses kann der gesamte Forschungs-
und Entwicklungsablauf sehr dynamisch auf entstehende Hürden reagieren und Rückschritte ermöglichen.


### Lösungsansätze
Die vorgegebene Aufgabenstellung setzt voraus, dass der gesamte technische Stapel der Klanggenerierung
im Web betrachtet werden muss, um das System entwickeln und dabei wissenschaftliche Erkenntnisse sammeln zu können.

Grundsätzlich muss zur Umsetzung des Systems eine Grundlagenforschung zur Funktionsweise
und möglichen Ansätzen von Klanggenerierung im Web stattfinden.
Dies ist nötig, da weitere Eigenentwicklungen oder beispielsweise bestehende Bibliotheken
anderer Entwickler voraussichtlich auf den Grundlagen dieses Tech-Stacks aufbauen,
und nur so ein tiefgreifendes Verständnis über den gesamten Stack entstehen kann.

Neben der Theorieforschung ist es dabei wichtig, bestehende Lösungen zu betrachten,
welche in vergleichbaren Kontexten existieren. So kann durch die Betrachtung praktischer Umsetzungen
(und im besten Fall des Source-Codes bei Open-Source Projekten)
weiteres Verständnis und Erkenntnisse hinsichtlich der praktischen Umsetzung entstehen.


### Chancen und Risiken
Kollaborative musikalische Prozesse setzen in der Regel voraus,
dass auditives Feedback zwischen den Musikern (nach menschlicher Wahrnehmung) Latenzfrei stattfindet.
Andernfalls können zeitliche Abweichungen entstehen und der gemeinsame Rhythmus verloren gehen.
Die Minimierung der Latenz bei gleichzeitiger Berücksichtigung akzeptabler Audioqualität ist somit unabdingbar
und stellt perspektivisch eine der zentralen Herausforderungen des Projekts dar.

Die im Kapitel 1 - Problemfeld beschriebene Analogität modularer Synthesizer
und die damit einhergehenden theoretisch unendlichen Konfigurationsmöglichkeiten
werden häufig als einer der zentralen Alleinstellungsmerkmale analoger Synthesizer gesehen.
Da diese Bandbreite an Möglichkeiten durch die digitale Simulation gezwungenermaßen eingegrenzt werden muss,
besteht in diesem Punkt das Risiko, dieses Alleinstellungsmerkmal eines Modularsynthesizers zu verlieren.
Ob und in welchem Umfang dies tatsächlich geschieht, wird davon abhängig sein,
wie stark diese Möglichkeiten unter Berücksichtigung anderer Anforderungen eingegrenzt werden müssen.

Die Ergebnisse dieser Arbeit können perspektivisch die Chance bieten,
Erkenntnisse über den Kontext der musikalischen Kollaboration hinaus zu bieten.
Es gibt viele Anwendungsfälle, in welchen ein synchroner Austausch mit mindestens zwei Personen
via des Webs nötig ist - dies kann auditiv oder visuell stattfinden, oder über einen anderen Kanal erfolgen.
Idealerweise bietet die Entwicklung der Synthesizer-Plattform neben Kontextspezifischen
auch allgemeingültige Erkenntnisse, welche für solche weiteren Projekte
wertvoll sein können - beispielsweise bezüglich Web-Architekturen, Frontend-Entwicklungsansätzen oder weiteren Themenfeldern.


### Ressourcen
Neben einem Grundverständnis zur Funktionsweise von Synthesizern und Modularsynthesizern im speziellen
ist es wichtig zu verstehen, wie der kollaborative Prozess an solcher Hardware in der Regel abläuft,
um die Anforderungen für eine Digitalisierung dieses Prozesses erarbeiten zu können.
Dafür steht ein Teenage Engineering PO400 (https://teenage.engineering/store/400) zur Verfügung.
Dieser Synthesizer bietet eine ähnlich modulare Aufteilung wie vollständig modulare Synthesizer
und kann somit im Rahmen des Projekts genutzt werden, um Vergleiche zwischen digitalen
und realen Handlungsschritten zu ziehen.

Desweiteren besteht ein Grundverständnis und -Erfahrung in der Nutzung von VCVRack (https://vcvrack.com),
einer Simulation von Eurorack-Synthesizern. Dies bietet ein Beispiel für Software,
anhand welcher ein Abgleich zu bisher existierenden digitalen Simulationen solcher Systeme gezogen werden kann.


### Motivation
Musikalische Kollaboration ist ein Prozess, welcher neben dem Unterhaltungsfaktor
und der Schaffung eines kreativen Ventils durch den Input mehrerer Personen häufig persönliche,
kreative Grenzen erweitern kann. In einer zunehmend digitalen Welt,
in welcher Freundschaften immer häufiger keine geographische Nähe voraussetzen
und vermehrt Prozesse des Alltags digital über große Distanzen stattfinden können,
besteht eine klare Motivation, auch Prozesse des musikalischen Kontextes in solchen Rahmen zu ermöglichen.
Ansätze wie das für dieses Projekt visionierte System haben das Potenzial, vielen Menschen zu helfen,
welche andernfalls aufgrund geographischer Distanz musikalische Projekte nicht umsetzen könnten.

Sollten die in diesem Projekt geschaffenen Erkenntnisse allgemeingültig anwendbar sein,
könnten Anwendungsfälle weit über den musikalischen Kontext hinaus betrachtet
und in technischer Hinsicht ermöglicht oder verbessert werden.


### Setup, Abhängigkeiten und Meilensteine
Bis auf die Vorgabe, das System im Web aufzubauen und via Browser zugänglich zu machen,
ist das Projektsetup bewusst offen gehalten - durch den explorativen Forschungsansatz
sollen möglichst keine Entwicklungsmöglichkeiten durch eine zu frühe Eingrenzung unbetrachtet bleiben.

Um das resultierende System hinreichend Testen zu können, wird das Hinzuziehen
von mindestens einer Testperson nötig sein - aus technischer Sicht mögen zwei Endgeräte zum Testen reichen,
doch um zwischenmenschliche Aspekte bei Remote-Kollaboration betrachten zu können,
ist eine reale Testperson unabdingbar.

Die umgesetzten Funktionalitätsstufen des Systems können als zentrale Meilensteine
in der Projektlaufzeit betrachtet werden. Diese Funktionalitätsstufen können in der Basis
zum Beispiel die Verbindung zweier Web-Sessions umfassen,
in einem späteren Schritt die Klang-Synchronisierung zwischen Sessions beschreiben,
und im letzten Meilenstein schließlich in das vollumfänglich abgeschlossene System münden.
Wie sich diese Stufen konkret unterteilen und welche Meilensteine dadurch entstehen,
wird perspektivisch Teil des Projektablaufes sein.


### Arbeitsergebnis
Das Ergebnis der Arbeit ist ein funktionales, Web-basiertes System zur synchronen Kollaboration
zwischen mindestens zwei Personen an einem virtuellen Abbild eines Modular-Synthesizers.
Damit einher gehen die Erkenntnisse, welche während der Konzeption und Entwicklung
dieses konkreten Systems entstanden sind. Diese Erkenntnisse haben daher den Mehrwert,
dass sie im Rahmen einer real stattgefundenen, praktischen Umsetzung entstanden sind
und daher nicht (nur) auf Basis von theoretischer Forschung bestehen.

Lösungsansätze, stattgefundene Abwägungen und Hürden auf dem Weg zu dem fertigen System
werden dabei anhand der Masterthesis dokumentiert und kritisch eingeordnet.
