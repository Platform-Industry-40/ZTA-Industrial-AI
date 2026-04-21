# 9	Anhang 2: Proof of Concept – LLM-gestützte ABAC-Regelgenerierung (Referenz-Repository)

Der vollständige Proof of Concept zur Machbarkeit des LLM-gestützten Betriebs einer Zero Trust Architecture mit ABAC-Regelgenerierung liegt im öffentlichen GitHub-Repository unter [**Anhang 2**](https://github.com/Platform-Industry-40/ZTA-Industrial-AI/tree/main/doc/de/apx/Anhang%202) (Stand: April 2026). Dokumentiert sind alle Prompts, LLM-Antworten und Zwischenergebnisse der einzelnen Prozessschritte – vollständig nachvollziehbar und reproduzierbar.

## 9.1 Iterativer 4-Schritte-Ansatz

Der POC folgt einem strukturierten, LLM-agnostischen Ansatz zur Überwindung struktureller LLM-Hindernisse (Halluzinationen, Silent Truncation, Seed-Varianz u. a.):

- **Schritt 1.1** – Strukturierte Datenerhebung: Mehrfachbefragung verschiedener LLMs ohne Kontext, erzwungenes JSON-Ausgabeformat mit Traceability-Feldern
- **Schritt 1.3** – Deterministische Aggregation: Konsolidierung der Rohantworten mit expliziter Darstellung von Gemeinsamkeiten und gewichteten Abweichungen
- **Schritt 2** – Anforderungsgenerierung: Architekturunabhängige, normreferenzierte Security Requirements
- **Schritt 3** – Code-Generierung: Ausführbarer ZTA-Code für verschiedene Laufzeitumgebungen

Die vollständige Methodenbeschreibung einschließlich Hindernisse und Lösungsstrategien ist in [Scope.md](https://github.com/Platform-Industry-40/ZTA-Industrial-AI/tree/main/doc/de/apx/Anhang%202/Scope.md) dokumentiert.

## 9.2 Zwei Use Cases

**Use Case 1 – SAP** ([1 SAP/](https://github.com/Platform-Industry-40/ZTA-Industrial-AI/tree/main/doc/de/apx/Anhang%202/1%20SAP)): Generierung von ABAC-Regeln für den sicherheitskritischen SAP-Funktionsbaustein `BAPI_USER_GET_DETAIL`. Gewählt als Vorbereitungs-Use-Case aufgrund verfügbaren Domänenwissens für die Verifikation. Ergebnis: ausführbarer Code in XACML, Python und ABAP.

**Use Case 2 – Industrie 4.0** ([2 I40/](https://github.com/Platform-Industry-40/ZTA-Industrial-AI/tree/main/doc/de/apx/Anhang%202/2%20I40)): Generierung von ABAC-Regeln für eine multinationale Kollaborationsplattform eines EU-ansässigen Robotik-Herstellers unter Berücksichtigung dynamischer Import-/Export- und Datenschutzregulierungen. Erweiterung um einen zweiten Ergebnispfad: Management- und Legal-Report aus denselben Quelldaten. Ergebnis: ausführbarer Code in XACML und C++ sowie ein PDF-Report.

## 9.3 Empfohlener Einstieg

- Einstieg: [README.md](https://github.com/Platform-Industry-40/ZTA-Industrial-AI/tree/main/doc/de/apx/Anhang%202/README.md) – Überblick, Hauptergebnisse und Lesereihenfolge
- Methodik: [Scope.md](https://github.com/Platform-Industry-40/ZTA-Industrial-AI/tree/main/doc/de/apx/Anhang%202/Scope.md) – iterativer Ansatz, Hindernisse, Lösungsstrategien
- Use Case SAP: [1 SAP/README.md](https://github.com/Platform-Industry-40/ZTA-Industrial-AI/tree/main/doc/de/apx/Anhang%202/1%20SAP/README.md)
- Use Case I40: [2 I40/README.md](https://github.com/Platform-Industry-40/ZTA-Industrial-AI/tree/main/doc/de/apx/Anhang%202/2%20I40/README.md)

---


