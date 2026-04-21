# Step 1.3 – Aggregation der Sicherheitsbewertungen

## Thema
Deterministische Aggregation der LLM-Rohantworten aus Schritt 1.1 zu einem konsolidierten JSON mit expliziter Darstellung von Gemeinsamkeiten und gewichteten Abweichungen.

## Motivation
Einzelne LLM-Antworten unterliegen Seed-Varianz, Biasing und anderen Effekten. Erst die strukturierte Aggregation mehrerer Antworten verschiedener LLMs erzeugt ein belastbares, vollständiges Bild. Der Aggregationsprompt arbeitet deterministisch: Er fasst nicht zusammen, sondern erhält alle inhaltlichen Informationen – Gemeinsamkeiten als Konsens, Abweichungen verbatim mit Signifikanzgewichtung.

## Hauptmessages
- Der Prompt agiert als deterministischer Aggregationsmotor, nicht als Zusammenfassungswerkzeug.
- Abweichungen werden verbatim extrahiert und mit Signifikanz (high / medium / low) bewertet.
- Der CriticalityScore wird als Median aller Eingabewerte berechnet.
- Ein optimierter zweiter Prompt (`Step_13__03`) verfeinert die Aggregationsstruktur.
- Antworten liegen vor von: Amazon Nova Pro, Claude Sonnet 4, DeepSeek, Gemini 2.5 Flash, Gemini 2.5 Pro, GPT-5, Grok 4, Mistral Large.

## Dokumente im Ordner
- `Step_13__01_Prompt_SAP_Domain_Aggregation_Step_2025_10_09.txt`           ← Aggregations-Prompt (Version 1)
- `Step_13__02_Answer_Amazon_Nova_Pro_...txt`                                ← Antwort Amazon Nova Pro
- `Step_13__02_Answer_Claude4_Sonnet_...txt`                                 ← Antwort Claude Sonnet 4
- `Step_13__02_Answer_Deep_Seek_...txt`                                      ← Antwort DeepSeek
- `Step_13__02_Answer_Gemini_25_Flash_...txt`                                ← Antwort Gemini 2.5 Flash
- `Step_13__02_Answer_Gemini_25_Pro_...txt`                                  ← Antwort Gemini 2.5 Pro
- `Step_13__02_Answer_GPT5_...txt`                                           ← Antwort GPT-5
- `Step_13__02_Answer_Grok4_...txt`                                          ← Antwort Grok 4
- `Step_13__02_Answer_Mistral_Large_...txt`                                  ← Antwort Mistral Large
- `Step_13__03_Optimized_Prompt_SAP_Domain_Aggregation_Step_2025_10_09.txt` ← Optimierter Aggregations-Prompt (Version 2)

## Verbindung zum Gesamtprojekt ZTA+KI_2026
Das konsolidierte Aggregationsergebnis bildet den Eingabedatensatz für Schritt 2 (Anforderungsgenerierung).
