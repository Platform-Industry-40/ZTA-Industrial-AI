## **Titel**
LLM-gestützte ABAC-Regelgenerierung für eine multinationale Industrie-4.0-Kollaborationsplattform: Regulatorische Datenerhebung, Aggregation und parallele Ergebnisverwendung für ZTA-Code und Legal-Reporting

## **Abstract**
Dieser Use Case dokumentiert die Übertragung des iterativen LLM-Ansatzes auf einen multinationalen Industrie-4.0-Kontext. Ausgangsszenario ist ein in der EU ansässiger Robotik-Hersteller mit Entwicklungspartnern in Indien, Singapur, Japan, USA und Kanada sowie Zulieferern aus Malaysia und China. Die Aufgabe bestand darin, die für dieses Partnernetzwerk relevanten Regulierungen (Import-/Exportregeln, Datenschutz, KI-Governance) kontinuierlich zu erheben, zu bewerten und daraus sowohl ausführbare ZTA-Zugriffsregeln als auch Berichte für Management und Legal zu generieren.

In Schritt 1.1 wurden strukturierte JSON-Prompts mit Regulierungsattributen (TypeOfRegulation, ImpactOfRegulation, ClassificationScore u. a.) gegen mehrere LLM-Anbieter gestellt. Schritt 1.3 führte erstmals eine Verzweigung in zwei parallele Auswertungspfade ein: den Pfad `CollaborativeEngineeringPlattform` für die ZTA-Regelgenerierung und den Pfad `ContractRiskReview` für Legal- und Management-Reporting. Schritt 2 generierte für den ZTA-Pfad geolokationsbasierte, normreferenzierte Security Requirements (ISO 27001, NIST SP 800-207). Schritt 3 überführte diese in ausführbaren Code für zwei ZTA-Laufzeitumgebungen (XACML, C++) sowie einen Management-/Legal-Report als PDF.

Der Use Case bestätigt die Übertragbarkeit und Skalierbarkeit des iterativen Ansatzes auf komplexe, multinationale Regulierungsszenarien. Alle Ergebnisse sind als Näherungslösungen zu verstehen.

### **Schlüsselwörter:**
Industrie 4.0, ABAC, Zero Trust Architecture, XACML, C++, Regulatorik, DSGVO, NIS-2, EU AI Act, Multinational, Legal Reporting, LLM-Aggregation, Kollaborationsplattform
