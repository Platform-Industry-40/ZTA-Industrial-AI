# Step 2 – Anforderungsgenerierung: Security Requirements für die Kollaborationsplattform

## Thema
Generierung menschenlesbarer, normreferenzierter Security Requirements aus dem aggregierten Regulierungsdatensatz – architekturunabhängig, für spätere Überführung in ZTA-Zugriffsregeln.

## Motivation
Das aggregierte JSON aus Step_1_3/Collaboration_Platform/ enthält konsolidiertes Regulierungswissen für alle Partnerländer. Schritt 2 überführt dieses Wissen in strukturierte Security Requirements, die von einem Domain Expert geprüft werden können und als präzise Eingabe für die Code-Generierung in Schritt 3 dienen.

## Hauptmessages
- Requirements sind geolokationsbasiert: Datenzugriffsregeln berücksichtigen Herkunftsland, Datenkategorie und regulatorische Zulässigkeit des Ziellandes.
- Normreferenzen umfassen ISO 27001, NIST SP 800-207 sowie länderspezifische Regulierungen (DSGVO, NIS-2, DPDP, CSL/PIPL).
- Der Prompt ist bewusst umfangreich, da er den vollständigen aggregierten Datensatz als Kontext enthält.
- Antwort liegt vor von: Gemini 2.5 Pro.

## Dokumente im Ordner
- `Step_2__01_Prompt_I40_Domain_Collab_Platform_Requirements_Gen_Step_2025_11_14.txt`         ← Prompt (inkl. aggregierter Eingabedaten)
- `Step_2__02_Answer_Gemini_25_Pro_I40_Domain_Collab_Platform_Requirements_Gen_...txt`        ← Generierte Security Requirements

## Verbindung zum Gesamtprojekt ZTA+KI_2026
Die generierten Security Requirements bilden den Eingabedatensatz für Step_3/Collaboration_Platform/.
