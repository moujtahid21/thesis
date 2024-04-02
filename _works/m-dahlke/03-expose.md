<p align="center">
    <img src="./TH_Koeln_Logo.png" alt="TH Köln Schriftzug" width="200">
</p>

# Konzeption und Entwicklung eines Plugins zur automatisierten Moderation von Textinhalten durch KI für die WoltLab Suite Community Software

## Problemstellung und Kontext

Die Moderation von nutzergenerierten Inhalten, bspw. zur Entfernung von rechtswidrigen oder beleidigenden Beiträgen, ist ein wichtiger Bestandteil von Online-Communitys und anderen Plattformen im Internet, bei denen nutzergenerierte Inhalte veröffentlicht werden, um die jeweilige Plattform für alle Nutzer sicher und attraktiv zu gestalten.   

Die manuelle Moderation von nutzergenerierten Inhalten bringt jedoch diverse Probleme mit sich. Das wohl größte Problem ist, dass das Moderieren von Inhalten sehr zeitintensiv sein kann und die dafür investierte Zeit nicht für andere Aufgaben zur Verfügung steht. Zeit ist ein wichtiger Faktor bei der Moderation von Inhalten, da dies sowohl die aufzuwendende und zu kompensierende Arbeitszeit, als auch die Reaktionszeit der Moderation umfasst. Die Reaktionszeit ist die Zeit, welche zwischen der Erstellung eines Inhalts und dessen Moderation vergeht. Je länger ein Inhalt auf dessen Moderation warten muss, desto mehr Nutzer können diesen sehen und darauf reagieren. Die Folgen daraus sind vielfältig und neben verärgerten oder verschreckten Nutzern, können daraus auch weitreichende Konsequenzen, wie bspw. Abstrafungen durch Suchmaschinen resultieren. Bereits bei kleinen Plattformen mit wenig Aktivität und einem kleinen Team an Moderatoren kommt es vor, dass Inhalte nicht rechtzeitig moderiert werden können, bspw. weil die Moderatoren nicht rund um die Uhr online sind. Die Schwierigkeit, jeden Inhalt zeitnah zu überprüfen wird bei ansteigender Größe der Plattform und Anzahl der Inhalte zunehmend schwieriger, was zu einer verminderten Qualität der Moderation führen kann, da Inhalte zu langsam, zu ungründlich oder gar nicht mehr moderiert werden,  möglicherweise auch aus dem Grund, dass einzuhaltende Quoten zur Ermittlung der Moderationsleistung eingeführt werden.  

Anders als für die Leistung von Moderatoren, spielt Zeit oder die Größe der Plattform für die Leistung von KI nur eine untergeordnete Rolle, da dessen Einsatz in der Regel beliebig skalierbar ist. Darüber hinaus ist die manuelle Moderation von Inhalten nicht immer objektiv und transparent. Moderatoren können Inhalte unterschiedlich bewerten und unterschiedlich streng moderieren, was dazu führen kann, dass Nutzer die Moderation als ungerecht oder willkürlich empfinden. Dies kann auch passieren, wenn Sprachbarrieren die Moderation erschweren und Moderatoren Inhalte missinterpretieren, was wiederum dazu führt, dass zusätzliche Moderatoren benötigt werden, welche die Inhalte übersetzen können. Auch diese Probleme können durch den Einsatz von KI gelöst werden, da diese Inhalte immer nach denselben Kriterien und unabhängig von der Inhaltssprache bewerten kann.  

Trotzdem muss die automatisierte Moderation durch KI mit Vorsicht eingesetzt werden, da Inhalte aufgrund fehlender menschlicher Intelligenz und mangelnder Einordnung in den Gesamtkontext, sowie einfach aufgrund von möglichen Fehlern, falsch beurteilt werden können. Um die Integrität der Plattform zu wahren und eine willkürliche Zensur von Inhalten zu vermeiden, muss die Moderation durch KI daher kontinuierlich überwacht bzw. kontrolliert werden.  

## Zielsetzung

Im Rahmen dieser Bachelorarbeit soll ein Plugin für die [WoltLab Suite Community Software][woltlab-suite] konzipiert und entwickelt werden, welches die halbautomatische Moderation von Textinhalten durch KI ermöglicht. Dabei sollen neue Inhalte wie Kommentare oder Forenbeiträge mit Hilfe der [OpenAI-API][openai-api] und dem Sprachmodell GPT-3.5 (evtl. GPT-4) auf unerwünschte Inhalte überprüft werden. Die Lösung soll nahtlos in das Framework der [WoltLab Suite][woltlab-suite] integriert werden und die bereits darin enthaltenden Moderationswerkzeuge verwenden. Dies bedeutet, Inhalte sollen bei einem möglichen Regelverstoß nicht automatisch gelöscht, sondern lediglich zur Überprüfung markiert werden. In einem dafür vorgesehenen Moderationsbereich hat ein Moderator anschließend die Möglichkeit, Änderungen am Inhalt vorzunehmen und zu entscheiden, ob der Inhalt gelöscht oder freigegeben werden soll.  

## Aufgabenstellung und Forschungsfragen

Um nachvollziehen zu können, wie Sprachmodelle funktionieren, bedarf es eingangs einer kurzen Recherche zu diesem Thema. Dabei wird auch geprüft, inwiefern Sprachmodelle zur automatisierten Moderation von Textinhalten verwendet werden können und welche Vor- und Nachteile dies mit sich bringt.  

Bevor im Anschluss mit der Entwicklung des Plugins begonnen werden kann, müssen zunächst die Anforderungen an das Plugin identifiziert und priorisiert werden. Darüber hinaus muss ermittelt werden, wie die [OpenAI-API][openai-api] für diesen Einsatzzweck in das Framework der [WoltLab Suite][woltlab-suite] integriert werden kann. Erst anhand der Spezifikation der genutzten API, sowie den ermittelten Anforderungen kann das Plugin konzipiert werden. Nach Fertigstellung der Konzeption kann anschließend mit der Implementierung des Plugins begonnen werden.  

Nach Abschluss der Entwicklung des Plugins muss dieses getestet und auf Anforderungserfüllung überprüft werden. Während der Evaluation sollen die erzielten Ergebnisse kritisch hinterfragt und das Plugin, sowie die Inhaltsmoderation durch Sprachmodelle, entsprechend bewertet werden.  

Während der Bearbeitung dieser Arbeit sollen folgende Fragen beantwortet werden:

1. Wie kann die [OpenAI-API][openai-api] in die [WoltLab Suite][woltlab-suite] integriert werden?  
2. Wie kann eine automatisierte Inhaltsmoderation durch Sprachmodelle implementiert werden und welche Herausforderungen ergeben sich dabei?  
3. Eignen sich Sprachmodelle wie GPT zur automatisierten Moderation von nutzergenerierten Inhalten?  
4. Welche Vor- und Nachteile (auch: Risiken) ergeben sich durch die Verwendung von KI zur automatisierten Moderation von nutzergenerierten Inhalten?  
5. Können Sprachmodelle zur kontextsensitiven Moderation von nutzergenerierten Inhalten verwendet werden?  
6. Welchen Einfluss können Anwender (Nicht-Entwickler) auf die Sprachmodelle bzw. deren Ergebnisse nehmen?  
7. Kann KI die Moderation von nutzergenerierten Inhalten auf längere Sicht vollständig übernehmen und erprobte Maßnahmen und Algorithmen ersetzen?   


## Zeitplan und Meilensteine

**Bearbeitungsdauer:** ~9 Wochen  

**Woche 1-2**
* Beginn der Ausarbeitung  
* Recherche zu den Themen Sprachmodelle, Inhaltsmoderation und WoltLab Suite  
* *(Meilenstein 1)* Konzeption des Plugins und Spezifikation der Anforderungen  

**Woche 3-4**
* Fortführung der Ausarbeitung  
* *(Meilenstein 2)* Entwicklung des Plugins  

**Woche 5-6**
* Fortführung der Ausarbeitung  
* Testing und Fehlerbehebung  
* Fertigstellung des Plugins  
* Dokumentation des Plugins  

**Woche 7-8**
* Fortführung der Ausarbeitung  
* Zusammenfassen der Arbeitsergebnisse  
* *(Meilenstein 3)* Evaluation des Plugins  

**Woche 9**
* Fertigstellung der Ausarbeitung  
* Abgabe der Bachelorarbeit  

## Ausblick

Nach Abschluss der Entwicklung des Plugins ist es denkbar, dieses zur Optimierung der Ergebnisse stetig weiterzuentwickeln und um neue Funktionen, wie beispielsweise der Moderation von weiteren Textinhalten innerhalb der WoltLab Suite, zu erweitern. Potenziell könnten sogar zusätzliche KI-Systeme integriert werden, welche die automatisierte Moderation auch auf andere Inhaltstypen wie Bildinhalte ausweiten können. Außerdem könnte geprüft werden, ob die Ergebnisse zuverlässig genug sind, um die Inhaltsmoderation vollständig zu automatisieren und keine Prüfung durch die Moderation mehr zu erfordern.  

Die Ergebnisse dieser Arbeit können auch als Grundlage für weitere Forschungsarbeiten dienen, um die Inhaltsmoderation durch Sprachmodelle weiter zu erforschen. Im Rahmen einer detaillierteren Evaluation des Plugins oder dessen Funktionsweise unter nachgestellten Bedingungen, können nicht nur weitere Verbesserungen des Plugins identifiziert werden, sondern auch die Ergebnisse dieser Arbeit noch einmal kritisch hinterfragt und bewertet werden. Denkbar wäre auch eine Gegenüberstellung der Ergebnisse verschiedener Sprachmodelle bzw. KI-Systeme, um diese miteinander zu vergleichen.  

Bietet das Plugin genug Potenzial, die Moderation von zumindest textbasierten Inhalten zufriedenstellend zu automatisieren, könnten  auch vergleichbare Lösungen für weitere Plattformen umgesetzt werden.  


[woltlab-suite]: https://www.woltlab.com/
[openai-api]: https://openai.com/blog/openai-api/