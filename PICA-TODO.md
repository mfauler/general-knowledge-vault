---
title: "PiCA — Offene Aufgaben und Entwicklungsstand"
erstellt: 2026-06-16
aktualisiert: 2026-06-16
tags: [pica, todo, index]
---

# PiCA-TODO — Offene Aufgaben und Entwicklungsstand

## Verwendung dieses Dokuments

Dieses Dokument ist das zentrale Arbeitsregister für das **PiCA-Projekt** (Physiologisch-integrierte Curriculums-Architektur) im GitHub-Vault `mfauler/general-knowledge-vault`.

**Konventionen:**

- `[ ]` — offen, noch nicht begonnen
- `[~]` — in Bearbeitung
- `[x]` — abgeschlossen; Verweis auf Zieldokument in Klammern
- Einträge werden **nicht gelöscht**, sondern als `[x]` markiert — der Erledigungsverlauf bleibt erhalten.
- Neue Einträge werden mit Datum ergänzt (Format: `YYYY-MM-DD`).
- Jeder Eintrag benennt den **Dokumenttyp**: PPM, Kaskade, Illness Script (IS), Variable, Klinik-DD, Lehrdokument.

**Dieses Dokument wird von Claude in Claude.ai-Gesprächen aktuell gehalten**, sofern das Gespräch auf ein ausarbeitungsbedürftiges Störungs- oder Krankheitsbild stößt. Claude aktualisiert es per GitHub Contents API und trägt neue Einträge unter der passenden Kategorie ein.

---

## Klinik / Differenzialdiagnosen

Klinisch-pathophysiologische Falldiskussionen und DD-Dokumente. Primär als Ausgangsmaterial für Illness Scripts und PPMs.

- [x] **DD posttraumatischer Kopfschmerz, Schwindel, Vertikalnystagmus** *(2026-06-16)*
  → [klinik/dd-posttraumatischer-kopfschmerz-schwindel-vertikalnystagmus.md](https://raw.githubusercontent.com/mfauler/general-knowledge-vault/main/klinik/dd-posttraumatischer-kopfschmerz-schwindel-vertikalnystagmus.md)
  — Führende Hypothese traumatische intrakranielle Hypotension; Vertikalnystagmus als zentraler Anker; DD VBI, zervikogener Kopfschmerz/Schwindel, BPPV, Migräne.

---

## Illness Scripts (IS)

- [ ] **Traumatische intrakranielle Hypotension / spinales Liquorleck** *(2026-06-16)*
  — Enabling conditions: Rückentrauma mit Hyperextension über Hypomochlion; duraler Einriss thorakolumbal. Fault-slot: Liquorvolumenverlust → brain sag → trigeminale/autonome/zerebellookuläre Dysfunktion. Consequences: orthostatischer Kopfschmerz, Schwindel, Vertikalnystagmus, dysautonome Symptome. Basis: DD-Dokument vorhanden (s. o.).

- [ ] **Zervikogener Kopfschmerz** *(2026-06-16)*
  — Enabling conditions: Nackentrauma, HWS-Degeneration, subokzipitale Muskelpathologie. Fault-slot: trigeminozervikale Konvergenz C1–C3 / Ncl. spinalis trigemini. Consequences: okzipitaler/retroorbitaler Kopfschmerz, bewegungs-/haltungsabhängig.

- [ ] **Zervikogener Schwindel** *(2026-06-16)*
  — Enabling conditions: obere HWS-Pathologie (Trauma, Degeneration, Instabilität). Fault-slot: Dysfunktion der zervikalen Propriozeption → sensory mismatch in Vestibulariskernen. Consequences: Benommenheitsschwindel, positionsabhängig, autonome Begleitsymptome. Cave: Ausschlussdiagnose ohne Goldstandard.

- [ ] **Vertebralisdissektion, traumatisch** *(2026-06-16)*
  — Enabling conditions: zervikale Hyperextension/Rotation; Bindegewebsschwäche. Fault-slot: Intimaeinriss → intramurales Hämatom → luminale Stenosierung / Emboliequelle. Consequences: posteriore Zirkulationsischämie, Horner-Syndrom, Nackenschmerz. Akutes „can't miss" bei zervikaler Traumakomponente.

- [ ] **Rotatorische Vertebralisokklusion (Bow-Hunter-Syndrom)** *(2026-06-16)*
  — Enabling conditions: atlantoaxiale Hypermobilität oder knöcherne Variante. Fault-slot: intermittierende mechanische Vertebralisokklusion bei Kopfrotation/-extension. Consequences: rotationsgetriggerte posteriore TIA, Schwindel, Nystagmus. Diagnose: dynamische TCD (transkranielle Dopplersonographie) oder DSA in Provokationsstellung.

---

## PPMs (Pathophysiologische Prozess-Module)

- [ ] **PPM: Monro-Kellie-Dynamik bei Liquorvolumenverlust** *(2026-06-16)*
  — Zustandsvariablen: intrakranieller Druck (ICP), Liquorvolumen, venöses Blutvolumen, Hirnparenchymvolumen. Kaskaden: Liquorverlust → venöse Engorgement-Kaskade; Liquorverlust → brain-sag-Kaskade (kaudaler Hirnstammverlagerung). Ausgangspunkt: DD-Dokument.

- [ ] **PPM: Trigeminozervikale Konvergenz / nozizeptive Sensitivierung** *(2026-06-16)*
  — Zustandsvariablen: zentrale Sensitivierung Ncl. spinalis trigemini, C1–C3-Afferenzrate, Schmerzschwelle. Kaskaden: Nackentrauma → periphere Sensitivierung → zentrale Sensitivierung. Verwendung in IS: zervikogener Kopfschmerz.

- [ ] **PPM: Zervikale Propriozeptionsdysfunktion → vestibulär-visueller Mismatch** *(2026-06-16)*
  — Zustandsvariablen: zervikale Afferenzrate (C1–C3 Muskelspindeln), vestibulärer Input, visueller Input, Kohärenzindex. Kaskaden: Muskelspasmus/Gelenkdysfunktion → Afferenzdysfunktion → Mismatch in Vestibulariskernen. Ausgangspunkt: IS zervikogener Schwindel.

- [ ] **PPM: Hirnstammtraktion → autonome Dysfunktion** *(2026-06-16)*
  — Zustandsvariablen: axiale Hirnstammdislokation, Aktivität NTS/dorsaler Vaguskern/RVLM, Herzfrequenz, Blutdruck. Kaskaden: brain sag → Kompression autonomer Kerngebiete → Dysautonomie. Ausgangspunkt: DD-Dokument, Abschnitt dysautonome Symptome.

- [ ] **PPM: Zerebellookuläre Dysfunktion → Vertikalnystagmus** *(2026-06-16)*
  — Zustandsvariablen: Aktivität Flokkulus/Paraflokkulus, GABA-erge Inhibition der Vestibulariskerne, okulomotorische Integrator-Output. Kaskaden: Hirnstammtraktion → Flokkulusdysfunktion → Downbeat-Nystagmus; Medulla-Affektion → Upbeat-Nystagmus. Kerndifferenzial: peripher vs. zentral via Fixationssuppression und HIT.

---

## Kaskaden

- [ ] **Kaskade: Duraleinriss → Liquoraustritt → ICP-Abfall** *(2026-06-16)*
  — Trigger: mechanisches Trauma (Hyperextension). Zwischenzustände: Duraruptur → epiduraler Liquoreinstrom → spinaler Druckausgleich → ICP-Abfall. Terminaler Output: intrakranielle Hypotension.

- [ ] **Kaskade: ICP-Abfall → brain sag → Hirnstammtraktion** *(2026-06-16)*
  — Trigger: Liquorvolumenverlust. Zwischenzustände: Auftriebsverlust → kaudales Absacken Hirnstamm/Kleinhirn → Zug an Brückenvenen + Duraadhäsionen + Hirnnerven. Terminaler Output: multifokale Dysfunktion (Kopfschmerz, Nystagmus, Dysautonomie).

- [ ] **Kaskade: Vertebralis-Intimaeinriss → thromboembolische posteriore Ischämie** *(2026-06-16)*
  — Trigger: Scherkraft zervikal. Zwischenzustände: Intimariss → subintimales Hämatom → Lumeneinengung → lokale Thrombose oder Embolisierung. Terminaler Output: posteriore Zirkulationsischämie.

---

## Variablen (Deklarationsbedarf)

- [ ] **ICP** (intrakranieller Druck) — Zustandsvariable, Einheit mmHg / cmH₂O, Normbereich liegend 7–18 cmH₂O *(2026-06-16)*
- [ ] **Liquorvolumen** — Strukturvariable, ca. 150 ml gesamt; spinal ca. 75 ml *(2026-06-16)*
- [ ] **Axiale Hirnstammdislokation (brain sag)** — virtuelle/latente Zustandsvariable, messbar über pontomamilläre Distanz im MRT *(2026-06-16)*
- [ ] **Zervikale Propriozeptionsafferenzrate C1–C3** — latente Zustandsvariable *(2026-06-16)*

---

## Lehrdokumente / Unterrichtsmaterial

*(Einträge folgen, wenn Lehrmaterialien aus PiCA-Inhalten entwickelt werden)*

---

## Erledigte Einträge (Archiv)

*Abgeschlossene Einträge werden hier gesammelt, sobald sie als `[x]` markiert wurden.*

---

*Zuletzt aktualisiert: 2026-06-16 — automatisch gepflegt via Claude / GitHub Contents API*
