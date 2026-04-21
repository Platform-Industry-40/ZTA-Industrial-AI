# Step 2 – Anforderungsgenerierung: Security Requirements für BAPI_USER_GET_DETAIL

## Thema
Generierung menschenlesbarer, normreferenzierter Security Requirements aus dem aggregierten Bewertungsergebnis – architekturunabhängig und als Vorstufe zur Code-Generierung.

## Motivation
Das aggregierte JSON aus Schritt 1.3 enthält konsolidiertes Sicherheitswissen, aber noch keinen ausführbaren Code. Schritt 2 überführt dieses Wissen in strukturierte Security Requirements, die einerseits von einem Domain Expert geprüft werden können und andererseits als präzise Eingabe für die Code-Generierung in Schritt 3 dienen.

## Hauptmessages
- Die generierten Requirements sind bewusst architektur- und laufzeitunabhängig formuliert.
- Jede Anforderung enthält ID, Beschreibung, Rationale, Control und Normreferenz (IEC 62443).
- Abgedeckte Bereiche: Least Privilege, Audit Logging, RFC-Absicherung, Netzwerksegmentierung und Anomalieerkennung.
- Antworten liegen vor von: Gemini 2.5 Flash Lite, Gemini 2.5 Pro, GPT-5, Grok 4, Mistral Large Instruct.

## Dokumente im Ordner
- `Step_2__01_Prompt_SAP_Domain_Requirements_Gen_Step_2025_10_14.txt`              ← Prompt (inkl. aggregierter Eingabedaten)
- `Step_2__02_Answer_Gemini_25_Flash_Lite_...txt`                                  ← Antwort Gemini 2.5 Flash Lite
- `Step_2__02_Answer_Gemini_25_Pro_...txt`                                         ← Antwort Gemini 2.5 Pro
- `Step_2__02_Answer_GPT5_...txt`                                                  ← Antwort GPT-5
- `Step_2__02_Answer_Grok4_...txt`                                                 ← Antwort Grok 4
- `Step_2__02_Answer_Mistral_Large_Instruct_...txt`                                ← Antwort Mistral Large Instruct

## Verbindung zum Gesamtprojekt ZTA+KI_2026
Die generierten Security Requirements bilden den Eingabedatensatz für Schritt 3 (Code-Generierung).
