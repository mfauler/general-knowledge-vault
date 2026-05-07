# general-knowledge-vault

Spiegel zentraler Konzeptdokumente aus dem Obsidian-Vault von Michael Fauler.
Zweck: Bereitstellung als Kontext für Claude.ai (Web/Android) via `web_fetch`.

**Letzte Aktualisierung:** 2026-05-07

---

## Einstiegspunkt

Die konsolidierte Kontextdatei für Claude.ai:

```
https://raw.githubusercontent.com/mfauler/general-knowledge-vault/main/_KONTEXT.md
```

---

## Struktur

```
_KONTEXT.md                         Konsolidierter Index (Persona, Begriffe, Konzepte, Verweise)
README.md                           Diese Datei

berufsbilder/
  berufsbild-mtf.md                 MTF – Medizinische Technologie Funktionsdiagnostik (v0.4)
  berufsbild-mtr.md                 MTR – Medizinische Technologie Radiologie (v0.2)
  berufsbild-mtl.md                 MTL – Medizinische Technologie Laboratoriumsanalytik (v0.2)
  berufsbild-ata.md                 ATA – Anästhesietechnische Assistenz (v0.2)
  berufsbild-da.md                  DA – Diätassistenz (v0.1)
  berufsbild-slt.md                 SLT – Sprachtherapie/Logopädie (v0.1)
  mt-familie-synthese.md            Synthese der drei MT-Profile (v0.2)
  typologische-achsen-der-berufsbilder.md  Methodisches Bezugsdokument (v0.3)
  ausbildungsgang-spezifische-dokumenterstellung.md
  berufsbild-template.md            Template für neue Berufsbilder

sofl/
  trias-der-befundkategorien.md     Zentrale These: strukturell / kompositorisch / funktionell (v0.2)
  krankheitsprozess-definition.md   Definition Krankheitsprozess für SOFL und PiCA
  systemtheoretische-abgrenzung.md  Abgrenzung funktionell / strukturell / psychogen
  variablen-in-physiologischen-systemen.md

diagnostik/
  fundamentale-ansaetze-der-diagnostik.md   Mustererkennung vs. Modellidentifikation
  funktionsorientierte-medizin.md           Störungsbild- vs. Krankheitsbild-orientierter Ansatz
```

---

## Kerninhalte

- **Trias der Befundkategorien**: strukturell-morphologisch (MTR) · kompositorisch-stofflich (MTL) · funktionell-dynamisch (MTF); ärztliche Diagnose als Synthese; institutionelle Verankerung via Klinische Physiologie Skandinavien
- **SOFL**: Störungsbildorientierte Funktionslehre als didaktische Operationalisierung der funktionellen Befundkategorie; Krankheitsprozess-Klassen 1-4; Kaskaden und PPMs als Bausteine
- **Funktionsorientierte Medizin**: störungsbildorientiert (patientendatenbasiert) vs. krankheitsbildorientiert (populationsdatenbasiert); Modellidentifikation vs. Mustererkennung
- **Berufsbilder**: MTF, MTR, MTL (MT-Familie nach MTBG), ATA (ATA-OTA-G), DA (DiätAssG), SLT (LogopG); Reasoning-Modelle, Befundkategorien, gesetzliche Grundlagen, internationale Einordnung

---

## Synchronisierung

Synchronisierung über Slash-Command `/update-claude-web-context` in Claude Code (Obsidian-Vault-Sitzung).
