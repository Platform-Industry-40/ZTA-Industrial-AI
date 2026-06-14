
# Zusammenhang KI-VO / KI-MIG und Kritische Infrastrukturen – Kurzfassung

## Kernantwort

**Ja, es gibt einen sehr engen Zusammenhang.** KI-Systeme in kritischen Infrastrukturen sind in der KI-VO als **Hochrisiko-KI-Systeme** eingestuft (Anhang III Nr. 2). Aber: Die KI-VO regelt nur die **Produktsicherheit** des KI-Systems, nicht die **Betriebssicherheit** der Infrastruktur. Für die Verfügbarkeit der KI-Leistungen in kritischen Systemen ist ein **Mehr-Regime-System** zuständig.

---

## Tabelle 1: KI in kritischer Infrastruktur = Hochrisiko

| Merkmal | Ausprägung |
|---|---|
| **Rechtsgrundlage** | Anhang III Nr. 2 KI-VO |
| **Definition** | KI-Systeme als Sicherheitsbauteile in kritischer digitaler Infrastruktur, Straßenverkehr, Wasser-, Gas-, Wärme- oder Stromversorgung |
| **Begriffsbasis** | Verweis auf Art. 2 Nr. 4 CER-Richtlinie (nicht §2 Abs. 10 BSIG!) |
| **Ausnahme** | Reine Cybersicherheits-Tools (Firewalls, SIEM, Virenscanner) |
| **Registrierung** | Ausnahme von der EU-Datenbank-Registrierung (aus Sicherheitsgründen) |
| **Konformitätsbewertung** | Pflicht (Art. 43 KI-VO) |
| **CE-Kennzeichnung** | Pflicht (Art. 48 KI-VO) |

---

## Tabelle 2: Wer ist für was zuständig?

| Aufgabe | Zuständigkeit | Rechtsgrundlage |
|---|---|---|
| **Produktsicherheit des KI-Systems** (Konformität, CE, Risikomanagement, Dokumentation) | **BNetzA** (KI-MIG §2 Abs. 1) | KI-VO / KI-MIG |
| **Cybersicherheit des KI-Produkts** (Schwachstellen, Updates) | **Noch zu benennen** (CRA-Behörde) / übergangsweise **BSI** | CRA (VO 2024/2847) |
| **Betriebssicherheit der Infrastruktur** (Verfügbarkeit, Resilienz, Incident-Reporting) | **BSI** (NIS2-Aufsicht) | NIS2 / Kritis-Dachgesetz / BSIG |
| **Sektorale Aufsicht** (Netzstabilität, Versorgungssicherheit) | **BNetzA** (EnWG) / Landesbehörden / KBA etc. | Sektorales Recht (EnWG, etc.) |
| **Funktionale Sicherheit** (Safety, SIL) | **Notifizierte Stellen / TÜV** | EN 61508 etc. |

---

## Tabelle 3: Die zentrale Lücke im KI-MIG

| Was geregelt ist | Was NICHT geregelt ist |
|---|---|
| §10 KI-MIG: Zusammenarbeit KI-Marktüberwachung ↔ CRA-Behörde | **Keine explizite Zusammenarbeit KI-Marktüberwachung ↔ BSI (NIS2)** |
| §9 KI-MIG: Allgemeine Kooperation mit BSI | **Keine Informationspflicht bei Verdachtsfällen in kritischer Infrastruktur** |
| BNetzA als generelle Marktüberwachungsbehörde | **Keine klare Zuordnung, wer bei Ausfall eines KI-Systems in kritischer Infrastruktur die Einsatzleitung hat** |

---

## Fazit in einem Satz

> Die KI-VO/KI-MIG reguliert KI-Systeme in kritischen Infrastrukturen als Hochrisiko-Produkte, aber die **Verfügbarkeit der KI-Leistungen** wird durch ein **Parallelregime** sichergestellt: **NIS2/BSIG** für die Betriebssicherheit der Infrastruktur, **CRA** für die Cybersicherheit der Produkte, und **sektorale Aufsicht** für die Versorgungssicherheit – mit einer **fehlenden expliziten Schnittstelle** zwischen KI-Marktüberwachung und NIS2-Aufsicht im KI-MIG-Entwurf.
