# medical-docs-de-klinik

Textbausteine für die **stationäre/klinische** Dokumentation auf Deutsch (espanso), ergänzend
zu [medical-docs-de](../medical-docs-de) (welches primär hausärztliche/ambulante
Textbausteine aus dem Original [medical-docs](https://github.com/wressl/medical-docs)
übersetzt). Dieses Paket bildet gängige Konventionen deutscher Arztbriefe,
Notaufnahme-Befunde und klinischer Scores ab, orientiert an gebräuchlichen
Formulierungen wie sie z.B. auf [berichteguru.com](https://www.berichteguru.com/textbausteine)
und [befundomat.de](https://befundomat.de/internistischer-untersuchungsbefund.html) zu finden sind.

## Installation

```
espanso install medical-docs-de-klinik --git https://github.com/ArcticSpaceFox/medical-docs-ger --external
```

## Benötigte globale Variablen

Dieses Paket nutzt dieselben Platzhalter-Variablen wie `medical-docs-de`
(`cc`, `sp`, `op`, `pp`, `ap`). Siehe Haupt-[README](../README.md) für die
`global_vars`-Konfiguration.

## Übersicht der Textbausteine

Arztbrief-Struktur         | Beschreibung
-------------------------- | ------------------
:arztbrief                 | Grundgerüst eines Arztbriefs (Anrede, Diagnosen, Anamnese, Verlauf, Beurteilung)
:anrede                    | Standardanrede an Kollegen/in
:diagnosen                 | Diagnosenliste mit ICD-10-Platzhaltern
:epikrise                  | Epikrise-Textbaustein
:procedere                 | Procedere/Empfehlungen bei Entlassung
:medikation                | Entlassmedikation-Tabelle
:abschluss                 | Grußformel am Briefende
:vorstellungsgrund         | Vorstellungsgrund-Baustein
:sozialanamnese            | Sozial- und Familienanamnese
:vorerkrankungen           | Vorerkrankungen/Voroperationen/Medikation/Allergien

Notaufnahme                | Beschreibung
-------------------------- | ------------------
:not                       | Kompletter Notaufnahme-Aufnahmebefund
:triage                    | Manchester-Triage-System Baustein
:abcde                     | ABCDE-Schema (Primary Survey)
:sampler                   | SAMPLER-Anamneseschema
:opqrst                    | OPQRST-Schmerzanamnese
:schockraum                | SBAR-Schockraumübergabe
:entlassnotaufnahme        | Entlassbaustein aus der Notaufnahme
:aufnahmeindikation        | Begründung der stationären Aufnahme

Untersuchungsbefunde        | Beschreibung
-------------------------- | ------------------
:internistat               | Kompletter internistischer Normalbefund
:cor / :pulmo / :abd       | Einzelbausteine Herz/Lunge/Abdomen
:haut / :lk / :oedeme      | Haut, Lymphknoten, Ödeme
:ekgbefund / :auskult      | EKG-Normalbefund, Auskultationsbefund
:neurostat                 | Kompletter neurologischer Normalbefund
:hirnnerven                | Hirnnervenübersicht I-XII
:pupillen / :babinski      | Einzelbefunde
:aphasie / :facialisparese | Fokussierte neurologische Bausteine

Scores                      | Beschreibung
-------------------------- | ------------------
:nihss                     | NIH Stroke Scale, alle Items mit Punktwerten
:gcsklinik                 | Glasgow Coma Scale (ausführlich)
:chads                     | CHA2DS2-VASc-Score
:wellsdvtklinik            | Wells-Score TVT
:wellspeklinik             | Wells-Score Lungenembolie
:qsofa                     | qSOFA (Sepsis-Screening)
:curb65                    | CURB-65 (Pneumonie)
:nyha                      | NYHA-Klassifikation
:killip                    | Killip-Klassifikation
:glasgowblatchford          | Glasgow-Blatchford-Score
:mmse                      | Mini-Mental-Status-Test
:asa                       | ASA-Klassifikation

Reanimation/ALS             | Beschreibung
-------------------------- | ------------------
:reanimation               | Reanimationsprotokoll (ERC-Leitlinien, BLS/ALS)
:algorithmus                | ALS-Algorithmus Kurzfassung
:ample                     | AMPLE-Anamnese (Trauma, ATLS)
:roscbefund                | Postreanimationsbehandlung nach ROSC
:reanimationsabbruch       | Abbruch der Reanimation, Abbruchkriterien

Akutmedizin                 | Beschreibung
-------------------------- | ------------------
:stemi                     | Akutes Koronarsyndrom/STEMI-Versorgung
:anaphylaxie               | Anaphylaxie (Ring & Messmer, Sofortmaßnahmen)
:sepsis                    | Sepsis-Bundle ("Sepsis-Six"), Sepsis-3-Kriterien
:schockformen              | Differentialdiagnose der Schockformen
:intox                     | Verdacht auf Intoxikation, Giftnotruf, Antidot-Verweis

Notfallmedikamente           | Beschreibung
-------------------------- | ------------------
:notfallmedikamente        | Standarddosierungen häufiger Notfallmedikamente
:perfusor                  | Perfusor-Berechnung und Laufraten-Formel
:antidot                   | Antidota-Übersichtstabelle

Leichenschau                | Beschreibung
-------------------------- | ------------------
:leichenschau              | Ärztliche Leichenschau, sichere Todeszeichen, Todesart
:sicheretodeszeichen       | Detaillierte sichere Todeszeichen mit Zeitangaben
:vorlaeufigetodesbescheinigung | Vorläufige Todesbescheinigung (Notarzt)

## Disclaimer

Inhalte ausschließlich zur Nutzung durch approbiertes medizinisches Fachpersonal
gedacht, ohne Gewähr auf Richtigkeit oder Vollständigkeit. Ersetzt keine
eigenständige klinische Beurteilung. Dosierungsangaben (`:notfallmedikamente`,
`:perfusor`, `:antidot`) sind Orientierungswerte nach gängigen
Rettungsdienst-/Klinikstandards (u.a. ERC-Leitlinien, GRC) - stets gegen
aktuelle hausinterne Standards und Fachinformation prüfen, insbesondere bei
Kindern, Schwangeren, Niereninsuffizienz.
