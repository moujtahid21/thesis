# Prototypische Evaluation der Nutzung und Darstellung von AR-Inhalten im Web, am Beispiel des Kooperationsprojektes “ARlebnispfad OBK”

## Problemfeld und Kontext

Im Rahmen des Projekts "Historische Augment Reality Tour 'ARlebnis OBK'" der VHS Oberberg soll entlang der [Straße der Arbeit][strasse-der-arbeit] in Wiehl und Wipperfürth ein innovatives Konzept zur digitalen Weiterbildung mittels Augmented Reality (AR) entwickelt werden. Es sollen ältere, nicht technikaffine Menschen sowie jüngere, technikaffine Menschen als auch Schulklassen gleichermaßen an neue Technologien herangeführt und ihnen gleichzeitig der Zugang zur Geschichte und Kultur ihrer Region ermöglicht werden. Der Fokus des Vorhabens liegt somit in der Förderung einer generationenübergreifenden, inklusiven und nachhaltigen Strategie zur digitalen Weiterbildung.

Augmented Reality gehört zum Sammelbegriff Extended Reality (XR) und umfasst zusätzlich die Technologien Virtual Reality (VR) und Mixed Reality (MR). Es wird davon ausgegangen, dass sich die Marktgröße des XR-Sektors von 2023 bis 2027 mehr als verdoppeln wird ([ARtillery Intelligence, 2022][ar-market-size]).

AR wird heutzutage in verschiedenen Formen bereits vorwiegend im E-Commerce, in Videospielen und in Social-Media Anwendungen eingesetzt ([Statista, Revenues, 2023][ar-software-statista]). Zu den bekanntesten Anwendungen gehören hierbei Pokémon Go, TikTok, Wayfair, Instagram und IKEA Place mit einem gemeinsamen Marktanteil von 55\% ([Statista, Market Shares, 2023][ar-software-statista]).

Die meisten AR-Anwendungen werden nativ mit den von Google und Apple bereitsgestellten Software Development Kits (SDKs) [ARCore][ar-core] und [ARKit][ar-kit] entwickelt. Diese bieten den Vorteil, den direkten Zugriff auf die erforderliche Gerätehardware zu ermöglichen und somit ein performantes und nutzerfreundliches Erlebnis mit allen Funktionen anbieten zu können. Ein Nachteil hierbei ist, dass Nutzer und Nutzerinnen vor Verwendung die benötigte App herunterladen und auf dem eigenen Gerät installieren müssen.

Eine andere Möglichkeit der Entwicklung und Darstellung von AR-Inhalten bietet die [WebXR Device API][webxr] über den Browser. Dadurch, dass die Spezifikation noch in Entwicklung ist und sich stetig verändert, ist eine einhaltliche Entwicklung über die verschiedenen Browser nicht möglich. So wird diese auf Apple iOS Geräten und der von allen auf dem Betriebssystem laufenden Browser-Engine, WebKit, gar nicht unterstützt ([Can I Use, 2023][caniuse-webxr]). Die Integration der benötigten Schnittstellen sind zwar in Entwicklung ([WebKit Bugtracker, 2023][webkit-bugtracker]), jedoch kann hier der Standpunkt nicht genau nachvollzogen werden.

Damit AR-Inhalte trotzdem auch in Browsern angezeigt werden können, die die WebXR Device API nicht unterstützen, können externe Bibliotheken wie z. B. [AR.js][arjs], [A-Frame][aframe] oder [model-viewer][model-viewer] verwendet werden. Diese setzen intern auf Polyfills, z. B. direkter Zugriff auf benötigte Sensoren, um die fehlenden Funktionen bereitstellen zu können.

## Zielsetzung

Das Ziel dieses Praxisprojektes ist es, die technischen Möglichkeiten von AR-Erlebnissen im Web zu analysieren, zu evaluieren und diese dann prototypisch zu implementieren. Das Projekt findet parallel zum Wahlpflichtfach (WPF) "Digitale Kommunikation" statt und soll die dort erarbeiteten Inhalte aufgreifen.

## Aufgabenstellung

Anhand des zuvor beschriebenen Problemfeldes, des Kontextes und des Ziels des Praxisprojektes, kann als konkrete Aufgabenstellung das Aufzeigen technischer Möglichkeiten von AR-Erlebnissen mit Hilfe von Webtechnologien festgelegt werden. Hierbei wird der Fokus nicht auf die Erstellung der eigentlichen Inhalte, sondern auf die technische Darstellung und Interaktion mit den Inhalten im Web gelegt.

## Lösungsansätze und Ressourcen

Folgende Ressourcen könnten für die Bearbeitung des Projektes benötigt werden:

- Entwicklungsumgebung
- AR-kompatibles Smartphone
- Tracking-Marker
- Geolocation Daten
- AR-Inhalte zur Darstellung (Video, Audio, Bilder, Text, 3D-Modelle)

Folgende Literatur könnte für die Bearbeitung des Projektes verwendet werden:

- [Web AR: A Promising Future for Mobile Augmented Reality - State of the Art, Challenges, and Insights](https://www.researchgate.net/publication/331205524_Web_AR_A_Promising_Future_for_Mobile_Augmented_Reality_-_State_of_the_Art_Challenges_and_Insights)
- [Evaluating User Acceptance using WebXR for an Augmented Reality Information System](https://ieeexplore.ieee.org/document/9419122)

Folgende Technologien und Ressourcen könnten zur Bearbeitung der Aufgabenstellung herangezogen werden:

- [WebXR API][webxr-mdn]
- [AR.js][arjs]
- [A-Frame][aframe]
- [Babylon.js][babylonjs]

## Chancen und Risiken

Durch die Bearbeitung des Projektes können vor allem die technischen Möglichkeiten zur Umsetzung von AR-Inhalten im Web aufgestellt werden.

Bei einer erfolgreichen Umsetzung kann das Bildungsangebot für die verschiedenen Zielgruppen erweitert werden. Außerdem wird somit ein neuer Zugang zur Vermittlung von historischem Wissen ermöglicht.

Das größte potenzielle Risiko wären Probleme bei der technischen Umsetzung der AR-Inhalte im Web-Umfeld, da die WebXR Spezifikation nicht kompatibel mit allen Browsern ist und die anderen genannten Technologien nur einen gewissen Bereich der Tracking-Methoden abdecken.

## Motivation

Die Motivation zur Bearbeitung des Projektes besteht zum einen aus dem Interesse zu neuen Technologien. In dem XR-Sektor ist in den nächsten Jahren mit einem erhöhten Wachstum zu rechnen, wodurch sehr gute Perspektiven für die zukünftige Entwicklung und Nutzungsbereitschaft der Technologie geboten werden.

Als Medieninformatiker bringe ich zusätzlich im Umgang mit Webtechnologien die benötigten fachlichen Kompetenzen mit.

Durch den Studienort am Campus Gummersbach besteht eine persönliche Bindung an den Oberbergischen Kreis. Durch das Projekt kann also ein Beitrag zur regionalen Entwicklung beigesteuert werden.

## Durchführungskontext und zeitliche Planung

### Setup

Das Projekt soll im Rahmen der TH Köln parallel zum WPF "Digitale Kommunikation" durchgeführt werden. Als Initiator fungiert die VHS Oberberg als Auftraggeber zusammen mit anderen Kooperationspartnern mit direktem Interesse, jedoch ohne direkten Einfluss auf das Projekt.

### Abhängigkeiten

Die Durchführung des Projektes ist von den im WPF erarbeiteten Inhalten und Erkenntnissen abhängig. Diese werden im Praxisprojekt aufgegriffen, analysiert und prototypisch implementiert. Außerdem müssen die technischen Ressourcen zur Umsetzung des Projektes gegeben sein. Abhängigkeiten von den Ergebnissen dieser Projektarbeit gibt es nicht.

### Meilensteine und Zeitrahmen

Die zu erarbeitenden Meilensteine sind von den Inhalten des WPFs abhängig, können aber in folgende Punkte eingeteilt werden:

- Festlegung der jeweiligen AR-Inhalte (1 Woche)
- Vergleich AR Bibliotheken/Frameworks (2 Wochen)
- Recherche zu existierenden Implementierungen (1 Woche)
- Prototypische Implementierung der Inhalte (3 Wochen)
- Cross-Browser Tests der Funktionen (1 Woche)
- Dokumentation der Ergebnisse (2 Wochen)

Der 05.07.2023 ist im WPF als letzter Termin festgelegt. Somit könnte auch dieses Projekt bis zu diesem Termin bzw. bis Mitte Juli fertiggestellt werden.

**Der 04.07.2023 ist im Sommersemester 2023 als der letzte Termin zur möglichen Abschlusspräsentation des Projektes festgelegt.**

## Arbeitsergebnis

Das Ergebnis des Praxisprojektes soll eine genaue Darstellung der Möglichkeiten zur technischen Umsetzung von AR-Inhalten im Web sein und eine Antwort auf die gestellten Forschungsfragen beinhalten. Durch diese kann den Kooperationspartnern bei Fragen zur Einbindung von neuen Inhalt eine klar definierte Antwort mit den jeweiligen Möglichkeiten geboten werden.

<!-- Sources -->

[strasse-der-arbeit]: https://www.ich-geh-wandern.de/stra%C3%9Fe-der-arbeit-bergisches-land
[ar-market-size]: https://artilleryiq.com/reports/xr-global-revenue-forecast-2021-2026/
[ar-software-statista]: https://www.statista.com/outlook/amo/ar-vr/ar-software/worldwide
[ar-core]: https://developers.google.com/ar
[ar-kit]: https://developer.apple.com/augmented-reality/
[webxr]: https://www.w3.org/TR/webxr/
[webxr-mdn]: https://developer.mozilla.org/en-US/docs/Web/API/WebXR_Device_API
[caniuse-webxr]: https://caniuse.com/webxr
[webkit-bugtracker]: https://bugs.webkit.org/show_bug.cgi?id=208988
[arjs]: https://github.com/AR-js-org/AR.js
[aframe]: https://github.com/aframevr/aframe
[model-viewer]: https://github.com/google/model-viewer
[threejs]: https://threejs.org/
[webgl]: https://www.khronos.org/webgl/
[artoolkitjs]: https://github.com/artoolkitx/jsartoolkit5
[webrtc]: https://www.w3.org/TR/webrtc/
[webvrpolyfill]: https://aframe.io/docs/1.4.0/introduction/vr-headsets-and-webxr-browsers.html#which-browsers-does-a-frame-support
[babylonjs]: https://doc.babylonjs.com/features/featuresDeepDive/webXR/webXRARFeatures
