# Scope

## Architektur der Modul-Teile 1–3

Die drei Modul-Teile beschreiben gemeinsam einen vollständigen Verifikationsbau:

- **Modul ZTA Teil 1** definiert den generischen Anforderungskatalog mit 15 Anforderungen (ZTA-01 bis ZTA-15). Jede Anforderung ist gleichwertig und vollständig spezifiziert.
- **Modul ZTA Teil 2** beschreibt für jede Anforderung die zugehörigen Prüfschritte. Pro Anforderung sind typischerweise 5–10 Prüfschritte vorgesehen.
- **Modul ZTA Teil 3** liefert für jeden Prüfschritt die granulare attributbasierte Verifikation mit konkreten Kontextdimensionen, erwarteten Ergebnissen und Evidenz-Nachweisen.

Der vollständige Bau würde damit mehrere hundert Verifikationspunkte umfassen – eine substanzielle Ingenieurs- und Compliance-Leistung, die im Rahmen dieses Projekts bewusst nicht vollständig ausgearbeitet wird.

## Exemplarischer Pfad

Aktuell ist **genau ein Pfad** vollständig und inhaltlich belastbar ausgearbeitet:

**ZTA-01 → ZTA-01-001 → ZTA-01-001-01 bis -07**

Dieser Pfad ist nicht als Platzhalter zu verstehen, sondern als vollwertiges, auditierbares Beispiel – er zeigt exemplarisch, wie der Gesamtkatalog in der Tiefe aussehen würde und welche Qualität für alle weiteren Äste anzustreben ist. Alle übrigen Anforderungen (ZTA-02 bis ZTA-15) sowie deren Prüfschritte und Verifikationspunkte sind in Teilen 2 und 3 noch nicht ausgearbeitet und müssen analog ergänzt werden.

## Strukturübersicht

Das folgende Diagramm zeigt den vollständigen Bau. Rot markiert ist der aktuell ausgearbeitete Pfad, grün die granularen Verifikationspunkte, grau die noch ausstehenden Äste:

```mermaid
graph LR
    %% === Hauptknoten ===
    Katalog[Anforderungskatalog<br>Modul ZTA Teil 1]:::haupt

    %% === Haupt-Anforderungen ===
    subgraph "Hauptanforderungen"
        ZTA01((ZTA-01<br>Dynam. Richtlinien)):::aktuell
        ZTA02[ZTA-02<br>Identität & Zugriff]:::normal
        ZTA03[ZTA-03<br>Datenprovenienz]:::normal
        ZTA04[ZTA-04<br>Audit & Explain]:::normal
        ZTA05[ZTA-05<br>Human Oversight]:::normal
        ZTA06[ZTA-06<br>Micro-Segmentation]:::normal
        ZTA07[ZTA-07<br>Monitoring & Response]:::normal
        ZTA08[ZTA-08<br>Lifecycle Mgmt]:::normal
        ZTA09[ZTA-09<br>Sichere Kommunikation]:::normal
        ZTA10[ZTA-10<br>Just-in-Time Access]:::normal
        ZTA11[ZTA-11<br>Continuous Posture]:::normal
        ZTA12[ZTA-12<br>Automation & Orchest]:::normal
        ZTA13[ZTA-13<br>Daten-Schutz-Kern]:::normal
        ZTA14[ZTA-14<br>Sichtbarkeit & Analytics]:::normal
        ZTA15[ZTA-15<br>Resilienz & Recovery]:::normal
    end

    %% === Prüfschritte ZTA-01 ===
    subgraph "Prüfschritte ZTA-01"
        PS001((ZTA-01-001<br>Kontext-Erfassung)):::aktuell
        PS002[ZTA-01-002<br>Änderungstest]:::normal
        PS003[ZTA-01-003<br>Logs & Nachvollziehbarkeit]:::normal
        PS004[ZTA-01-004<br>Fail-safe Deny]:::normal
        PS005[ZTA-01-005<br>Performance unter Last]:::normal
        PS006[ZTA-01-006<br>KI-Anomalie-Integration]:::normal
        PS007[ZTA-01-007<br>End-to-End-Trace]:::normal
    end

    %% === Granulare Verifikationspunkte ===
    subgraph "Verifikationspunkte ZTA-01-001"
        VP01((ZTA-01-001-01<br>User-Identität)):::detail
        VP02((ZTA-01-001-02<br>Geräteintegrität)):::detail
        VP03((ZTA-01-001-03<br>Netzwerkkontext)):::detail
        VP04((ZTA-01-001-04<br>OT-Prozesszustand)):::detail
        VP05((ZTA-01-001-05<br>Verhaltensmuster / KI)):::detail
        VP06((ZTA-01-001-06<br>Daten-Integrität & TLS)):::detail
        VP07((ZTA-01-001-07<br>Vollständigkeit & Fail)):::detail
    end

    %% === Verbindungen ===
    Katalog --> ZTA01 & ZTA02 & ZTA03 & ZTA04 & ZTA05 & ZTA06 & ZTA07 & ZTA08 & ZTA09 & ZTA10 & ZTA11 & ZTA12 & ZTA13 & ZTA14 & ZTA15
    ZTA01 --> PS001 & PS002 & PS003 & PS004 & PS005 & PS006 & PS007
    PS001 --> VP01 & VP02 & VP03 & VP04 & VP05 & VP06 & VP07

    %% === Interaktive Klicks ===
    click ZTA01 "https://github.com/artkeller/Plattform_Industrie_4.0/blob/main/ZTA%2BKI_2026/Compliance/V2/Modul_ZTA_Teil_1.md#zta-01" "ZTA-01 Details" _blank
    click PS001 "https://github.com/artkeller/Plattform_Industrie_4.0/blob/main/ZTA%2BKI_2026/Compliance/V2/Modul_ZTA_Teil_2.md#zta-01-001" "Prüfschritt ZTA-01-001" _blank
    click VP01 "https://github.com/artkeller/Plattform_Industrie_4.0/blob/main/ZTA%2BKI_2026/Compliance/V2/Modul_ZTA_Teil_3.md#zta-01-001-01" "User-Identität" _blank

    %% === Styling ===
    classDef haupt fill:#1e3a8a,stroke:#60a5fa,stroke-width:3px,color:#fff,font-weight:bold
    classDef aktuell fill:#b91c1c,stroke:#fecaca,stroke-width:3px,color:#fff
    classDef normal fill:#334155,stroke:#94a3b8,color:#e2e8f0
    classDef detail fill:#065f46,stroke:#6ee7b7,color:#fff
```

## Erweiterung

Jede neue Ausarbeitung eines weiteren Pfades (z. B. ZTA-02 mit seinen Prüfschritten und Verifikationspunkten) folgt exakt der hier gezeigten Struktur und Qualität. Der exemplarische Pfad ZTA-01 dient dabei als verbindliche Vorlage.
