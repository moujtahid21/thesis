# Exposé für eine Masterarbeit zum Thema:
**Untersuchung und Vergleich verschiedener Ansätze zur Implementierung von Microfrontends**

## Vorgelegt von:
Javad Alamdar\
Merowinger Str 192\
40225 Düsseldorf\
E-Mail: javad.alamdar@smail.th-koeln.de

Matrikelnummer: 11136142\
MA Medieninformatik\
Datum: 11.09.2023

## Einleitung

In den letzten Jahren hat sich die Landschaft der Webarchitekturen erheblich verändert. Diese Veränderungen sind auf die Einführung neuer Trends und Technologien zurückzuführen, die Art und Weise, wie Webanwendungen entwickelt und verwaltet werden, revolutioniert haben. Heutzutage müssen Webseiten hochwertig, reaktionsschnell, schnell ladend und geräteübergreifend nutzbar sein, um unterschiedliche Interaktionsmöglichkeiten für verschiedene Benutzer anzubieten.

In diesem sich ständig ändernden Szenario hat sich die Micro Frontend Architektur ähnlich wie die Microservices Architektur im Hinblick auf das Backend-Development zu einer der führenden Technologien für die Entwicklung skalierbarer und modularer Webanwendungen entwickelt.

Die Idee hinter Microfrontends besteht darin, die Entwicklung, Wartung und Skalierbarkeit von Frontend Anwendungen zu verbessern, indem sie in kleinere, handhabbare Teile aufgeteilt werden. Jedes Microfrontend kann von seinem eigenen Team entwickelt, getestet und bereitgestellt werden. Dadurch können Teams unabhängig voneinander arbeiten, ohne sich gegenseitig zu beeinträchtigen.

## Problemfeld und Kontext

In unserer digitalisierten Welt sind Webanwendungen allgegenwärtig geworden und spielen eine entscheidende Rolle in Bereichen wie E-Commerce, Unternehmensanwendungen, sozialen Medien und mehr. Moderne Webanwendungen müssen nicht nur benutzerfreundlich und funktionsreich sein, sondern auch skalierbar, wartbar und flexibel. Diese Anforderungen haben zu einer Evolution in der Art und Weise geführt, wie Frontend-Anwendungen entwickelt und bereitgestellt werden, und das Konzept der "Microfrontends" hat an Bedeutung gewonnen.

Das Problemfeld, dem diese Untersuchung gewidmet ist, liegt in der Notwendigkeit, effiziente Strategien zur Entwicklung, Integration und Verwaltung von Microfrontends zu identifizieren und zu verstehen. Angesichts der Vielfalt der Ansätze, die derzeit auf dem Markt verfügbar sind, stehen Entwickler vor der Herausforderung, den besten Weg zu finden, um Microfrontends in bestehende oder neue Webanwendungen zu integrieren.

Die Skalierbarkeit von Webanwendungen, insbesondere in großen Organisationen oder Projekten, kann schnell zu einem Engpass werden. Das Management verschiedener Teams, die unabhängig voneinander an unterschiedlichen Teilen der Anwendung arbeiten, kann komplex sein und zu Problemen bei der Koordination, Konsistenz und Effizienz führen.

Zusätzlich dazu sind Webanwendungen oft gezwungen, auf verschiedenen Plattformen oder in unterschiedlichen Technologiestapeln zu arbeiten. Dies kann zu Inkonsistenzen, Performance-Problemen und mangelnder Wartbarkeit führen.

Unsere Untersuchung beginnt mit einer grundlegenden Einführung in das Konzept der Microfrontends und erklärt, wie es sich von traditionellen monolithischen Ansätzen unterscheidet. Wir werden die zugrunde liegenden Prinzipien erkunden, die es ermöglichen, Frontend-Anwendungen in kleinere, autonome Einheiten aufzuteilen, die unabhängig voneinander entwickelt, getestet und skaliert werden können.

Im weiteren Verlauf werden wir verschiedene Ansätze zur Implementierung von Microfrontends betrachten.Es gibt verschiedene Ansätze zur Implementierung von Microfrontends, wie z.B. komponentenbasierte Frontends, clientseitige oder serverseitige Integrationen, Web Components und Module Federation. Jedes dieser Ansätze hat seine eigenen Vor- und Nachteile, abhängig von den Anforderungen des Projekts und den technischen Präferenzen.

Die zentrale Fragestellung, die diese Untersuchung angeht, lautet daher: Welche Ansätze zur Implementierung von Microfrontends sind verfügbar, wie unterscheiden sie sich voneinander und wie können Entwickler die am besten geeignete Methode für ihre spezifischen Anforderungen auswählen?

Indem wir verschiedene Ansätze zur Implementierung von Microfrontends untersuchen und vergleichen, werden wir dazu beitragen, Klarheit über die Vor- und Nachteile jedes Ansatzes zu schaffen. Wir werden uns mit Fragen der Performance, Wartbarkeit, Flexibilität und Integration auseinandersetzen, um Entwicklern und Technologieentscheidern dabei zu helfen, fundierte Entscheidungen zu treffen, die auf den Bedürfnissen ihrer Projekte und Anwendungen basieren. Die Ergebnisse dieser Untersuchung werden dazu beitragen, bewährte Praktiken und Strategien für die erfolgreiche Implementierung von Microfrontends zu identifizieren und zu etablieren.

## Zielsetzung

Das Hauptziel dieser Masterarbeit ist es, verschiedene Ansätze zur Implementierung von Microfrontends zu analysieren und miteinander zu vergleichen, um fundierte Erkenntnisse und Empfehlungen für die Auswahl und Umsetzung von Microfrontend-Architekturen in modernen Webanwendungen zu liefern. 

## Forschungsfragen
Vor dem Hintergrund des Kontexts und der Ziele lassen sich die folgenden Unterfragen stellen, die in dieser Arbeit beantwortet werden sollen.

1. Wann ist sinnvoll über microfrontend nachdenken ?
2. Welche Vor- und Nachteile hat ein Microfrontend?
3. Welche Entwicklungswerkzeuge und Frameworks sind am besten geeignet, um Microfrontends zu erstellen und zu verwalten? 
4. Wie beeinflussen die verschiedenen Micro Frontend-Frameworks die Performance und Ladezeiten von Webanwendungen ?
5. Welche Frameworks bieten die besten Tools und Methoden, um das Testen und die Qualitätssicherung von Micro Frontends zu erleichtern?
6. Welche Herausforderungen treten typischerweise bei der Implementierung von Micro Frontends auf?
7. Wie einfach ist es, Änderungen und Updates in einem Micro Frontend-Framework durchzuführen, ohne Auswirkungen auf andere Module zu haben?
8. Welche verschiedenen Ansätze zur Implementierung von Microfrontends existieren, und wie unterscheiden sie sich in Bezug auf Architektur, Integration und Kommunikation?
9. Welche Ansätze zur Implementierung von Microfrontends sind am effektivsten? 
10. Wie können diese Ansätze die Performance und Wartbarkeit verbessern? 
11. Welche Erfahrungen haben Unternehmen gemacht, die bereits Microfrontends implementiert haben, und welche Empfehlungen können daraus abgeleitet werden?

## Gliederungsentwurf
1. Einleitung
   * Problemfeld und Kontext 
   * Zielsetzung
   * Hintergrund und Motivation
   * Forschungsfragen
2. Archäologie der Webentwicklung
   1. Die Ursprünge des Webs
      1. HTML
      2. CSS
      3. Javascript
    2. Dynamische Seiten, Frameworks und Bibliotheken
    3. Client Server Architekture
3. Evolution der Webarchitekturen
   1. Dreischichtige Architektur
   2. Web service Architekture
       1. REST
       2. SOAP
       3. RPC
   3. Backend Architekturen
       1. Monolithische
       2. Microservices
       3. Service Oriented (SOA)
   4. Frontend Architekturen 
       1. Multi Pageanwendung (MPA)
       2. Single Pageanwendung (SPA)
       3. Model-View-ViewModel (MVVM)
       4. Model-View-Controller (MVC)
       5. Serverseitiges Rendering (SSR)
       6. Clientseitiges Rendering (CSR)
4. Microfrontend Architekture
    1. Definition und Konzept von Microfrontends
    2. Aus Monolithische Architektur zu Microfrontend Architektur 
    3. Microfrontend Frameworks
       1. Piral
       2. Qiankun
       3. Luigi
       4. Podium
       5. Vergleich der Eigenschaften und Funktionen der Frameworks
    4. Technologien und Tools for Microfrontend
       1. Web Components
       2. Module Bundler
       3. Package Manager
    5. Vorteile und Herausforderungen von Microfrontends
       1. Vorteile und Einsatzszenarien
          1. Skalierbarkeit
          2. Autonomie
          3. Wiederverwendbarkeit
          4. Unabhängige Bereitstellung
          5. Technologievielfalt
       2. Herausforderungen und Einschränkungen
          1. Komplexität
          2. Performance
          3. Testen und Debuggen  
5. Ansätze zur Implementierung von Microfrontends
    1. iFrames
    2. Komponentenbasiertes Frontend
    3. Clientseitige Integration
    4. Serverseitige Integration
    5. Web Components
    6. Module Federation
6. Evaluierung und Vergleich der Ansätze von Microfrontend Architektur
    1. Definition von Evaluierungskriterien
       1. Performance
       2. Skalierbarkeit und Wartbarkeit
       3. Flexibilität und Erweiterbarkeit
       4. Entwicklungsgeschwindigkeit
       5. SEO Freundlichkeit
       6. Dokumentation und Community Unterstützung
    2. Vergleich mit alternativen Architekturansätzen
    3. Analyse der Ergebnisse
7. Fallstudien und Beispiele aus verschiedenen Branchen und Anwendungsfällen 
   1. NETFLIX
   2. SPOTIFY
   3. DAZN   
8. Fazit und Ausblick 
    1. Zusammenfassung der Ergebnisse
    2. Bewertung der erreichten Ziele
    3. Ausblick und zukünftige Entwicklungen
9. Literaturverzeichnis
10. Anhang    
     
## Zeitplan (noch in der Arbeit, wird nach der Gliederungsentwurf vervollständigt)

*	18.09 - 08.10 - Recherchephase (3 Woche)
*	09.10 - 29.10 - Theoretisches Teil der Arbeit (3 Woche)
*	30.10 - 24.12 - Praktisches Teil der Arbeit (8 Woche)
*	25.12 - 21.01 - Evaluation den Ergebnissen (4 Woche)
*	22.01 - 18.02 - Zusammenfassung und Korrektur (4 Woche)

## Ergebnis
tbd

## Literaturverzeichnis

* https://micro-frontends.org/
* https://intellipaat.com/blog/what-is-client-server-Architecture/#:~:text=Client%20server%20architecture%20is%20a
* Davide Taibi and Luca Mezzalira. 2022. Micro-Frontends: Principles, Implementations, and Pitfalls. SIGSOFT Softw. Eng. Notes 47, 4 (October 2022), 25–29. https://doi.org/10.1145/3561846.3561853
* Kroiß, Manuel. From Backend to Frontend-Case study on adopting Micro Frontends from a Single Page ERP Application monolith. Diss. Wien, 2021
* Nishizu, Yuma, and Tetsuo Kamina. "Implementing Micro Frontends Using Signal-based Web Components." Journal of Information Processing 30 (2022): 505-512
* Baumann, Matthias. Micro-Frontends. Diss. HSR Hochschule für Technik Rapperswil, 2019
* Tutisani, Tengiz. "Design and Architecture." Effective Software Development for the Enterprise: Beyond Domain Driven Design, Software Architecture, and Extreme Programming. Berkeley, CA: Apress, 2023. 105-175
* Pavlenko, A., Askarbekuly, N., Megha, S., & Mazzara, M. (2020). Micro-frontends: application of microservices to web front-ends. J. Internet Serv. Inf. Secur., 10(2), 49-66
* Bui, S. (2021). Micro frontend: Microservice implementation on Web Development.
