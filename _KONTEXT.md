# _KONTEXT.md — Konsolidierter Index für claude.ai

> Indexdatei für den Zugriff über claude.ai per `web_fetch`. Spiegelt Essentials aus den drei Vault-Bereichen `Berufsbilder/`, `SOFL/` und `Diagnostik/` und verweist auf die Volltexte im selben Repository.
>
> Synchronisierung über Slash-Command `/update-claude-web-context` aus Claude Code im lokalen Obsidian-Vault.
>
> Letzte Aktualisierung: 2026-05-07 (initiale Version, manuell von Claude erstellt; spätere Updates erfolgen automatisch durch den Slash-Command).

---

## 1. Nutzer

**Michael Fauler** ist Facharzt für Physiologie mit Weiterqualifikation in Datenwissenschaften. Tätig als medizinischer Lehrer im deutschsprachigen Raum, primär für MT-Berufe (MTF, MTR, MTL), zusätzlich für DA, SLT und Studierende der Humanmedizin. Lehrgebiete: Funktionsdiagnostik, Physiologie, HNO, Neurologie, Radiologie, Statistik/Datenanalyse, Sonographie/Echokardiographie. Didaktische Klammer: SOFL (Störungsbildorientierte Funktionslehre), klinisches Modell-Framework: PiCA (Pathophysiological Concept Architecture).

## 2. Kommunikationspräferenzen

- Antworten auf Deutsch, Niveau Facharzt für Physiologie
- knapp, präzise, vollständig durchargumentiert; bei längeren Erklärungen primär Bullet-Points
- Quellen für kritische medizinisch-physiologische Aussagen; Existenz prüfen, sonst markieren
- abweichende quellenunabhängige Antwort kennzeichnen, wenn die Quelle ein anderes Ergebnis liefert
- keine Emojis
- Semikolons sparsam
- nicht-übliche Abkürzungen bei Erstnennung in Klammern erläutern, z. B. "DPOAE (Distortion Product Otoacoustic Emissions)"

## 3. Begriffsregelung (zentral)

Konsistent über alle Dokumente; ausführlich im Volltext `sofl/Trias der Befundkategorien.md`.

- **Fachbefund** — Standardbegriff für das MT-eigene, fachlich begründete, qualitätsgesicherte Untersuchungsergebnis
- **Kategorialbefund** — Synonym mit epistemologischer Zuspitzung (Trias-Zugehörigkeit explizit)
- **Vorbefundung** — Tätigkeitsbegriff der MTF nach § 5 Abs. 3 MTBG (rechtlich-prozessual)
- **Vorbefund** — nur bei direktem MTBG-Bezug; sonst durch Fachbefund ersetzen
- **Praxissprache** profession-spezifisch erlaubt: Bildbefund (MTR), Funktionsbefund (MTF), Laborbefund (MTL)
- **Trias-Vollform**:
  - kurz: "struktureller / kompositorischer / funktioneller Fachbefund"
  - präzise: "strukturell-morphologischer / kompositorisch-stofflicher / funktionell-dynamischer Fachbefund"

## 4. Trias der Befundkategorien (zentrale These)

Quelle: `sofl/Trias der Befundkategorien.md` (v0.2)

Die drei MT-Berufe bestimmen sich epistemologisch über die Kategorie ihres Fachbefunds. Diese positive Identitätsbestimmung ersetzt die negative Bestimmung über "Vor-Stufe-zur-ärztlichen-Befundung".

| Kategorie | Profession (Idealtyp) | Charakteristische Frage | Zeitlogik | Tradition |
|---|---|---|---|---|
| strukturell-morphologisch | MTR | Wo befindet sich was, in welcher Form? | Schnittbild eines Zustands | Morgagni, Bichat, Virchow |
| kompositorisch-stofflich | MTL | Was ist in der Probe enthalten, in welcher Menge? | Momentaufnahme zum Entnahmezeitpunkt | Folin, Van Slyke, Astrup; Pasteur, Koch |
| funktionell-dynamisch | MTF | Wie funktioniert das System? | Zeit konstitutives Element | Bernard, Cannon, Selye |

**Ärztliche Diagnose** = kategoriale Synthese der drei Fachbefunde. Eine Diagnose, die sich nur auf eine Kategorie stützt, ist im Regelfall unvollständig.

**Hybridfelder** mit kategorialer Reflexion in der Person:
- in MTR: CMR-Stress-Perfusion, fMRT, dynamische Verfahren, Nuklearmedizin (modalitätenseitig MTR, epistemologisch funktionell)
- in MTL: dynamische Funktionstests (oraler Glukosetoleranztest, ACTH-Test, Wasserdeprivationstest), integrative Parameter (HbA1c, Steroidprofile)

**Institutionelle Verankerung der funktionell-dynamischen Kategorie**: Skandinavische Klinische Physiologie als eigenständige medizinische Disziplin (Schweden 1954 gegründet; Dänemark 1982 mit Nuklearmedizin zusammengelegt; Finnland und Norwegen ab 1960er/1970er; Scandinavian Society of Clinical Physiology and Nuclear Medicine, gegründet 1965). In Deutschland fehlt diese institutionelle Heimat — MTF verteilt sich auf organbezogene klinische Spezialitäten.

**Wert kategorialer Reinheit**: Vermischt eine Profession Kategorien (z. B. funktioneller Fachbefund mit strukturellen Vermutungen), beschädigt sie den eigenen Beitrag und erschwert die ärztliche Synthese.

## 5. Krankheitsprozess-Definition (für SOFL und PiCA)

Quelle: `sofl/Krankheitsprozess Definition.md`

**Kerndefinition**: Ein Krankheitsprozess ist eine zeitlich geordnete, mechanistisch gekoppelte Veränderung eines Funktionssystems oder mehrerer gekoppelter Funktionssysteme, durch die sich Struktur/Topologie, Zustandsdynamik, wirksame Parameter, Eingänge/Randbedingungen oder Stabilitäts-/Attraktorstruktur so verändern, dass pathologische Zustände, klinisch relevante Störungsbilder, persistierende Fehlfunktionen oder rezidivierende pathologische Regime entstehen, aufrechterhalten oder verstärkt werden.

**Vier Klassen krankheitsprozesshafter Veränderungen**:
1. **Klasse 1 — Struktur- oder Topologieänderung**: neue/entfallende Prozesseinheiten oder Kopplungen (z. B. bakterielle Invasion, Embolus, Denervierung, Klappeninsuffizienz)
2. **Klasse 2 — Parametrische/adaptive Veränderung**: Compliance, Leitfähigkeit, Rezeptordichte, Schwellen verändern sich (z. B. Fibrose, Hypertrophie, Remodeling)
3. **Klasse 3 — Änderung des Betriebsregimes/Inputs/Randbedingungen**: extreme Belastungszustände bei erhaltener Struktur (z. B. akuter Stress, Hypoxie, Volumenmangel)
4. **Klasse 4 — Attraktor-/Regimewechsel**: pathologische Stabilitätsverhältnisse (z. B. epileptische Anfälle, Arrhythmien, Bistabilität)

**Hierarchie**: Krankheitsprozess → PPM-Netzwerk → PPM (Pathophysiological Process Module) → Kaskaden. Kaskaden sind atomare lineare DAG-Äste; PPMs verkoppeln sie zu zyklischen Regelkreisen.

**Modellierungsvorschrift**: x'(t) = f(x, u, p, t); y(t) = h(x, u, p, t). Krankheitsprozess wirkt durch Strukturerweiterung, Parameterdynamisierung, pathologische Inputs oder Attraktorwechsel.

## 6. Systemtheoretische Abgrenzung funktionell/strukturell/psychogen

Quelle: `sofl/Systemtheoretische Abgrenzung funktioneller, struktureller und psychogener Störungen.md`

**Primärzuordnung**:
- **strukturelle/organische Störungen** = primär Klasse-1- und Klasse-2-Prozesse
- **funktionelle Störungen** = primär Klasse-3- und Klasse-4-Prozesse
- **psychogene Störungen** = Unterkategorie funktioneller Störungen des Gehirns (interne Repräsentations-, Bewertungs-, Wahrnehmungs- und Gedächtnisprozesse als pathogene Dynamik)

**Wichtige Einschränkungen**:
- "funktionell" bedeutet NICHT "ohne biologische Grundlage", sondern "primär durch Zustandsdynamik/Regulation erklärbar"
- "psychogen" bedeutet NICHT "eingebildet", sondern "interne kognitive/affektive/wahrnehmungsbezogene Prozesse kausal zentral"
- "ungeklärte Störung" ist NICHT automatisch "psychogen"
- Übergänge zwischen den Klassen sind häufig (sekundäre strukturelle Folgen funktioneller Prozesse, sekundäre funktionelle Folgen struktureller Veränderungen)

## 7. Variablen in physiologischen Systemen

Quelle: `sofl/Variablen in physiologischen Systemen.md`

- **Strukturmerkmale**: Stoffmengen, Konzentrationen, Längen, Volumina, Masse, Verbindungen, Elastizitätsmodul
- **Zustandsmerkmale**: Kraft, Beschleunigung, Geschwindigkeit, Position; abgeleitet Druck, Fluss
- Zusätzliche Achsen: beobachtbar/latent; real/virtuell-abstrakt
- **Abstrakte Variablen** definieren sich über ein Beobachtungs-/Messmodell und sind nur durch das messtheoretische Konzept interpretierbar (z. B. Widerstandswerte, Sollwerte, Steuersignale in heuristisch-empirischen Funktionsblock-Modellen)

## 8. Funktionsorientierte Medizin

Quelle: `diagnostik/Funktionsorientierte Medizin - Motivation, Logik und Mission Statement.md`

**Kernunterscheidung**:
- **störungsbildorientierter Ansatz** (funktionsorientiert): patientendatenbezogen; identifiziert klinisch relevante Funktionssysteme, beschreibt deren quantitative Zustandsbilder, plant einen experimental-design-tauglichen diagnostischen Workflow (statisches und dynamisches Verhalten/physiologisches Regime). Operationalisiert in der **Störungsbilddiagnose** (z. B. "diastolische Dysfunktion" statt "diastolische Herzinsuffizienz").
- **krankheitsbildorientierter Ansatz** (nosologisch): de facto populationsdatenbezogen; Mustererkennung als Zuordnung zu einem Populationsdaten-Mittel mit zwangsläufigem statistischem Bias; im clinical reasoning System-1-nah, ohne mehrschichtige Wissensstrukturierung (encapsulated knowledge); strukturell affin.

**Konsequenz**: nosologische Krankheitsbegriffe sind nicht patientenindividuell operationalisierbar, komorbide Einflüsse auf gemeinsame Aspekte des Störungsbildes nicht darstellbar.

## 9. Fundamentale Ansätze der Diagnostik

Quelle: `diagnostik/Fundamentale Ansätze der Diagnostik.md`

1. **Mustererkennung**: Nachweis eines krankheitsbildtypischen Phänotyps; benötigt nosologische Beschreibung und Klassifikation von Krankheitsentitäten.
2. **Modellidentifikation**: Beinhaltet Störungsbildbeschreibung und -analyse basierend auf einem Krankheitsmodell; benötigt die Abbildung von Krankheitsprozessen, Störungsketten, Anpassungsreaktionen und deren Wechselwirkung mit normalen Körperfunktionen.

## 10. Berufsbilder — Kompaktübersicht

Volltexte unter `berufsbilder/`. Reasoning- und Identitätsbestimmung jeweils auf Grundlage der Trias.

### MTF — Medizinische Technologie für Funktionsdiagnostik

Volltext: `berufsbilder/Berufsbild – MTF.md`

- Befundkategorie: **funktionell-dynamisch**; Tätigkeit "Vorbefundung" nach § 5 Abs. 3 MTBG; Ergebnis: funktioneller Fachbefund (Praxissprache: Funktionsbefund)
- Aufgabenfelder: Kardiologie, Angiologie, Pneumologie, HNO, Neurologie (Schlaf nicht ausdrücklich, aber faktisch MTF-vorbehalten)
- Reasoning-Modus: signal-/messwertorientiert, regelkreis- und systemorientiert, funktionell-physiologisch, prozedural-methodisch, präanalytisch
- Reasoning-Architektur: in Deutschland kein etabliertes Modell; international Sonographic Reasoning Method (Thoirs) für sonographische/echokardiographische Anteile, ASET-Stufenmodell (USA) als Verantwortungslogik
- Default-Wissenstiefe: Organ/Organsystem in funktioneller Sicht; vertieft bei verfahrensspezifischen Anforderungen
- Akademisierungsstand: Deutschland schulisch (MTBG seit 1.1.2023); UK BSc Healthcare Science; USA AAS plus ARRT/ASET; Skandinavien als institutioneller Anker (Klinische Physiologie als ärztliche Disziplin)
- Charakteristische Fehlattribution: funktionell auffälliger Befund suggeriert strukturelles Substrat — gehört nicht in den funktionellen Fachbefund

### MTR — Medizinische Technologie für Radiologie

Volltext: `berufsbilder/Berufsbild – MTR.md`

- Befundkategorie: **strukturell-morphologisch** im Idealtyp (mit funktionellen Hybridfeldern: CMR, fMRT, Stress-Perfusion, Nuklearmedizin)
- Tätigkeit: "Beurteilung der Qualität der Ergebnisse" nach § 5 Abs. 2 MTBG (keine ausdrückliche Vorbefundungsklausel); Ergebnis: struktureller Fachbefund (Praxissprache: Bildbefund)
- Drei Großgebiete: bildgebende Diagnostik, Strahlentherapie, Nuklearmedizin
- Zeitliche Architektur **doppelt**: Diagnostik punktuell, Strahlentherapie längsperspektivisch über Wochen
- Reasoning-Architektur: Lundvall 3-Phasen-Modell (planning, image production, evaluation); dual-process theory mit cognitive continuum; PIE/PCE in UK/AUS als formalisierte Vorbefundungs-Architektur
- Advanced-Practice (UK): Reporting Radiographer mit eigenständiger Befundungskompetenz; 4-Stufen-Modell und 4 Pillars of Practice
- Akademisierungsrückstand Deutschlands deutlich (UK BSc, USA AAS/BSc plus ARRT, Österreich/Schweiz BSc)
- Strahlenschutzregime als zusätzliche Strukturebene (StrlSchG, StrlSchV)
- Charakteristische Fehlattribution: strukturelle Auffälligkeit suggeriert funktionelle Konsequenz (z. B. 70%-Stenose ohne hämodynamische Relevanz)

### MTL — Medizinische Technologie für Laboratoriumsanalytik

Volltext: `berufsbilder/Berufsbild – MTL.md`

- Befundkategorie: **kompositorisch-stofflich** im Idealtyp (mit funktionellen Hybridfeldern: dynamische Funktionstests; Sonderfall integrative Parameter wie HbA1c)
- Tätigkeit: "technische Validation" nach § 5 Abs. 1 MTBG; klare Begriffsabgrenzung in der Fachliteratur (Kachler, Halle): technische Validation (MTL) vs. biomedizinische Validation (Arzt); Ergebnis: kompositorischer Fachbefund (Praxissprache: Laborbefund)
- Reasoning-Architektur: am stärksten formalisiert von allen MT-Berufen — Total Testing Process (TTP) nach Lundberg/Plebani, in ISO 15189 verankert; pre-pre, prä-, analytisch, post-, post-post-analytisch
- Reasoning-Modus: präanalytisch-plausibilisierend, analytisch-methodisch, postanalytisch-pattern-matching, mikroskopisch-mustererkennend, statistisch-qualitätsgesichert (Levey-Jennings, Westgard, Sigma)
- Default-Wissenstiefe: vertieft auf molekularer, zellulärer und Stoffwechselebene
- Patient:innenkontakt strukturell fehlend; "Patient hinter der Probe" als didaktische Grundhaltung
- Zusätzliche Normebene: RiliBÄK (verpflichtend via MPBetreibV), DIN EN ISO 15189 (Goldstandard)
- Akademisierungsrückstand: Österreich und Schweiz seit über 20 Jahren akademisiert (BMA), UK BSc Biomedical Science, USA Bachelor MLS
- Charakteristische Fehlattribution: punktueller Wert suggeriert Dauerzustand (z. B. Momentaufnahme ohne Berücksichtigung circadianer Schwankungen)

### ATA — Anästhesietechnische Assistenz

Volltext: `berufsbilder/Berufsbild – ATA.md`

- Therapeutisch-überwachende Profession **neben** der MT-Trias, nicht in ihr; geteiltes funktionell-dynamisches mentales Modell mit MTF, aber kein Fachbefund-Output sondern Verlaufsdokumentation
- Berufsgesetz: ATA-OTA-G (Anästhesietechnische- und Operationstechnische-Assistenten-Gesetz, verkündet 14.12.2019, Verordnung 4.11.2020, in Kraft 1.1.2022, geändert 12.12.2023)
- Ausbildungsumfang: 4720 h (2100 h theoretisch-praktisch, 2500 h praktisch, 120 h Pflegepraktikum)
- Reasoning-Frameworks: ANTS (Anaesthetists' Non-Technical Skills, Fletcher Aberdeen), CRM (Crew Resource Management, Gaba/Howard/Fish Stanford), Situation Awareness (Endsley), Cognitive Aids (Stanford Emergency Manual)
- Kernkompetenz: perioperatives Monitoring, Überwachung der Vitalfunktionen, situative Vigilanz, kommunikatives Teamhandeln in zeitkritischen Situationen
- Verantwortungsstruktur: ausführend gegenüber ärztlich verantwortetem Anästhesiekonzept, mit eigenverantwortlicher Beobachtungs- und Reaktionspflicht

### DA — Diätassistenz

Volltext: `berufsbilder/Berufsbild – DA.md`

- Therapeutisch tätige Profession mit eigenständiger Therapieführung (G-NCP); älteste therapeutische Profession dieser Gruppe in Deutschland
- Berufsgesetz: DiätAssG (8.3.1994, zuletzt geändert 2021), DiätAss-APrV
- Reasoning-Modell: **G-NCP (German Nutrition Care Process)**, VDD-Manual 2015, seit Herbst 2017 verbindlich; fünf Schritte mit kontinuierlichem Re-Assessment (Assessment, Ernährungsdiagnose im PESR-Format, Planung, Durchführung, Evaluation)
- International anschlussfähig (NCP USA, NDCP UK, Diëtistisch ZorgProces NL, Diaetologischer Prozess AT)
- Längsperspektivische Therapieführung über Wochen bis Monate; eigenständige Ernährungsdiagnose neben der ärztlichen Diagnose
- Akademisierung als europäischer Standard (EFAD); in Deutschland Modellstudiengänge verfügbar

### SLT — Sprach-, Sprech-, Stimm- und Schlucktherapie

Volltext: `berufsbilder/Berufsbild – SLT.md`

- Logopäd:innen plus akademische Sprachtherapeut:innen unter heterogenen Qualifikationswegen; gleiche Heilmittelerbringer-Funktion
- Berufsgesetz: LogopG (1980); seit 1.1.2025 reguläre Hochschulausbildung; Neufassung des LogopG für 2026 erwartet
- Reasoning-Modell: **Reasoning-Repertoire nach Beushausen** (basierend auf Higgs/Jones), strukturiert durch ICF/ICF-CY; sechs Reasoning-Formen (prozedural, interaktiv, konditionell, narrativ, pragmatisch-ethisch, didaktisch)
- Längsperspektivische Therapieführung über Wochen bis Monate; eigenständige sprachtherapeutische Diagnostik
- Störungsachsen: Sprache, Sprechen, Stimme, Schlucken, Hören (im therapeutischen Kontext), Kommunikation (AAC, Autismus-Spektrum)

### Methodische Bezugsdokumente

- **`berufsbilder/Berufsbild – Template.md`** — Vorlage für neue Berufsbilder
- **`berufsbilder/Ausbildungsgang-spezifische Dokumenterstellung.md`** — Bezugsdokument: Anforderungsprofil je Ausbildungsgang als Voraussetzung für need-to-know vs. nice-to-know in PiCA-Anwendung
- **`berufsbilder/Typologische Achsen der Berufsbilder.md`** — neun Achsen (A–I) für vergleichende Berufsbild-Analyse: Reasoning-Architektur, zeitliche Architektur, Akteursrolle, berufseigene Diagnose/Bewertung, Verhältnis zur ärztlichen Diagnose, Default-Wissenstiefe, Reasoning-Modus, Klassifikationsrahmen, Befundkategorie/epistemologische Position
- **`berufsbilder/MT-Familie – Synthese.md`** — synthetische Sicht auf die MT-Trias: gemeinsame rechtliche Architektur, internationale Reasoning-/Stufenmodelle, Vorschlag eines MT-übergreifenden 6-Phasen-Modells (Auftragsverstehen, Indikations-/Sicherheitsprüfung, Vorbereitung/Durchführung, berufseigene Bewertungstätigkeit, Übergabe, Reflexion)

## 11. Verweise auf Volltexte (raw URLs)

Basis: `https://raw.githubusercontent.com/mfauler/general-knowledge-vault/main/`

**Berufsbilder:**
- `berufsbilder/Berufsbild – ATA.md`
- `berufsbilder/Berufsbild – DA.md`
- `berufsbilder/Berufsbild – MTF.md`
- `berufsbilder/Berufsbild – MTR.md`
- `berufsbilder/Berufsbild – MTL.md`
- `berufsbilder/Berufsbild – SLT.md`
- `berufsbilder/Berufsbild – Template.md`
- `berufsbilder/Typologische Achsen der Berufsbilder.md`
- `berufsbilder/MT-Familie – Synthese.md`
- `berufsbilder/Ausbildungsgang-spezifische Dokumenterstellung.md`

**SOFL:**
- `sofl/Krankheitsprozess Definition.md`
- `sofl/Systemtheoretische Abgrenzung funktioneller, struktureller und psychogener Störungen.md`
- `sofl/Trias der Befundkategorien.md`
- `sofl/Variablen in physiologischen Systemen.md`

**Diagnostik:**
- `diagnostik/Fundamentale Ansätze der Diagnostik.md`
- `diagnostik/Funktionsorientierte Medizin - Motivation, Logik und Mission Statement.md`

URLs müssen URL-encoded werden, wenn sie Leerzeichen oder Sonderzeichen enthalten (z. B. `%20` für Leerzeichen, `%E2%80%93` für den En-Dash "–").

## 12. Externe verwandte Repositories

- **PiCA** (PPMs, Kaskaden, Illness Scripts, Variablen): `https://github.com/mfauler/pica-knowledge-base`
