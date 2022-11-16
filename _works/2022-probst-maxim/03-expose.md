# Exposé

Dem folgendem Praxisprojekt liegt eine grundlegende Frage zu Grunde: Wie kann man eine schnelle Zwischenlösung für die Umgestaltung alter Klienten erstellen und für den ersten Einsatz bereitstellen. 
Durch das Projekt wird soll der Firma eine Möglichkeit geboten werden auf Basis einer bestehenden XML-Vorlage einen automatisch generierten Webklienten zu erstellen. Dieser soll einen ersten Eindruck für das neue Design ermöglichen und im besten Falle als eine Übergangslösung für die Umstellung dienen.
Hierbei werden Folgende Fragen gestellt:
-	Was ist das beste Vorgehen bei dem Einlesen und Interpretieren der bestehenden XML Vorlage?
-	Welches Fronend-Framework eignet sich bei einer Solchen Umsetzung am besten?
-	Wie komplex ist eine Inbetriebnahme durch Anschluss der Datenbank, in einer solchen generierten Webumgebung?
Als Basis des Projektes dient ein alter FAT-Client, welcher durch eine Beschreibende XML-Datei erzeugt wird. Diese XML-Vorlage beschreibt im Detail die Anordnung der zur Verfügung stehenden Elemente in den dargestellten Tabs. Zusätzlich ist in jeder Komponente Logik dargestellt, welche Nutzerrechte, Daten Befüllung und sonstige komplexe Darstellungs-Sonderregeln beschreibt. Zum Aufabau des Projektes stehen mir zudem zwei Frameworks zur Verfügung, React und Vaadin. Die Abwägung dieser Frameworks und deren detailierte beschreibung wird als Teil des Projektes betrachtet. 
Das Projekt zeichnet sich durch mehrere Teilschritte aus. Zunächst ist es  wichtig durch Recherche im Internet, aber auch durch interne Expertenbefragung die geeigneten Frameworks und Lösungsansätze zu ermitteln. Da firmen intern mehrere Frontendentwickler momentan React und Vaadin nutzen bietet sich hier mehrere Experteninterviews an. 
In dem zweiten Schritt muss das Regelwerk erstellt werden, welches zum Interpretieren der XML-Vorlage dient. Dieses wird zunächst statisch anhand der Vorhandenen Regeln in dem Programm implementiert. 
Folgend wird dann eine Lösung zum Einlesen der XML-Vorlage erstellt, welche auf Basis der Regeln in eine von dem Programm interpretierbare Form bringt.
Wenn alle notwendigen Daten in dem neuen System vorhanden sind, müssen diese dann mittels Fronendkomponenten dargestellt werden. Diese Komponenten sind zu designen und anhand der Regeln anzuordnen.
In dem letzten Schritt wird die Komplixität einer Anbindung an die Datenbank ermittelt, und ob diese noch im Umfang meines Projektes unter einem angemessenen Umfang an Arbeit ergänzt werden kann.
Zum Ende des Projektes soll ein Prototyp zur Generierung eines Fronenddesigns erstellt und durch eine Umfassende Dokumentation beschrieben sein. Dieser Prototyp sollte als eine mögliche Designvorlage für das Vollständige Projekt dienen können und mit relativ wenig Arbeitsumfang an andere Systeme angepasst werden können.
Zudem wird eine Umfassende Analyse zu dem genutzten und abgewogenen Framework erstellt, welche in zukünftigen Projekten als Unterstützung zur Entscheidung Findung dienen kann.
