## **Titel**
Proof of Concept: Iterativer LLM-agnostischer Ansatz zur Generierung von ABAC-Regeln für Zero Trust Architectures in Industrie-4.0-Umgebungen

## **Abstract**
Der vorliegende Proof of Concept untersucht die Machbarkeit des Einsatzes von Large Language Models (LLMs) zur automatisierten Generierung von Attribute-Based Access Control (ABAC)-Regeln in Zero Trust Architectures (ZTA). Ausgangspunkt war die Beobachtung, dass LLM-typische Hindernisse – darunter Halluzinationen, Silent Truncation, Token-Drop-Effekte, Seed-Varianz, Attention Erosion und Instruction Drift – einen direkten Einsatz in sicherheitskritischen Umgebungen zunächst ausschließen.

Als Antwort darauf wurde ein iterativer, schrittweiser Ansatz entwickelt, der durch kleine, kontextfreie Prompts, mehrfache LLM-Befragungen (gleicher Prompt, verschiedene LLMs und Versionen) und explizite Aggregationsschritte die genannten Effekte systematisch minimiert. Der Ansatz ist vollständig LLM-agnostisch und wurde gegen sieben verschiedene LLM-Anbieter und -Versionen validiert. Jeder Schritt ist einzeln protokollierbar und durch einen Domain Expert als „Human in the Loop" verifizierbar, womit Traceability-Anforderungen des EU AI Act erfüllt werden.

Die Methodik wurde an zwei Use Cases erprobt: der Generierung von ABAC-Regeln für ein SAP-S/4HANA-System sowie für eine multinationale Industrie-4.0-Kollaborationsplattform mit komplexen Import-/Export- und Datenschutzanforderungen. In beiden Fällen konnte ausführbarer ZTA-Code (XACML, C++, Python, ABAP) erfolgreich generiert und durch verfügbares Domänenwissen verifiziert werden. Alle Ergebnisse sind als Näherungslösungen zu verstehen.

### **Schlüsselwörter:**
Large Language Models, Zero Trust Architecture, ABAC, Industrie 4.0, EU AI Act, Traceability, Halluzination, Prompt Engineering, LLM-Agnostizität, XACML, SAP Security
