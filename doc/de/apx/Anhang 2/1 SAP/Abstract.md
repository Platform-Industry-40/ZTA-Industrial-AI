## **Titel**
LLM-gestützte Sicherheitsbewertung und ABAC-Regelgenerierung für SAP S/4HANA im Zero-Trust-Kontext: Exemplarische Durchführung des iterativen 4-Schritte-Ansatzes am Funktionsbaustein BAPI_USER_GET_DETAIL

## **Abstract**
Dieser Use Case dokumentiert die vollständige Durchführung des iterativen LLM-Ansatzes zur Generierung von Attribute-Based Access Control (ABAC)-Regeln im SAP-Sicherheitskontext. Als Untersuchungsobjekt diente der RFC-fähige SAP-Funktionsbaustein `BAPI_USER_GET_DETAIL`, der aufgrund seiner Fähigkeit, sensitive Benutzerdaten inklusive Rollen, Profile und Anmeldedaten offenzulegen, ein hohes Sicherheitsrisiko darstellt.

In Schritt 1.1 wurde ein strukturierter JSON-Prompt mit Traceability-Feldern (LLM-Name, Version, Timestamps, Sourcing) mehrfach und gegen verschiedene LLM-Anbieter gestellt (Gemini, GPT-4, Grok, DeepSeek). Schritt 1.3 aggregierte die Rohantworten deterministisch zu einem konsolidierten JSON, das Gemeinsamkeiten und gewichtete Abweichungen explizit erhält. In Schritt 2 wurden daraus menschenlesbare Security Requirements generiert, referenziert gegen IEC 62443 (SR 1.3, SR 1.5, SR 2.8, SR 2.9, SR 5.2). Schritt 3 überführte diese Anforderungen in ausführbaren Code für drei ZTA-Laufzeitumgebungen: XACML, Python und ABAP.

Alle Schritte wurden durch verfügbares SAP-Domänenwissen verifiziert. Der Use Case bestätigt die Machbarkeit des Ansatzes und diente als methodische Grundlage für den anspruchsvolleren Industrie-4.0-Use-Case. Alle Ergebnisse sind als Näherungslösungen zu verstehen.

### **Schlüsselwörter:**
SAP Security, BAPI_USER_GET_DETAIL, ABAC, Zero Trust Architecture, XACML, ABAP, IEC 62443, LLM-Aggregation, Prompt Engineering, Traceability
