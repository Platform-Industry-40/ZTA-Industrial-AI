# 8	Anhang 1: Detaillierte Umsetzungs- und Evaluierungsstruktur (Referenz-Repository)

Die vollständige, auditierbare und aktuell gepflegte Dokumentation zur Implementierung einer **Zero Trust Architektur (ZTA) mit KI-Assistenz** im Industrie-4.0-Kontext liegt im öffentlichen GitHub-Repository:

[**Anhang 1: Detaillierte Umsetzungs- und Evaluierungsstruktur (Referenz-Repository)**](https://github.com/Platform-Industry-40/ZTA-Industrial-AI/edit/main/doc/de/08%20Anhang%201%20%20Detaillierte%20Umsetzungs-%20und%20Evaluierungsstruktur%20(Referenz-Repository).md)) (Stand: April 2026)

Dieses Repository enthält alle relevanten Dokumente in Markdown-Format, inklusive interaktiver Diagramme (Mermaid), vollständiger Tabellen, Evidenz-Nachweisen und Versionshistorie. Es dient als lebendige Ergänzung zu diesem Word-Dokument und wird fortlaufend aktualisiert.

## 8.1 Dreistufige Struktur - Warum, Was, Wie

Die gesamte Dokumentation folgt einer klaren, dreistufigen Logik:

- **Governance-Ebene** (das „Warum") Strategische Leitlinien, Begründung, Risikoklassifizierung, Rollen/RACI, menschliche Aufsicht, Lebenszyklus-Betrachtung → Haupt-Dokument: [Data-\_und_AI-Governance.md](https://github.com/artkeller/Plattform_Industrie_4.0/blob/main/ZTA%2BKI_2026/Compliance/V2/Data-_und_AI-Governance.md)
- **Policy-Ebene** (das „Was") Verbindliche Prinzipien für Zugriffssteuerung, Integrität, Nachvollziehbarkeit, kontinuierliche Überwachung → Haupt-Dokument: [Policy.md](https://github.com/artkeller/Plattform_Industrie_4.0/blob/main/ZTA%2BKI_2026/Compliance/V2/Policy.md)
- **Modul-/Prüf-Ebene** (das „Wie") Konkrete Anforderungen, Prüfschritte und attributgenaue Verifikationspunkte
  - [Modul_ZTA_Teil_1.md](https://github.com/artkeller/Plattform_Industrie_4.0/blob/main/ZTA%2BKI_2026/Compliance/V2/Modul_ZTA_Teil_1.md) - Generischer Katalog (ZTA-01 bis ZTA-15)
  - [Modul_ZTA_Teil_2.md](https://github.com/artkeller/Plattform_Industrie_4.0/blob/main/ZTA%2BKI_2026/Compliance/V2/Modul_ZTA_Teil_2.md) - Prüfschritte (aktuell nur ZTA-01)
  - [Modul_ZTA_Teil_3.md](https://github.com/artkeller/Plattform_Industrie_4.0/blob/main/ZTA%2BKI_2026/Compliance/V2/Modul_ZTA_Teil_3.md) - Granulare Verifikation (aktuell nur ZTA-01-001)

Zentrales Mapping-Dokument (für Zertifizierung / Audits): → [SoA.md](https://github.com/artkeller/Plattform_Industrie_4.0/blob/main/ZTA%2BKI_2026/Compliance/V2/SoA.md) (Statement of Applicability mit allen 38 Controls aus ISO/IEC 42001 Annex A + IEC 62443 SRs)

## 8.2 Warum GitHub statt reiner Word-Anhänge?

- **Aktuelle Version immer verfügbar**
- **Vollständige Nachverfolgbarkeit**
- **Interaktive Elemente**
- **Einfache Kollaboration**
- **Auditfähigkeit** reproduzierbar

## 8.3 Empfohlener Einstieg (3 Minuten)

- Verzeichnis:<https://github.com/artkeller/Plattform_Industrie_4.0/tree/main/ZTA%2BKI_2026/Compliance/V2>

- Start mit der **Governance** → [Data-\_und_AI-Governance.md](https://github.com/artkeller/Plattform_Industrie_4.0/blob/main/ZTA%2BKI_2026/Compliance/V2/Data-_und_AI-Governance.md) (strategische Übersicht, Rollen, Risiko-Klassifizierung)
- Weiter zur **Policy** → [Policy.md](https://github.com/artkeller/Plattform_Industrie_4.0/blob/main/ZTA%2BKI_2026/Compliance/V2/Policy.md) (verbindliche Prinzipien und Tabellen)
- Vertiefung in die **Module** → Beginn mit [Modul_ZTA_Teil_1.md](https://github.com/artkeller/Plattform_Industrie_4.0/blob/main/ZTA%2BKI_2026/Compliance/V2/Modul_ZTA_Teil_1.md) (vollständiger Anforderungskatalog + SoA-Mapping)
- Für Audits & Nachweise → [SoA.md](https://github.com/artkeller/Plattform_Industrie_4.0/blob/main/ZTA%2BKI_2026/Compliance/V2/SoA.md)

Alle Dokumente sind so gestaltet, dass sie **selbstständig lesbar** sind, aber zusammen das vollständige Bild ergeben.
