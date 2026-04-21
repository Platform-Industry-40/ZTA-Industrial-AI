# Proof of Concept: LLM-gestützte ABAC-Regelgenerierung für Zero Trust Architectures

## Thema
Machbarkeitsnachweis für den Einsatz von Large Language Models (LLMs) zur automatisierten Generierung von Attribute-Based Access Control (ABAC)-Regeln in Zero Trust Architectures (ZTA) – exemplarisch für zwei Sicherheitsdomänen.

## Motivation
Die Frage, ob heutige General Purpose AI bzw. LLMs zuverlässig zur Verwaltung von ABAC-Regeln in sicherheitskritischen ZTA-Umgebungen eingesetzt werden können, ist nicht trivial. LLMs bringen strukturelle Hindernisse mit – von Halluzinationen über Silent Truncation bis zu Seed-Varianz –, die in Sicherheitskontexten nicht tolerierbar sind. Dieser POC untersucht systematisch, ob und wie diese Hindernisse durch einen iterativen, LLM-agnostischen Ansatz überwunden werden können, und liefert dazu konkrete, reproduzierbare Ergebnisse für zwei Anwendungsdomänen.

## Hauptmessages
- LLM-typische Hindernisse (Halluzinationen, Silent Truncation, Seed-Varianz u. a.) sind durch einen iterativen, schrittweisen Ansatz mit kleinen Prompts beherrschbar.
- Der Ansatz ist LLM-agnostisch: Prompts wurden gegen GPT, Gemini, Grok, DeepSeek, Mistral, Amazon Nova und Claude getestet.
- Traceability-Anforderungen (EU AI Act) werden durch lückenlose Protokollierung jedes Schritts erfüllt.
- Für beide Use Cases (SAP, Industrie 4.0) konnte ausführbarer ZTA-Code generiert werden (XACML, C++, Python, ABAP).
- Ein Domain Expert als „Human in the Loop" bleibt in jedem Schritt zwingend erforderlich.
- Alle Ergebnisse sind als Näherungslösung zu verstehen (**Approximation approach only**).

## Dokumente und Ordner
- [1 SAP/](./1%20SAP/)  ← Use Case 1: ABAC-Regelgenerierung für SAP S/4HANA
- [2 I40/](./2%20I40/)  ← Use Case 2: ABAC-Regelgenerierung für Industrie-4.0-Kollaborationsplattform
- [Scope.md](./Scope.md)  ← Iterativer Ansatz, Schrittstruktur und LLM-Hindernisse im Detail
- [Abstract.md](./Abstract.md)  ← Übergeordnetes Abstract des Anhangs 2

## Scope-Hinweis
Der POC folgt einem strukturierten 4-Schritte-Ansatz (Datenerhebung → Validierung → Aggregation → Anforderungen → Code). Jeder Schritt ist durch Prompts und LLM-Antworten dokumentiert. Die vollständige Methodik, die Hindernisse und deren Lösungsstrategien sind in [Scope.md](./Scope.md) beschrieben.

## Empfohlene Lesereihenfolge
1. Abstract.md (Zusammenfassung und Einordnung)
2. Scope.md (Methodik, Hindernisse, Lösungsstrategien)
3. 1 SAP/README.md (Use Case SAP – Beschreibung und Ergebnisse)
4. 2 I40/README.md (Use Case I40 – Beschreibung und Ergebnisse)
5. Einzelne Step-Ordner nach Bedarf (Prompts und LLM-Antworten)

## Verbindung zum Gesamtprojekt ZTA+KI_2026
Dieser Anhang liefert den empirischen Machbarkeitsnachweis für das Gesamtprojekt. Er zeigt, dass LLM-gestützte ZTA-Compliance unter kontrollierten Bedingungen funktioniert, und begründet damit die methodischen Entscheidungen in Anhang 1 (Compliance-Dokumentation) und Anhang 3 (KI-Modelle).
