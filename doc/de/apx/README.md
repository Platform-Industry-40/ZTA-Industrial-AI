# Anhänge – ZTA+KI_2026

## Kontext und Zweck

Die drei Anhänge in diesem Verzeichnis sind Bestandteil des Hauptdokuments
**„ZTA+KI_2026"**, das als geschlossenes PDF auf der Plattform Industrie 4.0
veröffentlicht wird. Da die Anhänge in ihrer Tiefe und ihrem Umfang jeweils
ein eigenständiges Dokument rechtfertigen würden, wurde entschieden, sie nicht
nur als Verweis im Hauptdokument zu führen, sondern vollständig als Markdown
im GitHub-Repository bereitzustellen – zur freien Nachnutzung, Weiterentwicklung
und Versionierung.

Jeder Anhang beleuchtet einen der drei zentralen Teilaspekte des Gesamtthemas,
die im Hauptdokument motiviert und eingeführt, hier aber in der notwendigen
Tiefe ausgearbeitet werden.

## Die drei Anhänge

### [Anhang 1 – Compliance-Dokumentation](./Anhang%201/)
Auditfähige Compliance-Vorlagen für den kombinierten Einsatz von Zero Trust
Architecture (ZTA) und KI in Industrie-4.0-Umgebungen. Enthält
Governance-Rahmenwerk, Policy, einen dreistufigen Anforderungskatalog
(ZTA-01 bis ZTA-15) sowie ein vollständiges Statement of Applicability (SoA)
mit Mapping aller 38 ISO/IEC 42001 Annex-A-Controls. Konzipiert für C-Level,
Legal, CISO und Auditoren – nahe 10/10 Audit-Reife.

### [Anhang 2 – Proof of Concept](./Anhang%202/)
Empirischer Machbarkeitsnachweis für den LLM-gestützten Betrieb einer ZTA
mit ABAC-Regelgenerierung. Dokumentiert einen iterativen, LLM-agnostischen
4-Schritte-Ansatz zur Überwindung struktureller LLM-Hindernisse (Halluzinationen,
Silent Truncation, Seed-Varianz u. a.) – mit vollständigen Prompts und
LLM-Antworten für zwei Use Cases: SAP-Sicherheit und eine multinationale
Industrie-4.0-Kollaborationsplattform.

### [Anhang 3 – KI-Modelle](./Anhang%203/)
Technische und theoretische Grundlage für alle Architektur-, Sicherheits- und
Compliance-Entscheidungen im Projekt. Bündelt sechs komplementäre Perspektiven
auf KI-Modelle: Semantik, Attention-Erosion, SLM, MoE, KI-Datenblatt und
KI-Fingerprint – und zeigt, warum reine KI-Modelle weder Bedeutung noch
Vertrauen allein tragen können.

## Beziehung der Anhänge zueinander

Die drei Anhänge sind nicht unabhängig, sondern aufeinander aufbauend konzipiert:

**Anhang 3** legt die theoretisch-technische Basis: Er erklärt, was KI-Modelle
leisten können und wo ihre fundamentalen Grenzen liegen. Dieses Verständnis
ist Voraussetzung für einen verantwortungsvollen Einsatz in
sicherheitskritischen Systemen.

**Anhang 2** überführt dieses Verständnis in die Praxis: Der POC zeigt empirisch,
unter welchen methodischen Bedingungen LLMs dennoch zuverlässig in ZTA-Kontexten
eingesetzt werden können – und dokumentiert die dabei gefundenen Lösungsstrategien.

**Anhang 1** zieht die normativen Konsequenzen: Die Compliance-Dokumentation
setzt voraus, dass die Grenzen der KI bekannt (Anhang 3) und die methodischen
Voraussetzungen für ihren Einsatz nachgewiesen sind (Anhang 2).

## Empfohlene Lesereihenfolge

Für den **Einstieg über das Hauptdokument** folgt man dessen Verweisen – die
Anhänge vertiefen jeweils den dort eingeführten Gedanken.

Wer die Anhänge **eigenständig** liest, empfiehlt sich folgende Reihenfolge:

1. Anhang 3 (theoretische Basis)
2. Anhang 2 (empirischer Nachweis)
3. Anhang 1 (normative Umsetzung)

## Veröffentlichung

Das Hauptdokument erscheint als PDF auf der
[Plattform Industrie 4.0](https://www.plattform-i40.de).
Dieses Repository stellt die Anhänge ergänzend als versioniertes Markdown
zur Verfügung.
