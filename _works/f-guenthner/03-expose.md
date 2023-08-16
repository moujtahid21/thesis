# Exposé

## Problemfeld und Kontext
Eine bestehende Dating-App, die mit dem Framework Flutter entwickelt wurde, soll um das Feature „Virtuelle Geschenke“ erweitert werden. Dadurch können Benutzer ihren Matches virtuelle Geschenke senden. Diese Geschenke werden mithilfe von Augmented Reality (AR) im Umfeld der Benutzer dargestellt. Diese Funktionalität konnte aufgrund fehlender AR-Plugins für Flutter Web bislang nicht implementiert werden (Pub Dev, 2023). Das Ziel dieser Arbeit besteht daher darin, ein solches AR-Plugin für die Web-Plattform zu entwickeln und damit die gewünschte Funktionalität in der App zu ermöglichen.

Augmented Reality gehört zur Gruppe der Extended Reality-Technologien, die unsere Sinne erweitern, einschließlich Virtual Reality und Mixed Reality (Microsoft, 2023). Durch AR wird die physische Welt mit der digitalen Welt verbunden und ermöglicht eine begrenzte Interaktion mit digitalen Elementen, die über eine reale Ansicht eingeblendet werden. Im Jahr 2021 wurde der Wert des mobilen Augmented-Reality-Marktes auf 12,45 Milliarden US-Dollar geschätzt. Es wird prognostiziert, dass der Wert bis 2026 auf über 36 Milliarden US-Dollar ansteigt. Der Markt umfasst digitale Güter wie In-App-Käufe in AR-Anwendungen sowie Werbeplatzierungen und Visualisierungssoftware (ARtillery Intelligence, 2023). Dies unterstreicht das Potenzial von AR und die Notwendigkeit, diese Technologie für Flutter Web zugänglich zu machen. Die Entwicklung eines solchen Plugins würde die Grenzen des Möglichen erweitern und das Potenzial von Flutter als Werkzeug für die Erstellung interaktiver, immersiver Web-Erlebnisse verbessern.

Für IOS und Android sind kompatible Software-Entwicklungskits für AR verfügbar (Google Developers, 2023). Für die Web-Plattform gibt es die WebXR-API, die AR-Erfahrungen im Web bereitstellen soll. Diese befindet sich jedoch noch in der Entwicklung, verändert sich stetig und hat einige Einschränkungen in Bezug auf Geräte und Browser-Kompatibilität (MDN Web Docs, 2023). Zum Beispiel gibt es keine Unterstützung für IOS-Geräte (Can I Use, 2023). Zudem weist Flutter Web trotz seiner Stabilität noch einige Probleme auf, darunter Leistungsschwankungen abhängig vom verwendeten Renderer, fehlende Web-APIs und Herausforderungen bei der Plugin-Entwicklung (Günthner, 2023). Vor diesem Hintergrund stellt sich die Frage, inwiefern ein AR-Plugin entwickelt werden kann. Da das Risiko eines Misserfolgs besteht, wird in der Forschungsarbeit mit einem Fallback gearbeitet, der im Falle eines Scheiterns der Entwicklung zum Einsatz kommt.

## Problem
Zum aktuellen Zeitpunkt (25.07.2023) existiert im Flutter-Ökosystem kein Plugin, das die Umsetzung von AR-Erfahrungen für Flutter Web ermöglicht.

## Zielsetzung
Entwicklung und Konzeption eines AR-Plugins für das Flutter-Ökosystem, um AR-Funktionalitäten in Flutter Web zu ermöglichen. Dieses Plugin sollte in der Lage sein, einen spezifischen Anwendungsfall zu unterstützen, der auf der in der Praxis entwickelten App basiert.

## Ergebnisse
Die Forschung zielt darauf ab, zu klären, ob die Entwicklung und Veröffentlichung eines funktionalen AR-Plugins für Flutter Web möglich ist, das gleichzeitig einen spezifischen Anwendungsfall unterstützt.

## Forschungsfragen
1. Wie kann ein Argumented Reality Plugin in Flutter Web unter Verwendung der WebXR-API effektiv implementiert werden?
2. Was sind die Herausforderungen und Hürden bei der Entwicklung eines Argumented Reality Plugins für Flutter Web und wie können diese gelöst werden?
3. Welche spezifischen Anforderungen hat der ausgewählte Anwendungsfall an das Argumented Reality Plugin und wie können diese erfüllt werden?
4. Wie kann eine robuste und wirksame Fallback-Lösung für den Fall eines Misserfolgs bei der Implementierung des Argumented Reality Plugins entworfen und implementiert werden?
5. Wie und warum wird der Anwendungsfall für die Implementierung von Argumented Reality in einer Flutter Web App bestimmt und welche Aspekte der Argumented Reality werden hierbei besonders fokussiert?

## Quellen
- Microsoft. (2023). Was ist Augmented Reality oder AR?. Abgerufen am 25. Juli 2023, von https://dynamics.microsoft.com/de-de/mixed-reality/guides/what-is-augmented-reality-ar/
- ARtillery Intelligence. (2023). Mobile augmented reality (AR) market revenue worldwide from 2021 to 2026. Abgerufen am 25. Juli 2023, von https://www.statista.com/statistics/282453/mobile-augmented-reality-market-size/
- Felix Günthner. (2023). Entwicklung einer produktionsreifen Progressive Web App mit dem Cross-Platform Framework Flutter. Abgerufen am 25. Juli 2023, von https://drive.google.com/file/d/1g0p2afaJWmL5J9aKgsMcmmHsgIOlZm_A/view?usp=sharing
- Can I Use. (2023). Can I use WebXR Device API. Abgerufen am 24. Juli 2023, von https://caniuse.com/webxr
- Google Developers. (2023). Make the world your canvas. Abgerufen am 25. Juli 2023, von https://developers.google.com/ar?hl=en
- MDN Web Docs. (2023). WebXR Device API. Abgerufen am 25. Juli 2023, von https://developer.mozilla.org/en-US/docs/Web/API/WebXR_Device_API
- Pub Dev. (2023). The official package repository for Dart and Flutter apps. Abgerufen am 25. Juli 2023, von [https://pub.dev](https://pub.dev/)