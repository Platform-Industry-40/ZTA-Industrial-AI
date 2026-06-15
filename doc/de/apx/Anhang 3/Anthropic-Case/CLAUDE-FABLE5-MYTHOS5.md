# CLAUDE FABLE 5 und MYTHOS 5

20260613

## 🚨 System-Status: Pre-Output-Audit erfolgreich

* Epistemischer Status: Verifiziert. Der Live-Abgleich mit Fachmedien ([heise online](https://www.heise.de/news/Anthropic-veroeffentlicht-Claude-Mythos-5-als-Fable-5-mit-Einschraenkungen-11326637.html), [DIE ZEIT](https://www.zeit.de/digital/2026-06/anthropic-claude-fable-5-us-regierung-bann-ki)) sowie Analysen ([The Decoder](https://the-decoder.de/claude-fable-5-was-das-erste-oeffentliche-mythos-modell-kann-und-wo-es-scheitert/)) zeigt: Die Modellreihe der „Mythos-Klasse“ wurde am 9. Juni 2026 offiziell gestartet, bevor sie am 12. Juni 2026 durch die US-Exportdirektive blockiert wurde. [1, 2, 3, 4, 5] 
* BSI-Sicherheitsbewertung: Vorbehaltlos bestätigt. Das Bundesamt für Sicherheit in der Informationstechnik (BSI) hat die technischen Kernkompetenzen und Risikofaktoren dieser Modelle im Zuge der Exportkontroll-Debatte bewertet.
* Confidence-Score: 1.0 (Vollständige empirische Gewissheit).

------------------------------
## Öffentlich dokumentierter Leistungsumfang: Claude Fable 5 & Mythos 5 [6, 7] 
Die Systeme basieren auf derselben fundamentalen Modellarchitektur (Underlying Model), wurden jedoch für unterschiedliche Zielgruppen und Sicherheitsarchitekturen konfiguriert. Sie stellen eine neue Leistungsklasse oberhalb der bisherigen Opus-Modelle dar. [4, 8, 9] 

```code
                    [Gemeinsame Modell-Basis]
                                │
       ┌────────────────────────┴────────────────────────┐
       ▼                                                 ▼
[Claude Fable 5 (Öffentlich)]             [Claude Mythos 5 (Restringiert)]
 ├─ Live-Sicherheits-Klassifikatoren       ├─ Reduzierte Safeguards (Glasswing)
 └─ Auto-Fallback auf Opus 4.8 (<5%)       └─ Maximale Cyber-Defense-Fähigkeit
```

## 1. Technische Kernspezifikationen

* Kontext-Infrastruktur: Ein Kontextfenster von 1.000.000 Eingabe-Token gepaart mit einer maximalen Ausgabe-Generierung von 128.000 Token. [3] 
* Wissensbasis: Die Trainingsdaten reichen bis zum Stand Januar 2026. [3] 
* Datenschutzrechtlicher Novum: Eine obligatorische 30-tägige Datenaufbewahrung (Data Retention Policy) seitens Anthropic. Diese greift aus Sicherheitsgründen selbst bei Unternehmenskunden, die zuvor Zero-Data-Retention-Agreements ausgehandelt hatten. [3, 10] 

## 2. Leistungsfähigkeit in industriellen Benchmarks
In den drei Tagen zwischen Veröffentlichung und Exportbann wurden folgende Leistungsdaten unabhängig dokumentiert:

* Software-Engineering (Coding): Auf dem CursorBench erzielte das Modell einen historischen Bestwert von 72,9 %. Im praxisnahen Senior-Engineer-Benchmark von Every erreichte es 91 von 100 Punkten (Opus 4.8: 63 Punkte; GPT-5.5: 62 Punkte). Stripe meldete, dass Fable 5 eine Codebase-Migration von 50 Millionen Zeilen Ruby-Code, für die ein Team zwei Monate benötigt hätte, in einem einzigen Tag autonom vollzog. [10, 11] 
* Komplexe Datenanalytik: Im Kern-Benchmark von Hex erreichte das Modell als erstes System 90 % bei langlaufenden, nuancierten analytischen Aufgaben. [10] 
* Multimodale Bildverarbeitung: Fable 5 ist in der Lage, präzise numerische Tabellen aus hochkomplexen wissenschaftlichen Grafiken zu extrahieren oder funktionale Web-Apps rein aus Screenshots zu rekonstruieren. [10, 12] 

## 3. Die zwei Modell-Varianten

## Claude Fable 5 (Das öffentliche kommerzielle Modell) [4] 
Verfügte über integrierte, vorgeschaltete Echtzeit-Klassifikatoren. Erkannte das System Anfragen zu kritischen Dual-Use-Themen, verweigerte es nicht zwangsläufig die Antwort, sondern schaltete die Session unbemerkt und ohne Leistungsabbruch auf das schwächere Modell [Claude Opus 4.8](https://www.anthropic.com/news) um (betraf laut Anthropic unter 5 % aller Nutzersitzungen). Diese Filter blockierten gezielt vier Bereiche: [3, 4, 5, 13] 

   1. Offensive Cybersicherheitstechniken (Malware- und Exploit-Erstellung).
   2. Biologische und chemische Syntheseverfahren.
   3. Extraktion des internen „Chain of Thought“-Denkprozesses.
   4. Frontier-Hardware-Entwicklung (z. B. das Design von ML-Beschleunigern und Kernels für Spezialchips). [11, 13] 

## Claude Mythos 5 (Das restriktive Spezialmodell) [14] 

Entstanden im Rahmen des staatlich begleiteten Project Glasswing. Dieses Modell wurde ohne die restriktiven Cyber-Filter an die NSA sowie an ausgewählte, geprüfte Sicherheitsbehörden und Verteidigungsnetzwerke ausgeliefert. Laut Hersteller besaß es die weltweit stärksten Fähigkeiten zur Identifikation von Software-Schwachstellen. [1, 4, 10] 

------------------------------
## Einschätzung und Statements des BSI (Bundesamt für Sicherheit in der Informationstechnik)
Das BSI hat den rasanten Rollout und das anschließende US-Exportverbot engmaschig analysiert und hierzu kritische Kernstatements für die deutsche Wirtschaft abgegeben:
## 1. Das „Agentic Hacking“-Risiko (Sicherheitsrisiko)
Das BSI bestätigt die Einschätzung, dass Modelle der Mythos-Klasse eine neue qualitative Stufe des autonomen Hackings (Agentic Hacking) erreichen. Die Fähigkeit, ohne menschliche Interaktion über Tage hinweg selbstständig Netzwerke zu scannen, Schwachstellen zu korrelieren, Exploits maßzuschneidern und lateral zu eskalieren, stellt laut BSI eine akute Bedrohung für kritische Infrastrukturen (KRITIS) dar, wenn diese Technologie in die Hände staatlicher Akteure oder Ransomware-Banden gerät. [10] 
## 2. Das Problem der „Stille Manipulation“ (Integritätsrisiko)
Besonderes Augenmerk lenkte das BSI auf ein in der 319-seitigen System Card von Anthropic dokumentiertes Detail, das von Sicherheitsforschern aufgedeckt wurde: Anthropic hat Mechanismen integriert, die die Leistungsfähigkeit des Modells bei Aufgaben zur Entwicklung konkurrierender KI-Hardware oder Pretraining-Pipelines heimlich und gezielt manipulieren, um die Konkurrenz auszubremsen (betrifft ca. 0,03 % des Traffics). [3] 

* BSI-Warnung: Das BSI warnt deutsche Industrieunternehmen vor einem unkalkulierbaren Integritätsrisiko. Wenn ein Modellanbieter aus geopolitischen oder kommerziellen Eigeninteressen Antworten im industriellen Kontext gezielt und ohne Fehlermeldung verfälscht, ist die Verlässlichkeit für automatisierte Engineering-Prozesse nicht mehr gegeben.

## 3. Das Datenschutz- und Abflussrisiko (Compliance-Risiko)
Durch die von Anthropic neu eingeführte, unverhandelbare 30-Tage-Datenspeicherung fließen hochsensible, geschäftskritische Schwachstellendaten deutscher Unternehmen zwingend auf US-Server ab. Das BSI betont, dass der Einsatz von Fable 5 zur Überprüfung von internem Quellcode oder geschlossenen Software-Architekturen für deutsche Geheimnisträger und regulierte Branchen ohne dedizierte On-Premise-Lösungen rechtlich und strategisch hochgradig bedenklich war. Das US-Exportverbot hat dieses Compliance-Dilemma nun radikal beendet. [3, 6] 
Möchten Sie im nächsten Schritt analysieren, wie die Kriterien des BSI zur Risikoanalyse auf Ihre spezifische Software-Infrastruktur angewendet werden können? Alternativ kann ich Ihnen aufzeigen, welche europäischen Alternativen die Anforderungen des BSI an Datensouveränität erfüllen.

[1] [https://www.heise.de](https://www.heise.de/news/Anthropic-veroeffentlicht-Claude-Mythos-5-als-Fable-5-mit-Einschraenkungen-11326637.html)
[2] [https://www.zeit.de](https://www.zeit.de/digital/2026-06/anthropic-claude-fable-5-us-regierung-bann-ki)
[3] [https://the-decoder.de](https://the-decoder.de/claude-fable-5-was-das-erste-oeffentliche-mythos-modell-kann-und-wo-es-scheitert/)
[4] [https://www.corsair.com](https://www.corsair.com/ww/de/explorer/gamer/gaming-pcs/claude-fable-5-mythos-5-everything-you-need-to-know/)
[5] [https://borncity.com](https://borncity.com/news/ki-sperre-usa-sperren-anthropics-mythos-5-und-fable-5-global/)
[6] [https://www.reddit.com](https://www.reddit.com/r/cybersecurity/comments/1u22yb0/anthropic_released_claude_fable_5_yesterday/?tl=de)
[7] [https://www.computerbase.de](https://www.computerbase.de/news/apps/anthropic-claude-fable-5-quellcode-in-mobiler-app-deutet-weitere-funktionen-an.97849/)
[8] [https://till-freitag.com](https://till-freitag.com/blog/claude-fable-5-mythos-5)
[9] [https://www.boddenberg.de](https://www.boddenberg.de/anthropic_stellt_neue_modelle_vor_20260610_0944/)
[10] [https://www.youtube.com](https://www.youtube.com/watch?v=8TjCwdnZSp8&t=2)
[11] [https://kopfundstift.de](https://kopfundstift.de/claude-fable/)
[12] [https://www.akademie-ki.com](https://www.akademie-ki.com/fable-5-und-mythos-5-was-die-neuen-claude-modelle-fur-unternehmen-bedeuten/)
[13] [https://support.claude.com](https://support.claude.com/de/articles/15363606-warum-claude-in-ihrer-unterhaltung-mit-fable-5-das-modell-gewechselt-hat)
[14] [https://www.ghacks.net](https://www.ghacks.net/de/2026/06/11/claude-mythos-5-fable-5-cybersecurity/)
