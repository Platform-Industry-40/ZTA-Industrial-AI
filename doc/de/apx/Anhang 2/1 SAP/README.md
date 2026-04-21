# Use Case 1: ABAC-Regelgenerierung für SAP S/4HANA

## Thema
Generierung von attributbasierten Zugriffsregeln (ABAC) für sicherheitskritische SAP-Objekte in einem SAP-S/4HANA-System – als ausführbarer Code für eine ZTA-Laufzeitumgebung.

## Motivation
SAP-Systeme enthalten hochsensible Funktionsbausteine, deren unkontrollierter Zugriff Privilege-Escalation-Angriffe, Reconnaissance und Datenmissbrauch ermöglicht. Die Frage, ob LLMs zuverlässig Sicherheitsbewertungen und daraus abgeleiteten ausführbaren Code für ZTA-Laufzeiten erzeugen können, wurde anhand eines konkreten SAP-Objekts (`BAPI_USER_GET_DETAIL`) geprüft. Dieser Use Case diente zugleich als Vorbereitungs-Use-Case, da Domänenwissen für die Validierung der LLM-Antworten verfügbar war.

## Hauptmessages
- Alle vier Schritte des iterativen Ansatzes (Datenerhebung, Aggregation, Anforderungen, Code) wurden erfolgreich durchlaufen und verifiziert.
- Der Prompt für Schritt 1.1 erzwingt ein strukturiertes JSON-Ausgabeformat mit Traceability-Feldern (LLM-Name, Version, Timestamps).
- Schritt 1.3 aggregiert mehrere LLM-Antworten deterministisch zu einem konsolidierten JSON mit Gemeinsamkeiten und Abweichungen.
- Aus dem aggregierten Ergebnis wurden in Schritt 2 menschenlesbare Security Requirements generiert (IEC-62443-referenziert).
- In Schritt 3 wurde ausführbarer Code in drei Sprachen erzeugt: XACML, Python und ABAP.
- Alle Ergebnisse sind als Näherungslösung zu verstehen (**Approximation approach only**).

## Dokumente und Ordner
- [Step_1_1/](./Step_1_1/)  ← Prompt und LLM-Antworten: Sicherheitsbewertung BAPI_USER_GET_DETAIL
- [Step_1_3/](./Step_1_3/)  ← Prompt und LLM-Antworten: Aggregation der Bewertungen
- [Step_2/](./Step_2/)      ← Prompt und LLM-Antworten: Generierung der Security Requirements
- [Step_3/](./Step_3/)      ← Prompt und LLM-Antworten: Code-Generierung (XACML, Python, ABAP)

## Empfohlene Lesereihenfolge
1. Step_1_1/ (Ausgangsfrage und LLM-Rohantworten)
2. Step_1_3/ (Aggregiertes Ergebnis mit Gemeinsamkeiten und Abweichungen)
3. Step_2/ (Abgeleitete Security Requirements)
4. Step_3/ (Generierter ausführbarer Code)

## Verbindung zum Gesamtprojekt ZTA+KI_2026
Dieser Use Case belegt die grundsätzliche Machbarkeit des iterativen Ansatzes im SAP-Sicherheitskontext und bildet die methodische Basis für den komplexeren Use Case 2 (Industrie 4.0).
