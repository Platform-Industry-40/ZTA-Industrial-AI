# Step 1.1 – Datenerhebung: Sicherheitsbewertung BAPI_USER_GET_DETAIL

## Thema
LLM-basierte Sicherheitsbewertung des SAP-Funktionsbausteins `BAPI_USER_GET_DETAIL` im strukturierten JSON-Format mit Traceability-Feldern.

## Motivation
Ausgangspunkt ist eine konkrete Sicherheitsfrage im SAP-Domänenkontext: Wie kritisch ist der Funktionsbaustein `BAPI_USER_GET_DETAIL` aus Sicherheitssicht? Der Prompt ist so gestaltet, dass verschiedene LLMs dasselbe maschinenlesbare Ausgabeformat liefern und jede Antwort eindeutig rückverfolgbar ist (LLM-Name, Version, Timestamps).

## Hauptmessages
- Der Prompt erzwingt ein striktes JSON-Ausgabeformat; Freitextantworten außerhalb der definierten Attribute sind explizit untersagt.
- Traceability-Felder (LLM_Name, LLM_Version, AnswerTimeStamp, QueryTimeStamp, Sourcing) ermöglichen die lückenlose Protokollierung jeder Antwort.
- Das Feld `ObjectKnown` verhindert Halluzinationen: LLMs dürfen nur dann inhaltliche Aussagen treffen, wenn sie das Objekt mit exaktem Namen kennen.
- Derselbe Prompt wurde ohne vorherigen Kontext mehrfach und gegen verschiedene LLM-Anbieter gestellt.

## Dokumente im Ordner
- `Step_11__01_Prompt_SAP_Domain_DataCollection_Step_2025_10_02.txt`  ← LLM-agnostischer Prompt
- `Step_11__02_1Answer_Gemini_25_Pro_Online_...txt`                   ← Antwort Gemini 2.5 Pro (mit Online-Recherche)
- `Step_11__02_1Answer_GPT4_without_Online_...txt`                    ← Antwort GPT-4 (ohne Online-Recherche)
- `Step_11__02_2Answers_Grok4_Online_...txt`                          ← 2 Antworten Grok 4 (mit Online-Recherche)
- `Step_11__02_3Answers_Gemini_25_Pro_without_Online_...txt`          ← 3 Antworten Gemini 2.5 Pro (ohne Online-Recherche)
- `Step_11__02_3Answers_GPT4_Online_...txt`                           ← 3 Antworten GPT-4 (mit Online-Recherche)
- `Step_11__02_4Answers_DeepSeek_without_Online_...txt`               ← 4 Antworten DeepSeek (ohne Online-Recherche)
- `Step_11__02_4Answers_Gemini_Flash_Online_...txt`                   ← 4 Antworten Gemini Flash (mit Online-Recherche)

## Verbindung zum Gesamtprojekt ZTA+KI_2026
Die hier gesammelten Rohantworten bilden den Eingabedatensatz für Schritt 1.3 (Aggregation).
