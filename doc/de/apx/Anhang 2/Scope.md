# Scope

## LLM-Hindernisse im Sicherheitskontext

Der direkte Einsatz von LLMs in sicherheitskritischen ZTA-Umgebungen scheitert an einer Reihe struktureller Hindernisse. Die folgende Liste ist nicht abschließend:

- **Reproduzierbarkeit maschinenlesbarer Ausgaben:** Strukturierte Ausgaben (JSON, XML) werden nicht zuverlässig geliefert und müssen durch gezieltes Prompting erzwungen werden.
- **Halluzinationen:** In Sicherheitskontexten nicht tolerierbar; müssen durch Prompting und Human-in-the-Loop auf ein Minimum reduziert werden.
- **Silent Truncation:** Unbemerkte Auslassungen von Ausgaben; kritisch in sicherheitsrelevanten Antworten.
- **Token-Drop-Effekte:** Auftreten besonders bei langen Dokumenten oder Ressourcenkonflikten.
- **Seed-Varianz:** Statistische Variation der Antworten durch unterschiedliche Startpunkte der Inferenz.
- **Mixture-of-Experts-Optimierungseffekte:** Variante Antworten durch unterschiedliche Expertenaktivierung.
- **Silent Arbitration, Instruction Drift, Attention Erosion, Lost in the Middle:** Weitere Effekte, die zu ungenauen oder inkonsistenten Antworten führen.
- **Semantische Fähigkeiten:** Im Rahmen dieses POC nicht untersucht; siehe Anhang 3 (KI-Modelle/Semantik).

## Der iterative 4-Schritte-Ansatz

Als Antwort auf diese Hindernisse wurde ein strukturierter Ansatz entwickelt:

**Schritt 1.1 – Datenerhebung:**
Die Sicherheitsfrage wird mehrfach, ohne vorherigen Kontext, an denselben LLM sowie an verschiedene LLMs und Versionen gestellt. Prompts sind so optimiert, dass alle LLMs dasselbe Ausgabeformat erzeugen.

**Schritt 1.2 – Validierung:**
Ein Domain Expert prüft die Antworten auf Korrektheit und KI-Fehler. Dieser Schritt ist zwingend manuell.

**Schritt 1.3 – Aggregation:**
Die validierten Antwort-Datensätze werden aggregiert: Gemeinsamkeiten und Abweichungen werden explizit erhalten. Abschließend erfolgt eine KI-gestützte Risikobewertung als Grundlage für die ZTA-Maßnahmen.

**Schritt 2 – Anforderungsgenerierung:**
Aus den aggregierten Daten werden architekturunabhängige, menschenlesbare Sicherheitsanforderungen im Format von Security Controls generiert. Noch kein ausführbarer Code.

**Schritt 3 – Code-Generierung:**
Aus den Anforderungen wird ausführbarer Code generiert (XACML, C++, Python, ABAP) – angepasst an die jeweilige ZTA-Architektur.

**Schritt 4 – Qualitätssicherung:**
Ein Domain Expert bewertet das Ergebnis und führt Tests mit dem Ziel des produktiven Einsatzes durch.

## Lösungsstrategien

**Durch iterativen, schrittweisen Ansatz mit kleinen Prompts:**
- Silent Truncation und Token-Drop werden minimiert, da kleine Prompts diese Effekte deutlich reduzieren.
- Jeder Schritt ist separat protokollierbar (LLM-Typ, Version, Zeitstempel, Ausgabe) – Traceability-Anforderungen des EU AI Act werden erfüllt.

**Durch kontextfreie Wiederholung desselben Prompts:**
- Seed-Varianz wird durch Aggregation mehrerer Antworten gemindert.
- Biasing-Effekte werden durch Nutzung verschiedener LLMs reduziert (Vendor-Lock-in-Vermeidung).
- Kontexteffekte werden durch jeweils neue Sessions ohne Vorgeschichte eliminiert.
- **Empfehlung:** Mindestens 3 Wiederholungen pro LLM × 3 verschiedene LLMs.

**Durch spezialisiertes Prompting:**
- Maschinenlesbare Ausgaben werden durch explizite Strukturvorgaben mit Beispieldaten und Ausgabeverbot für Freitext erzwungen.
- Aggregation in Schritt 1.3 nutzt Direktiven wie *verbatim*, *greedy* oder *temperature=0* sowie explizite Abfrage von Gemeinsamkeiten und Abweichungen.
- Halluzinationen werden durch explizites Verbot und ein dediziertes Bool-Attribut für unbekannte Inhalte adressiert.

## Use Cases und Ordnerstruktur

Alle Ergebnisse (Prompts und LLM-Antworten) sind für die Schritte 1.1, 1.3, 2 und 3 in den folgenden Ordnern dokumentiert:

**Use Case 1 – SAP ([1 SAP/](./1%20SAP/)):**
Generierung von ABAC-Regeln für SAP-S/4HANA-Objekte (Transaktionen, Reports, Function Modules) als ausführbaren Code für eine ZTA-Laufzeitumgebung. Gewählt als Vorbereitungs-Use-Case, da Domänenwissen für die Validierung verfügbar war.

**Use Case 2 – Industrie 4.0 ([2 I40/](./2%20I40/)):**
Generierung von ABAC-Regeln für eine multinationale Industrie-4.0-Kollaborationsplattform unter Berücksichtigung dynamischer Import-/Export- und Datenschutzregulierungen. Erweiterung um Management- und Legal-Reports aus denselben Quelldaten.

Pro Use Case enthält jeder Step-Ordner den LLM-agnostischen Prompt sowie die Antworten von verschiedenen LLM-Anbietern und -Versionen.
