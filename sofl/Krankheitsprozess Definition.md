# Ressource: Universelle Definition des Krankheitsprozesses für SOFL und PiCA

## Status und Zweck

Diese Ressource definiert den Begriff **Krankheitsprozess** so, dass er

- innerhalb von **SOFL** konsistent zur Beschreibung klinisch relevanter Störungsbilder genutzt werden kann
- innerhalb von **PiCA** direkt als Grundlage für **pathophysiologische Kaskaden** und **pathophysiologische Prozess-Module (PPM)** dient
- zwischen beiden Projekten begrifflich identisch bleibt
- für **Skill-Definitionen**, **KI-Agenten**, **Lehrmaterialien**, **Fallanalysen** und **mathematische Modellierungen** gleichermaßen verwendbar ist

Die Definition ist bewusst **mechanistisch**, **systembezogen** und **modellierungsnah** formuliert. Sie soll nicht nur sprachliche Konsistenz sichern, sondern aus einer textlichen Beschreibung möglichst direkt eine **Modellierungsvorschrift** ableitbar machen.

---

## 1. Zielsetzung der Krankheitsprozess-Definition

### 1.1 Begriffliche Einheitlichkeit

Der Begriff soll in allen Projekten dieselbe Bedeutung haben.

### 1.2 Trennung von Diagnoseetikett und Mechanismus

Eine Krankheit soll nicht primär über ihren Namen, sondern über den zugrunde liegenden **mechanistischen Ablauf** beschrieben werden.

### 1.3 Anschlussfähigkeit an SOFL

Der Krankheitsprozess ist die **mechanistische Binnenstruktur eines Störungsbildes**.

### 1.4 Anschlussfähigkeit an PiCA

PiCA benötigt beschreibbare, wiederverwendbare und modularisierbare pathophysiologische Kaskaden.

### 1.5 Explizierung der Modellstruktur

Die Definition soll dazu zwingen, in jeder Beschreibung ausdrücklich zu unterscheiden zwischen Zustandsgrößen (latent oder beobachtbar), Parametern, Eingängen und Belastungen, strukturellen Kopplungen, Rückkopplungen, Schwellenbedingungen, Stabilitätsverhältnissen und klinisch beobachtbaren Outputs.

### 1.6 Direkte Ableitbarkeit einer Modellierungsvorschrift

Aus einer Beschreibung eines Krankheitsprozesses soll möglichst direkt hervorgehen, welche Variablen ins Modell aufgenommen werden müssen, welche Beziehungen kausal oder dynamisch relevant sind, welche Größen langsam oder schnell variieren, ob ein reines ODE-Modell ausreicht.

---

## 2. Terminologische Konventionen und Grundbegriffe

### 2.1 Krankheitseinheit

Klinisch oder nosologisch benannte Entität. Benennungsebene, keine mechanistische Beschreibung.

### 2.2 Funktionssystem

Mechanistisch integriertes Teilsystem des Organismus, das als strukturelles Korrelat eines physiologischen Mechanismus aufgefasst wird.

### 2.3 Störungsbild

Klinisch oder funktionell erkennbare Erscheinungsform einer gestörten Systemdynamik. Beobachtungs- und Beschreibungsebene.

### 2.4 Physiologische und pathophysiologische Kaskade

Lineare, gerichtete, azyklische Sequenz mechanistisch gekoppelter Zustandsänderungen innerhalb oder zwischen Funktionssystemen. Entspricht einem Ast in einem gerichteten azyklischen Graphen (DAG). Eigenständige, benannte, wiederverwendbare Bausteine. Rückkopplungsschleifen entstehen ausschließlich auf der PPM-Ebene durch Kombination gegenläufiger Kaskaden.

Ablageort: Obsidian Vault, Verzeichnis `Kaskaden/`, Dateiname: `Kaskade – [Name].md`

### 2.5 Pathophysiologisches Prozess-Modul (PPM)

Formal beschreibbare modulare Komposition aus einer oder mehreren Kaskaden. Stellt die mechanistisch geschlossene Darstellung eines abgegrenzten Regulationszusammenhangs dar. Im Unterschied zu einer Kaskade darf ein PPM Zyklen enthalten (negative oder positive Feedback-Schleifen).

Ablageort: Obsidian Vault, Verzeichnis `PPM/`, Dateiname: `PPM – [Name].md`

### 2.6 Krankheitsprozess

Zeitlich geordnete mechanistische Veränderung eines oder mehrerer Funktionssysteme, durch die pathologische Zustände oder klinisch relevante Störungsbilder entstehen, persistieren oder rezidivieren.

### 2.7 Pathologischer Zustand

Zustand des Funktionssystems, in dem Regelgrößen, Kopplungen oder Betriebsregime den physiologischen Funktionsbereich so verlassen haben, dass klinisch relevante Fehlfunktion, Beschwerde oder Schädigung resultiert.

### 2.8 Pathologisches Regime

Dynamischer Betriebsmodus eines Funktionssystems, der über bloße Einzelabweichungen hinausgeht und ein charakteristisches, krankheitsrelevantes Systemverhalten erzeugt.

---

## 3. Definition des Krankheitsprozesses

### 3.1 Kerndefinition

Ein **Krankheitsprozess** ist eine zeitlich geordnete, mechanistisch gekoppelte Veränderung eines Funktionssystems oder mehrerer gekoppelter Funktionssysteme, durch die sich

- die Struktur oder Topologie des Systems
- die Dynamik der Zustandsgrößen
- die wirksamen Parameter
- die Eingänge oder Randbedingungen
- oder die Stabilitäts- und Attraktorstruktur

so verändern, dass pathologische Zustände, klinisch relevante Störungsbilder, persistierende Fehlfunktionen oder rezidivierende pathologische Regime entstehen, aufrechterhalten oder verstärkt werden.

---

## 4. Klassen krankheitsprozesshafter Veränderungen

### 4.1 Klasse 1: Struktur- oder Topologieänderung

Veränderung der Modellstruktur selbst: neue Prozesseinheiten, Verlust bestehender Prozesseinheiten, neue Kopplungen, Wegfall von Kopplungen, Umlenkung, Fehlkopplung, Kurzschluss, Barriereverlust.

Beispiele: bakterielle Invasion mit Toxinsekretion, Tumorklon, Embolus, Denervierung, Shunt, Klappeninsuffizienz, Membranruptur.

Modelltheoretisch: Erweiterung, Reduktion oder Umverdrahtung des Gleichungssystems.

### 4.2 Klasse 2: Parametrische oder adaptive Veränderung

Grundstruktur erhalten, aber Eigenschaften verändern sich quantitativ oder funktionell.

Beispiele: Compliance-Änderung, Leitfähigkeitsänderung, Fibrose, Hypertrophie, Gefäßremodeling, Rezeptordichte, Enzymaktivität, Reizschwelle, chronische Entzündungsbereitschaft.

Modelltheoretisch: Parameter wird zu langsamer Zustandsgröße mit eigener Dynamik.

### 4.3 Klasse 3: Änderung des Betriebsregimes, der Eingänge oder der Randbedingungen

Struktur erhalten, aber System gerät in extremen oder unphysiologisch belastenden Betriebszustand.

Beispiele: akuter Stress, Volumenmangel, Hypoxie, Fieber, schwere metabolische Entgleisung, extreme Belastung, massive Sympathikusaktivierung, veränderte hormonelle Steuerung.

Modelltheoretisch: veränderte Inputs, Belastungen, Randbedingungen, Führungsgrößen oder Sollwerte.

Allostase und allostatische Last spielen hier eine Rolle.

### 4.4 Klasse 4: Attraktor-, Regime- oder Stabilitätswechsel

System besitzt mehrere mögliche stabile oder quasi-stabile Zustände oder geht in pathologischen Oszillationsmodus über.

Beispiele: epileptische Anfälle, Herzrhythmusstörungen, periodische Paralysen, paroxysmale Funktionsstörungen, hysteretische Umschläge, pathologische Grenzzyklen.

Modelltheoretisch: Stabilitäts- und Attraktorstruktur des Zustandsraums; Bifurkationen, Basins of attraction, hysteretische Übergänge.

### Wichtiger Hinweis

Klassen 1–3 beschreiben Arten von Modelländerungen oder Störungsquellen. Klasse 4 beschreibt eine Eigenschaft der Systemdynamik. In realen Krankheitsprozessen verschieben sich Struktur, Parameter oder Inputs, dadurch verändern sich die Stabilitätsverhältnisse, anschließend kann ein pathologischer Attraktor erreicht werden. Klasse 4 ist daher als Dynamikebene stets mitzudenken.

---

## 5. Minimalstruktur einer Krankheitsprozessbeschreibung

Eine brauchbare Krankheitsprozessbeschreibung soll mindestens folgende Fragen beantworten:

- Referenzsystem (welches Funktionssystem ist primär betroffen, welche gekoppelten Nebensysteme sind relevant)
- Ausgangszustand (funktioneller Referenzzustand, regulierte oder stabile Größen)
- Auslöser oder Eintrittsbedingung
- Primäre Veränderung (welche der Klassen 1–4 liegt vor)
- Mechanistische Folgeglieder (kausale Beziehungen, Rückkopplungen)
- Klinische oder funktionelle Outputs
- Zeitstruktur (schnelle vs. langsame Anteile, diskrete Ereignisse, Schwellen, Verzögerungen)
- Reversibilität und Persistenz

---

## 6. Krankheitsprozess und mathematische Modellierung

### 6.1 Grundidee

Ein physiologisches Grundmodell:

```text
x'(t) = f(x, u, p, t)
y(t)  = h(x, u, p, t)
```

mit `x` = Zustandsvariablen, `u` = Eingänge, `p` = Parameter, `y` = beobachtbare Outputs.

### 6.2 Vier Grundoperationen krankheitsprozesshafter Modelländerung

- A. Strukturänderung: zusätzliche Zustandsvariablen `z` oder neue Kopplungen
- B. Parameterdynamisierung: feste Parameter werden zu langsam veränderlichen Größen
- C. Änderung von Inputs oder Randbedingungen
- D. Regime- und Attraktorwechsel: qualitative Dynamikänderung

### 6.3 Erweiterte Modellformen

Nicht jeder Krankheitsprozess ist mit einem glatten ODE-System vollständig beschrieben. Zusätzliche Modellbausteine: hybride Modelle, Delay-Differentialgleichungen, PDE-Modelle, stochastische Modelle, agentenbasierte Modelle.

---

## 7. Modellierungsvorschrift aus einer Krankheitsprozessbeschreibung

Schritte:

1. Systemgrenzen festlegen
2. Zustandsgrößen identifizieren (Konzentrationen, Volumina, Drucke, Spannungen, Öffnungszustände, Erregbarkeiten, Zellzahlen, Reservoirgrößen)
3. Parameter identifizieren (Compliance, Leitfähigkeit, maximale Enzymaktivität, Rezeptordichte, Gewebesteifigkeit, Schwellwerte, Diffusionskoeffizienten)
4. Inputs und Randbedingungen identifizieren
5. Kausalkette formulieren
6. Rückkopplungen markieren (negative, positive, kompensatorische, dekompensierende)
7. Ereignisse, Schwellen und Regimewechsel markieren
8. Beobachtbare Outputs definieren (Symptome, Vitalparameter, Laborwerte, Funktionsmessungen, Bildgebungsmerkmale, Belastungsreaktionen)
9. Zeitmaßstäbe trennen (schnell, mittel, langsam)

---

## 8. Formale Darstellungslogik für PPM

### 8.1 Empfohlenes PPM-Schema

- PPM-Name
- Referenzsystem
- Auslöser
- Primäre Veränderung (Klasse 1–4)
- Relevante Zustandsgrößen
- Relevante Parameter
- Inputs und Belastungen
- Kaskadenkomponenten (Wikilinks auf `Kaskaden/Kaskade – [Name].md`)
- Zyklische Kopplung (neg./pos. Feedback)
- Mechanistische Kette (Gesamtblockdiagramm)
- Rückkopplungen
- Schwellen oder Regimewechsel
- Klinische Outputs
- Reversibilität
- Modellhinweis (ODE, ODE plus langsame Parameterdynamik, hybrides Modell, stochastisch getriggertes Regimewechselmodell)

---

## 9. Abgrenzungen

- Krankheitsprozess ≠ Krankheitseinheit (Mechanismus vs. Benennung)
- Krankheitsprozess ≠ Symptom (Mechanismus vs. Output)
- Krankheitsprozess ≠ Risikofaktor (Mechanismus vs. Wahrscheinlichkeitsmodifikation)
- Krankheitsprozess ≠ Befund (Mechanismus vs. Beobachtung)

---

## 10. Heuristische Leitregeln

- mechanistisch statt etikettenhaft formulieren
- Richtung und Vermittlung angeben
- Ursache, Verstärker und Folge trennen
- Struktur, Parameter, Input und Dynamik nicht vermischen
- Zeitlichkeit explizit machen (akut, subakut, chronisch, episodisch, rezidivierend, persistent)
- Beobachtbarkeit separat benennen
- terminologische Sparsamkeit wahren

---

## 11. Kompakte Arbeitsdefinition für Skills und Agenten

> Ein Krankheitsprozess ist eine zeitlich geordnete mechanistische Veränderung eines Funktionssystems, bei der sich Struktur oder Topologie des Systems, Parameter, Eingänge, Zustandsdynamik oder Stabilitätsstruktur so verändern, dass klinisch relevante pathologische Zustände oder Störungsbilder entstehen, persistieren oder wiederkehren.

---

## 12. Kompakte Modellierungsdefinition für PPM

> Ein PPM beschreibt einen abgegrenzten Regulationszusammenhang als Komposition benannter Kaskaden so, dass Auslöser, Systemgrenzen, Zustandsgrößen, Parameter, Inputs, mechanistische Kopplungen (linear in Kaskaden, zyklisch im PPM), Rückkopplungen, Schwellen, Zeitmaßstäbe und klinische Outputs explizit benannt und formal modellierbar werden.

---

## 13. Kurzbeispiele

- Beispiel A: Bakterielle Invasion mit Toxinbildung → Klasse 1 (Strukturänderung)
- Beispiel B: Chronische Druckbelastung mit Remodeling → Klasse 2 (parametrisch)
- Beispiel C: Akuter extremer Stresszustand → Klasse 3 (Betriebsregime)
- Beispiel D: Epileptischer Anfall → Klasse 4 (Attraktorwechsel)

---

## 14. Schlussformel

Der Krankheitsprozessbegriff dient in SOFL und PiCA als gemeinsamer mechanistischer Referenzbegriff. Hierarchie: **Krankheitsprozess → PPM-Netzwerk → PPM → Kaskaden**. Kaskaden sind die atomaren Bausteine; PPMs verkoppeln sie zu Regelkreisen; PPM-Netzwerke beschreiben das fault-Slot eines Illness-Scripts.
