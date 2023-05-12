# Exposé "Konzeption und Entwicklung einer automatisierten Lösung zur Generierung von Beschreibungstexten für Wein im E-Commerce Bereich auf Basis strukturierter Produktdaten"

## Kontext

Diese Arbeit entsteht zusammen mit dem externen Partner Gjuce. Gjuce ist eine Webagentur aus Köln, welche sich auf E-Commerce Lösungen mit Shopware spezialisiert hat. Unter anderem betreiben sie Online-Shops im Bereich des Weinhandels und können daher mit Expertise diese Arbeit unterstützen.

## Thema

Durch die Verlagerung des Point-of-Sale (POS) vom stationären Handel hin zum Online-Handel und das damit verbundene Wegfallen der persönlichen Beratung sind für die Informationssuche Beschreibungstexte äußerst relevant. Infolgedessen sind diese ein wichtiger Bestandteil der Kaufentscheidung im E-Commerce Bereich. Hier gilt es, potenzielle Kunden über ein Produkt und ihre Merkmale aufzuklären, um einen Kaufwunsch einzuleiten [^kaufverhalten]. <br>
Je nach Produktklasse werden Beschreibungstexte i.d.R. durch den Shop Betreiber erstellt oder direkt vom Produzenten übernommen. Die Rahmenbedingungen dieser Arbeit ist der Weinhandel, hier gibt es eine weitere Eigenheit: Für das Erstellen von Beschreibungstexten muss ein umfassendes Wissen über die Produkte vorhanden sein, da gewisse Nuancen wie Aroma, Geschmack etc. oftmals nicht trivial sind. Daher wird häufig auf die Texte der Großhändler zurückgegriffen, was wiederum das Problem mit sich bringt, dass viele Oonline-Shops die gleichen oder ähnliche Beschreibungstexte enthalten.

Thema dieser Arbeit ist das automatische Generieren von Beschreibungstexten für Wein im E-Commerce Bereich. Hierfür soll ein vortrainiertes Sprachmodell genutzt werden, welches auf Basis der strukturierten Produktdaten Beschreibungstexte voll-automatisch erstellt. Dementsprechend sollen aktuell verfügbare Sprachmodelle verglichen werden, um ein Geeignetes zu identifizieren. <br>
Die strukturierten Produktdaten werden durch den Großhandel bereitgestellt. Sie bestehen i.d.R. aus einer Beschreibung, einer Analyse sowie gastronomischen Empfehlungen. Die Beschreibung umfasst dann wiederum generelle Informationen über Jahrgang, Region, Rebsorte und Charakteristiken. Innerhalb der Analyse findet man Lagerfähigkeit, Alkoholgehalt, Säuregehalt und Ähnliches. Die gastronomischen Empfehlungen legen dann passende Speisen dar, zu welchem der Wein genossen werden kann [^daten].

Ebenfalls gilt es, durch Experten aus dem Bereich des Weinhandels zu Evaluieren, inwiefern sich die generierten Texte eignen, um Weine zu Beschreiben. Hierfür stellt der externe Partner dieser Arbeit Experten aus der Branche, welche durch Interviews die Texte bewerten sollen. Es besteht die Möglichkeit, Blind-Interviews durchzuführen, um sicherzustellen, dass die Interviews unvoreingenommen durchgeführt werden.

Der Autor geht davon aus, dass verschiedene Nutzergruppen Interesse an einer automatischen Lösung zur Generierung von Beschreibungstexten haben. Hierunter fallen beispielsweise die Shop Betreiber, Entwickler oder Copywriter, also alle Nutzergruppen, welche den Online-Shop initial mit Informationen anreichern müssen. Ebenfalls gehören Marketing Personal und Ähnliche dazu, welche im Laufe der Nutzungsdauer Produkte sowie Texte pflegen. Diese Nutzergruppen werden hier als "Redakteure" zusammengefasst.
Um die Nutzung für ebendiese Redakteure zu ermöglichen, soll ein Plugin für Shopware 6 entstehen. Hier sind zwei Punkte interessant: Wie muss das User Interface gestaltet sein, damit Redakteure effizient Texte Evaluieren, Bewerten und Tunen können? Und wie kann die Generierung für eine Menge von mehreren Hundert Produkten erfolgen?

[^kaufverhalten]: F. Deges, „Kaufprozess und Kaufverhalten im E-Commerce“, in Grundlagen des E-Commerce: Strategien, Modelle, Instrumente, F. Deges, Hrsg., Wiesbaden: Springer Fachmedien, 2020. doi: 10.1007/978-3-658-26320-1_4.
[^daten]: [Beispieldaten zum Comte de Sénéjac](https://www.weinkontor-freund.de/wein/frankreich/chateau.senejac/4033240)

## Forschungsfragen/Zielsetzungen

1. Welches Sprachmodell eignet sich am besten für die automatische Generierung von Beschreibungstexten aus strukturierten Produktmerkmalen?
2. Auf Basis welcher Kriterien lassen sich automatisch generierte Beschreibungstexte Bewerten und gibt es Unterschiede, wenn sich die Zielgruppe ändert?
3. Wie muss UX/UI gestaltet sein, um eine automatische Generierung und Evaluierung der Beschreibungstexte durch einen Redakteur im Shop-Backend effizient durchführen zu können?
4. Wie kann die Generierung und Evaluierung von Beschreibungstexten bei einer Anzahl von mehreren Hundert Produkten effizient durchgeführt werden?

## Gliederung

- Einleitung
  - Kontext
  - Problemstellung
  - Motivation
  - Forschungsfragen
  - Zielsetzung
- Weinhandel im E-Commerce
  - Varianten des Weinhandels
  - E-Commerce Allgemein / Überblick
    - Bedeutung von Beschreibungstexten im E-Commerce
    - Redaktionsprozess bei Beschreibungstexten (oder: Redaktionsprozess bei der Integration von Produkten)
  - Zielgruppen / Stakeholder Identifizieren
- Sprachmodelle und ihre Anwendung (in der Textgenerierung)
  - Aufbau und Funktionsweise von Sprachmodellen
  - Auswahl passender Sprachmodelle
  - Vergleich der Sprachmodelle
  - Prompt Engineering / Tuning
- Implementierung einer automatischen Lösung
  - Shopware und Plugin Ecosystem
  - Vorgehen (oder Prozess, oder Workflow) Aufstellen
    - Onboarding-Prozess
    - Generierungungs-Prozess
    - Bewertungs- / Evaluierungs-Prozess
    - Einpflegen in Produktiv Umgebung
  - Implementierung
- Evaluation und Validierung
  - Kriterien für die Bewertung der Beschreibungstexte aufstellen
  - Bewertung der Textqualität durch Experten
  - Bewertung der UX/UI durch Redakteure
  - Internationalisierung und Lokalisierung
- Beschreibung der automatisierten Lösung
- Fazit
  - Implikationen
  - _(Abstraktion in andere Branchen (zu Ambitioniert?))_
  - Ausblick

## Forschungsstand

Durch den aktuellen Fokus auf KI-gestütze Produktergänzungen gibt es eine Reihe an Unternehmen, welche an eigenen Sprachmodellen (Large Language Models - LLM) arbeiten. Die [Themenfeldanalyse](./01-resarch-area-analysis/Themenfeldanalyse.pdf) gibt hier einen Überblick von einigen Sprachmodellen die bei einer ersten Recherche aufgetreten sind. Die Aktuell am meisten genannten sind sicherlich OpenAI mit ChatGPT (v3.5 & v4) sowie Google mit Bert.

**Referenzen:**

- [OpenaAi - ChatGPT](https://openai.com/blog/chatgpt)
- [OpenAi - GPT4](https://openai.com/product/gpt-4)
- [Google - BERT](https://ai.googleblog.com/2018/11/open-sourcing-bert-state-of-art-pre.html)
- [Google - Flan-T5-XXL](https://huggingface.co/google/flan-t5-xxl)
- [Stanford - How Large Language Models Will Transform Science, Society, and AI](https://hai.stanford.edu/news/how-large-language-models-will-transform-science-society-and-ai)
- [Christopher D. Manning - Human Language Understanding & Reasoning](https://www.amacad.org/publication/human-language-understanding-reasoning)
- [Current Approaches and Applications in Natural Language Processing](https://www.mdpi.com/books/book/5892)

Der Themenbereich Sprachmodelle bzw. Large Language Models gibt innerhalb der [DigiBib](https://thb-koeln.digibib.net/search/eds/list?start=1&be-eds-expander=fulltext&parent_request_id=002pdinqolclk6o2vleg&parent_request_id_hmac=ea48c26539de621a6e235820151356e977b66b70&q-al=large+language+models&be-eds-sort=relevance) sowie Google-Scholar Suche mehrere Millionen Treffer. Hier gilt es dementsprechend stark Einzugrenzen.

**Genutze Suchbegriffe:**

- Large Language Models
- Language Models
- Sprachmodelle
- pre-trained language model

Im Bereich der Produktbeschreibung bzw. Beschreibungstexten ist in der ersten Orientierung aufgefallen, dass hier viel im Kontext der Search Engine Optimization (SEO) angesiedelt ist. Da das Thema SEO kein Fokus dieser Arbeit sein soll, muss davon ausgegangen werden, dass es deutlich aufwendiger wird, geeignete Referenzen zu finden.

## Deutsche Wein-Shops mit hochwertigen Weinbeschreibungen

- [Wein Plus](https://www.wein.plus/de)
- [Gute Weine](https://www.gute-weine.de/)
- [Wein am Limit](https://shop.weinamlimit.de/)
- [Baum Selection](https://baumselection.com/)
- [Tesdorpf](https://www.tesdorpf.de/)

## Zeitplan

tbd
