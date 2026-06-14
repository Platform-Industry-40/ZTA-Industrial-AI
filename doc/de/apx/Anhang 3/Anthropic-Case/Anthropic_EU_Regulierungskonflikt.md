
# Anthropic Fable 5 / Mythos 5 – US-Exportkontrolle und EU-Regulierungskonflikt

## 1. Die Faktenlage (Stand: 12.–13. Juni 2026)

### Was ist passiert?

Am **12. Juni 2026 um 17:21 Uhr ET** (23:21 Uhr MEZ) erhielt Anthropic eine direktive der US-Regierung (Commerce Secretary Howard Lutnick, Bureau of Industry and Security) mit folgendem Inhalt:

> **Sofortige Suspendierung des Zugangs zu Fable 5 und Mythos 5 für sämtliche ausländische Staatsangehörige** – unabhängig davon, ob sie sich innerhalb oder außerhalb der USA befinden, einschließlich ausländischer Anthropic-Mitarbeiter.

Anthropic musste daraufhin **beide Modelle für ALLE Kunden global abschalten**, da eine Filterung nach Staatsangehörigkeit technisch nicht möglich war.

### Begründung der US-Regierung

- Verdacht eines **„Jailbreaks"** (Sicherheitsumgehung) bei Fable 5
- Die Fähigkeit, Software-Schwachstellen zu identifizieren, könnte von nicht-US-Staatsangehörigen für Cyberangriffe missbraucht werden
- **„National security"** als Rechtfertigung nach Exportkontrollvorschriften

### Anthropics Position

- Die Regierung lieferte nur **„verbale Evidenz"** eines „potenziellen, engen, nicht-universellen Jailbreaks"
- Die demonstrierte Fähigkeit sei bei **OpenAI GPT-5.5** bereits verfügbar
- Kein universeller Jailbreak gefunden
- Die Maßnahme verstoße gegen die Prinzipien von **Transparenz, Fairness, Klarheit und technischen Fakten**
- Wenn dieser Standard branchenweit angewendet würde, würde dies **„im Wesentlichen alle neuen Modelle aller Frontier-Provider stoppen"

---

## 2. Der EU-Regulierungskonflikt: Eine systemische Analyse

### 2.1 Die „One-Vendor-Politik" ist nicht mehr möglich

| Aspekt | Vor dem 12.06.2026 | Nach dem 12.06.2026 |
|---|---|---|
| **Annahme** | US-Cloud-/KI-Dienste sind zuverlässig verfügbar | US-Regierung kann jederzeit Zugang unterbrechen |
| **Risiko** | Gering (technisch/betriebswirtschaftlich) | **Existenzielles politisches Risiko** |
| **Planbarkeit** | Gegeben | Nicht gegeben – ad-hoc-Entscheidungen ohne Vorankündigung |
| **Rechtsschutz** | Vertragsrecht | Kein effektiver Rechtsschutz gegen Exportkontroll-Entscheidungen |

### 2.2 Konfliktpunkte mit EU-Recht

#### A. KI-Verordnung (VO 2024/1689) – Art. 26 (Pflichten des Betreibers)

Art. 26 Abs. 1 KI-VO verpflichtet Betreiber von Hochrisiko-KI-Systemen zur:
- **Eingriffsmöglichkeit** (Art. 26 Abs. 1 lit. a)
- **Überwachung des Betriebs** (Art. 26 Abs. 1 lit. b)
- **Aufbewahrung von Protokollen** (Art. 26 Abs. 1 lit. c)

**Konflikt:** Wenn der US-Anbieter den Dienst abrupt einstellt, kann der Betreiber seine Pflichten nicht mehr erfüllen. Die KI-VO geht von **Verfügbarkeit** aus, nicht von **willkürlicher Unterbrechung durch Drittstaaten**.

#### B. KI-Verordnung – Art. 9 (Risikomanagement)

Art. 9 KI-VO verlangt ein kontinuierliches Risikomanagement über den gesamten Lebenszyklus.

**Konflikt:** Ein plötzlicher, staatlich angeordneter Dienstausfall durch einen Drittstaat ist **kein beherrschbares Risiko** im Sinne des Risikomanagementsystems. Es handelt sich um ein **exogenes politisches Risiko**, das weder vom Anbieter noch vom Betreiber vorhersehbar oder steuerbar ist.

#### C. NIS2-Richtlinie (RL 2022/2555) – Art. 21 (Risikomanagement)

NIS2 verpflichtet „wesentliche Einrichtungen" und „wichtige Einrichtungen" zu:
- **Geschäftskontinuitätsmanagement**
- **Krisenreaktionsplänen**
- **Redundanz und Resilienz**

**Konflikt:** Eine One-Vendor-Politik mit einem US-Anbieter, der jederzeit abgeschaltet werden kann, widerspricht dem **Resilienzgebot** der NIS2. Die Richtlinie impliziert – ohne es explizit zu sagen – dass **Drittstaaten-Risiken** bei der Lieferantenauswahl berücksichtigt werden müssen.

#### D. DSGVO – Art. 32 (Sicherheit der Verarbeitung)

Art. 32 DSGVO verlangt angemessene technische und organisatorische Maßnahmen zum Schutz personenbezogener Daten.

**Konflikt:** Ein plötzlicher Dienstausfall kann die **Verfügbarkeit von Daten** und die **Integrität von Verarbeitungsprozessen** gefährden. Wenn ein KI-System personenbezogene Daten verarbeitet und abrupt abgeschaltet wird, besteht das Risiko von Datenverlust oder -korruption.

#### E. Digitale Operational Resilience Act (DORA) – für Finanzsektor

DORA verpflichtet Finanzunternehmen zu:
- **ICT-Risikomanagement**
- **Konzentrationsrisiken bei Drittanbietern**
- **Exit-Plänen**

**Konflikt:** Die Abhängigkeit von einem einzigen US-KI-Anbieter stellt ein **Konzentrationsrisiko** dar, das unter DORA explizit adressiert werden muss.

---

## 3. Kritische Infrastrukturen: Der unbedachte Fall

### 3.1 Was passiert, wenn ein KI-System in kritischer Infrastruktur abrupt ausfällt?

**Szenario:** Ein europäisches Stromversorgungsunternehmen nutzt Anthropic Fable 5 für:
- Lastprognosen
- Netzstabilitätsanalysen
- Störfall-Erkennung

**Fall:** US-Regierung schaltet Fable 5 ab.

| Folge | Auswirkung |
|---|---|
| **Keine Lastprognosen** | Netzinstabilität, möglicherweise Blackouts |
| **Keine Störfall-Erkennung** | Verzögerte Reaktion auf Ausfälle |
| **Datenverlust** | Historische Trainingsdaten nicht mehr zugänglich |
| **Compliance-Verstoß** | Nicht-Erfüllung der Versorgungssicherheitspflichten (EnWG) |
| **NIS2-Verstoß** | Nicht-Erfüllung der Resilienzanforderungen |

### 3.2 Wer ist zuständig?

| Regulierungsebene | Zuständige Behörde | Was sie prüft |
|---|---|---|
| **KI-VO (Produktsicherheit)** | BNetzA | War das KI-System konform? |
| **NIS2 (Betriebssicherheit)** | BSI | War die Infrastruktur resilient? |
| **EnWG (Versorgungssicherheit)** | BNetzA | Wurde die Stromversorgung gefährdet? |
| **DSGVO (Datenschutz)** | Datenschutzbehörden | Gab es Datenverluste? |

**Das Problem:** Keine dieser Behörden hat eine **vorgelagerte Präventionspflicht**, die besagt: „Du darfst dich nicht von einem Anbieter abhängig machen, der jederzeit abgeschaltet werden kann."

---

## 4. Die regulatorische Lücke: Was wurde nicht bedacht?

### 4.1 Fehlende EU-weite Regelung

| Was fehlt | Warum es wichtig wäre |
|---|---|
| **Souveränitätsprüfung bei KI-Beschaffung** | Pflicht zur Prüfung, ob der Anbieter einem Drittstaat unterliegt, der Dienste willkürlich unterbrechen kann |
| **Redundanzgebot** | Pflicht zur Nutzung mehrerer Anbieter (Multi-Cloud/Multi-Model) |
| **Exit-Plan-Pflicht** | Pflicht zu einem Plan für den Fall der Dienstunterbrechung durch Drittstaaten |
| **Notifizierungspflicht** | Pflicht, die zuständige Behörde zu informieren, wenn ein KI-Dienst in kritischer Infrastruktur abgeschaltet wird |
| **Haftungsregelung** | Wer haftet für Schäden durch staatlich angeordnete Dienstunterbrechungen? |

### 4.2 Fehlende nationale Regelung im KI-MIG

Der KI-MIG-Entwurf regelt:
- Marktüberwachung der KI-Systeme (§2)
- Bußgelder bei Nichtkonformität (§15)
- Innovationsförderung (§12–14)

**Aber nicht:**
- **Resilienzanforderungen** für KI-Systeme in kritischen Infrastrukturen
- **Drittstaatenrisiken** bei der Beschaffung
- **Krisenreaktionspläne** bei abruptem Dienstausfall
- **Zusammenarbeit mit NIS2-Behörden** (BSI) bei Drittstaaten-bedingten Ausfällen

---

## 5. Rechtliche Handlungsoptionen für die EU/Deutschland

### 5.1 Sofortmaßnahmen (ohne Gesetzesänderung)

| Maßnahme | Rechtsgrundlage | Umsetzung |
|---|---|---|
| **BAuA-Risikomeldung** | §7 KI-MIG i.V.m. Art. 79, 82 KI-VO | Meldung des Ausfalls als Risiko trotz Konformität |
| **BSI-Information** | §9 KI-MIG (Zusammenarbeit) | Information des BSI über Drittstaaten-bedingten Ausfall |
| **BNetzA-Marktüberwachung** | §2 KI-MIG | Prüfung, ob der Ausfall ein systemisches Marktrisiko darstellt |

### 5.2 Mittelfristige Regelungsbedarfe

| Regelungsbedarf | Mögliche Umsetzung |
|---|---|
| **Souveränitätsklausel in öffentlicher Beschaffung** | Vergaberecht: Bevorzugung EU-basierter KI-Anbieter bei kritischen Anwendungen |
| **Redundanzpflicht in NIS2** | Ergänzung der NIS2-Durchführungsgesetze: Pflicht zur Multi-Cloud-/Multi-Model-Strategie |
| **KI-Exit-Pläne** | Analog zu DORA: Pflicht zu Exit-Plänen für KI-Dienste in kritischen Infrastrukturen |
| **Drittstaaten-Risikobewertung** | Pflicht zur Bewertung politischer Risiken bei KI-Beschaffung (analog zu Lieferkettengesetz) |
| **Haftungshaftung** | Klärung, ob der Betreiber haftet, wenn er ein Risiko kannte oder kennen musste |

---

## 6. Fazit

> **Der Anthropic-Fall vom 12. Juni 2026 offenbart eine fundamentale regulatorische Blindstelle:** Die EU-Regulierung (KI-VO, NIS2, DORA) geht davon aus, dass KI-Systeme entweder konform oder nicht konform sind, verfügbar oder nicht verfügbar. Sie bedenkt nicht den Fall, dass ein **konformes, funktionierendes System durch einen Drittstaat willkürlich abgeschaltet wird** – und dass diese Abschaltung die Betreiber in einen Regulierungskonflikt bringt, weil sie ihre eigenen Pflichten (Resilienz, Verfügbarkeit, Datenschutz) nicht mehr erfüllen können.

Der KI-MIG-Entwurf ist in dieser Hinsicht **nicht vorbereitet**. Er regelt die Marktüberwachung der KI-Systeme, aber nicht die **Resilienz der KI-Lieferketten** gegenüber politischen Risiken aus Drittstaaten.
