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

Die Definition des Krankheitsprozesses verfolgt mehrere zusammenhängende Ziele.

### 1.1 Begriffliche Einheitlichkeit

Der Begriff soll in allen Projekten dieselbe Bedeutung haben. Dadurch werden Widersprüche vermieden zwischen

- Lehrtexten
- Skill-Definitionen
- Agentenlogiken
- Fallbeschreibungen
- PPM-Darstellungen
- mathematischen Modellen

### 1.2 Trennung von Diagnoseetikett und Mechanismus

Eine Krankheit soll nicht primär über ihren Namen, sondern über den zugrunde liegenden **mechanistischen Ablauf** beschrieben werden. Der Krankheitsprozessbegriff trennt daher die Ebene der **Pathogenese** von der Ebene der bloßen **nosologischen Benennung**.

### 1.3 Anschlussfähigkeit an SOFL

SOFL arbeitet mit **Störungsbildern** und mit der Analyse von Funktionssystemen. Dafür ist ein Begriff erforderlich, der erklärt,

- wodurch ein Störungsbild entsteht
- welche Mechanismen es aufrechterhalten
- welche klinisch beobachtbaren Folgen daraus resultieren
- welche diagnostischen Zugänge funktionell sinnvoll sind

Der Krankheitsprozess ist damit die **mechanistische Binnenstruktur eines Störungsbildes**.

### 1.4 Anschlussfähigkeit an PiCA

PiCA benötigt beschreibbare, wiederverwendbare und modularisierbare pathophysiologische Kaskaden. Der Krankheitsprozessbegriff soll daher so gefasst sein, dass daraus **PPM** abgeleitet werden können, die

- formal beschreibbar sind
- zwischen Fällen wiederverwendbar sind
- miteinander kombiniert werden können
- prinzipiell in Rechenmodelle, ODE-Systeme oder hybride Modelle überführt werden können

### 1.5 Explizierung der Modellstruktur

Die Definition soll dazu zwingen, in jeder Beschreibung ausdrücklich zu unterscheiden zwischen

- Zustandsgrößen, latent oder beobachtbar
- Parametern
- Eingängen und Belastungen
- strukturellen Kopplungen
- Rückkopplungen
- Schwellenbedingungen
- Stabilitätsverhältnissen
- klinisch beobachtbaren Outputs

Dadurch werden mechanistische Beschreibungen präzise, prüfbar und modellierbar.

### 1.6 Direkte Ableitbarkeit einer Modellierungsvorschrift

Aus einer Beschreibung eines Krankheitsprozesses soll möglichst direkt hervorgehen,

- welche Variablen in ein Modell aufgenommen werden müssen
- welche Beziehungen kausal oder dynamisch relevant sind
- welche Größen langsam oder schnell variieren
- ob ein reines ODE-Modell ausreicht oder ob diskrete Ereignisse, Verzögerungen, Räumlichkeit oder Stochastik ergänzt werden müssen

Der Krankheitsprozessbegriff ist damit nicht nur ein didaktischer, sondern auch ein **modelltheoretischer Ordnungsbegriff**.

---

## 2. Terminologische Konventionen und Grundbegriffe

Damit der Begriff in SOFL und PiCA konsistent verwendet werden kann, gelten in dieser Ressource die folgenden Konventionen.

### 2.1 Krankheitseinheit

Eine **Krankheitseinheit** ist eine klinisch oder nosologisch benannte Entität. Sie ist eine Benennungsebene und keine mechanistische Beschreibung.

### 2.2 Funktionssystem

Ein **Funktionssystem** ist ein mechanistisch integriertes Teilsystem des Organismus, das als strukturelles Korrelat eines physiologischen Mechanismus aufgefasst wird. Es umfasst die für diesen Mechanismus relevanten Strukturen, Zustandsgrößen und Kopplungen.

Kennzeichen eines Funktionssystems sind

- funktional zusammengehörige Strukturen
- charakteristische Zustandsgrößen
- regulative Kopplungen und Rückkopplungen
- typische Eingänge, Belastungen und Outputs
- physiologisch beschreibbare Zustandsübergänge

### 2.3 Störungsbild

Ein **Störungsbild** ist die klinisch oder funktionell erkennbare Erscheinungsform einer gestörten Systemdynamik. Es ist eine Beobachtungs- und Beschreibungsebene und nicht identisch mit dem vollständigen Mechanismus.

Ein Störungsbild kann sich äußern durch

- Symptome
- klinische Zeichen
- Messbefunde
- funktionelle Einschränkungen
- charakteristische Belastungsreaktionen

### 2.4 Physiologische und pathophysiologische Kaskade

Eine **Kaskade** (physiologisch oder pathophysiologisch) ist eine **lineare, gerichtete, azyklische** Sequenz mechanistisch gekoppelter Zustandsänderungen innerhalb oder zwischen Funktionssystemen. Sie entspricht strukturell einem **Ast in einem gerichteten azyklischen Graphen (DAG)**: Es gibt keine Rückschleifen – jede Zustandsänderung propagiert strikt in Richtung des terminalen Outputs.

Eine Kaskade besteht aus:

- einem definierten **Trigger** (Eingangsvariable)
- einer geordneten Folge mechanistisch gekoppelter **Zwischenzustände**
- einem **terminalen Output** (Ausgangsvariable)

Kaskaden sind **eigenständige, benannte, wiederverwendbare Bausteine**. Sie können in mehreren PPMs als Komponenten referenziert werden. Rückkopplungsschleifen und Zyklen entstehen ausschließlich auf der PPM-Ebene durch Kombination gegenläufiger Kaskaden – eine einzelne Kaskade enthält keine Zyklen.

Eine **pathophysiologische Kaskade** beschreibt eine funktional gestörte oder krankheitsrelevante Kette; eine **physiologische Kaskade** beschreibt den entsprechenden Normalablauf. **Kompensatorische Kaskaden** bilden eine dritte Subklasse und sind typischerweise gegenläufig zur pathophysiologischen Kaskade gerichtet.

**Ablageort:** Obsidian Vault, Verzeichnis `Kaskaden/`, Dateiname: `Kaskade – [Name].md`

### 2.5 Pathophysiologisches Prozess-Modul (PPM)

Ein **PPM** ist eine formal beschreibbare **modulare Komposition aus einer oder mehreren Kaskaden**. Es stellt die mechanistisch geschlossene Darstellung eines abgegrenzten Regulationszusammenhangs dar – nicht die Krankheitseinheit selbst.

Im Unterschied zu einer Kaskade (linear, azyklisch) **darf ein PPM Zyklen enthalten**:

- **Negativer Feedback-Regelkreis:** Kombination einer Vorwärtskaskade und einer gegenregulatorischen Kaskade, deren Output den Trigger der Vorwärtskaskade hemmt – modelliert homöostatische Regelkreise (z. B. Barorezeptor-Reflex, RAAS-Rückkopplung)
- **Positiver Feedback-Zyklus:** Kombination zweier gleichgerichteter Kaskaden – modelliert sich selbst verstärkende Zustände und Dekompensation

Ein PPM beschreibt einen Mechanismus so, dass er

- in Texten einheitlich benannt werden kann
- in Fallanalysen wiederverwendbar ist
- als explizite Komposition benannter Kaskaden formal strukturiert ist
- rückkoppelnde Regulationsnetzwerke durch Verkopplung gegenläufiger Kaskaden beschreibt
- in formale Modelle (ODE-Systeme, Regelkreismodelle) übersetzt werden kann

**Ablageort:** Obsidian Vault, Verzeichnis `PPM/`, Dateiname: `PPM – [Name].md`

### 2.6 Krankheitsprozess

Ein **Krankheitsprozess** ist die zeitlich geordnete mechanistische Veränderung eines oder mehrerer Funktionssysteme, durch die pathologische Zustände oder klinisch relevante Störungsbilder entstehen, persistieren oder rezidivieren.

### 2.7 Pathologischer Zustand

Ein **pathologischer Zustand** ist ein Zustand des betrachteten Funktionssystems, in dem Regelgrößen, Kopplungen oder Betriebsregime den physiologischen Funktionsbereich so verlassen haben, dass klinisch relevante Fehlfunktion, Beschwerde oder Schädigung resultiert.

### 2.8 Pathologisches Regime

Ein **pathologisches Regime** ist ein dynamischer Betriebsmodus eines Funktionssystems, der über bloße Einzelabweichungen hinausgeht und ein charakteristisches, krankheitsrelevantes Systemverhalten erzeugt, z. B. anfallsartige Entladung, persistierende Fehlregulation oder rezidivierendes Kippen zwischen Zuständen.

---

## 3. Definition des Krankheitsprozesses

### 3.1 Kerndefinition

Ein **Krankheitsprozess** ist eine zeitlich geordnete, mechanistisch gekoppelte Veränderung eines Funktionssystems oder mehrerer gekoppelter Funktionssysteme, durch die sich

- die Struktur oder Topologie des Systems **(also die Menge der relevanten Prozesseinheiten und ihrer Kopplungen)**
- die Dynamik der Zustandsgrößen
- die wirksamen Parameter
- die Eingänge oder Randbedingungen
- oder die Stabilitäts- und Attraktorstruktur

so verändern, dass **pathologische Zustände**, **klinisch relevante Störungsbilder**, **persistierende Fehlfunktionen** oder **rezidivierende pathologische Regime** entstehen, aufrechterhalten oder verstärkt werden.

### 3.2 Erläuterung der Definition

Diese Definition enthält mehrere notwendige Bestandteile.

#### Zeitlich geordnet

Ein Krankheitsprozess entfaltet sich in der Zeit. Er ist kein statisches Etikett, sondern eine Entwicklung oder ein stabilisiertes *pathologisches Regime*.

#### Mechanistisch gekoppelt

Die einzelnen Bestandteile des Prozesses stehen nicht nur lose nebeneinander, sondern sind kausal, regulatorisch, stofflich, elektrisch, mechanisch oder informationell miteinander verbunden.

#### Systembezogen

Ein Krankheitsprozess bezieht sich immer auf ein bestimmtes Funktionssystem oder auf die Kopplung mehrerer Funktionssysteme. Dadurch bleibt klar, worauf sich die Modellgrenzen und die mechanistische Beschreibung beziehen.

#### Pathologisch relevant

Nicht jede Veränderung eines Systems ist ein Krankheitsprozess. Entscheidend ist, dass die Veränderung zu pathologischen Zuständen, klinisch relevanten Funktionsstörungen oder pathologischen Regimen führt.

#### Modellierungsnah

Die Definition ist so angelegt, dass aus ihr hervorgeht, welche Art von Änderungen an einem mechanistischen Modell vorzunehmen sind. Sie dient also nicht nur der Beschreibung, sondern auch der formalen Übersetzung.

---

## 4. Klassen krankheitsprozesshafter Veränderungen

Die nachfolgenden Klassen sind keine konkurrierenden Diagnosen, sondern **grundlegende Arten**, wie Krankheitsprozesse modelltheoretisch entstehen oder beschrieben werden können. In realen Fällen treten sie häufig kombiniert auf.

### 4.1 Klasse 1: Struktur- oder Topologieänderung

Hier verändert sich die **Struktur des Modells** selbst. Gemeint sind Änderungen darin, welche Prozesseinheiten vorhanden sind und wie sie miteinander gekoppelt sind.

Das kann bedeuten

- Auftreten einer neuen Prozesseinheit
- Verlust einer bisherigen Prozesseinheit
- Hinzukommen neuer Kopplungen
- Wegfall bestehender Kopplungen
- Umlenkung, Fehlkopplung oder Kurzschluss
- Barriereverlust oder neu entstandene Kommunikationswege

Typische Beispiele sind

- bakterielle Invasion mit Vermehrung und Toxinsekretion
- Tumorklon mit eigener Dynamik
- Embolus als neue wirksame Prozesseinheit
- Denervierung oder Leitungsblock
- Shunt, Fistel oder Klappeninsuffizienz
- Membranruptur oder Barrierebruch

#### Modelltheoretische Bedeutung

Die Struktur des Gleichungssystems muss erweitert, reduziert oder umverdrahtet werden.

Typische Folgen sind

- neue oder entfallende Zustandsvariablen
- neue oder entfallende Kopplungsterme oder Flüsse
- neue oder entfallende Parameter
- neu entstehende oder unterbrochene Rückkopplungen

### 4.2 Klasse 2: Parametrische oder adaptive Veränderung

Hier bleibt die Grundstruktur des Systems erhalten, aber **Eigenschaften des Systems verändern sich**. Betroffen sind also nicht primär die Knoten und Verbindungen, sondern deren quantitative oder funktionelle Eigenschaften.

Typische Beispiele sind

- Compliance-Änderung
- Leitfähigkeitsänderung
- Fibrose
- Hypertrophie
- Gefäßremodeling
- Änderung der Rezeptordichte
- Änderung der Enzymaktivität
- Änderung der Reizschwelle
- chronische Entzündungsbereitschaft

#### Modelltheoretische Bedeutung

Ein anfangs als konstant behandelter Parameter ist nicht mehr ausreichend als feste Größe beschreibbar.

Dann bestehen zwei Möglichkeiten

- der Parameter wird als veränderter, aber vorerst quasistatischer Modellparameter gesetzt
- der Parameter wird selbst zu einer langsamen Zustandsgröße mit eigener Dynamik

Damit werden langsame Struktur- oder Empfindlichkeitsänderungen in das Modell integriert.

### 4.3 Klasse 3: Änderung des Betriebsregimes, der Eingänge oder der Randbedingungen

Hier bleibt die Struktur des Systems im Wesentlichen erhalten und es liegt zunächst auch keine primäre strukturelle Umbildung vor. Der Krankheitsprozess entsteht dadurch, dass das System in einen **extremen oder unphysiologisch belastenden Betriebszustand** gerät.

Typische Beispiele sind

- akuter Stress
- Volumenmangel
- Hypoxie
- Fieber
- schwere metabolische Entgleisung
- extreme Belastung
- massive Sympathikusaktivierung
- veränderte hormonelle Steuerung
- geänderte Sollwerte oder Regelanforderungen

#### Modelltheoretische Bedeutung

Das Modell muss nicht primär strukturell verändert werden. Stattdessen werden verändert

- externe Inputs
- Belastungen
- Randbedingungen
- Führungsgrößen oder Sollwerte
- Steuer- und Modulationssignale

Diese Klasse ist wichtig, weil auch ohne erkennbare Strukturveränderung ein klinisch relevantes Störungsbild entstehen kann. Hierbei spielen Konzepte wie Allostase und allostatische Last eine Rolle.

### 4.4 Klasse 4: Attraktor-, Regime- oder Stabilitätswechsel

Hier ist entscheidend, dass das System aufgrund seiner Dynamik **mehrere mögliche stabile oder quasi-stabile Zustände** besitzen kann oder in einen pathologischen Oszillationsmodus übergeht. Diese Klasse beschreibt also vor allem die qualitative Form des Systemverhaltens.

Typische Beispiele sind

- epileptische Anfälle
- Herzrhythmusstörungen
- periodische Paralysen
- paroxysmale Funktionsstörungen
- hysteretische Umschläge zwischen zwei Regimen
- pathologische Grenzzyklen

#### Modelltheoretische Bedeutung

Diese Klasse beschreibt nicht primär eine neue Ursache, sondern die **Stabilitäts- und Attraktorstruktur des Zustandsraums** und die Art des Systemverhaltens.

Zu analysieren sind insbesondere

- stabile und instabile Zustände
- Kippunkte
- Bifurkationen
- Basins of attraction
- hysteretische Übergänge
- Trigger und Perturbationen

#### Wichtiger Hinweis zur Einordnung

Die Klassen 1 bis 3 beschreiben vor allem **Arten von Modelländerungen oder Störungsquellen**.

Klasse 4 beschreibt dagegen vor allem eine **Eigenschaft der Systemdynamik**.

In realen Krankheitsprozessen gilt häufig folgende Logik:

- Änderungen der Struktur, der Parameter oder der Inputs verschieben das System
- dadurch verändern sich die Stabilitätsverhältnisse
- anschließend kann ein pathologischer Attraktor oder ein pathologisches Oszillationsregime erreicht werden

Klasse 4 ist daher als **Dynamikebene** stets mitzudenken.

Zu beachten ist auch, dass Klasse-4-Beschreibungen diagnostisch schwer erfassbar sein können, wenn sich das System gerade nicht in einem pathologischen Attraktor befindet oder wenn gesunde und pathologische Zustandsräume teilweise überlappen. Diagnostisch wegweisend wird dann häufig die Beschreibung des Parameterraums oder des aktuellen pathophysiologischen Regimes.

---

## 5. Minimalstruktur einer Krankheitsprozessbeschreibung

Eine brauchbare Krankheitsprozessbeschreibung soll mindestens die folgenden Fragen beantworten.

### 5.1 Referenzsystem

- Welches Funktionssystem ist primär betroffen?
- Welche gekoppelten Nebensysteme sind relevant?

### 5.2 Ausgangszustand

- Was ist der funktionelle Referenzzustand?
- Welche Größen gelten im Ausgangszustand als reguliert oder stabil?

### 5.3 Auslöser oder Eintrittsbedingung

- Wodurch beginnt der Prozess?
- Handelt es sich um ein externes Ereignis, eine interne Dysregulation oder einen Zustandsübergang?

### 5.4 Primäre Veränderung

- Welche der Klassen 1 bis 4 liegt vor?
- Welche Systemkomponente verändert sich zuerst?

### 5.5 Mechanistische Folgeglieder

- Welche Veränderungen folgen daraus?
- Welche Beziehungen sind kausal und welche nur korrelativ?
- Welche Rückkopplungen verstärken oder dämpfen den Prozess?

### 5.6 Klinische oder funktionelle Outputs

- Welche Symptome, Zeichen oder Messgrößen resultieren?
- Welche Outputs sind diagnostisch besonders aussagekräftig?

### 5.7 Zeitstruktur

- Welche Anteile sind schnell?
- Welche Anteile sind langsam?
- Gibt es diskrete Ereignisse, Schwellen oder Verzögerungen?

### 5.8 Reversibilität und Persistenz

- Ist der Prozess reversibel?
- Welche Faktoren erhalten ihn aufrecht?
- Gibt es irreversible Strukturfolgen?

---

## 6. Krankheitsprozess und mathematische Modellierung

### 6.1 Grundidee

Ein Krankheitsprozess soll so beschrieben werden, dass er als Veränderung eines physiologischen Referenzmodells formuliert werden kann.

Ein einfaches physiologisches Grundmodell kann schematisch beschrieben werden als

```text
x'(t) = f(x, u, p, t)
y(t)  = h(x, u, p, t)
```

mit

- `x` = Zustandsvariablen
- `u` = Eingänge, Belastungen, Führungsgrößen oder externe Einflüsse
- `p` = Parameter
- `y` = beobachtbare Outputs

Ein Krankheitsprozess kann dieses Grundmodell auf verschiedene Weise verändern.

### 6.2 Vier Grundoperationen krankheitsprozesshafter Modelländerung

#### A. Strukturänderung

```text
x'(t) = f(x, z, u, p, t)
z'(t) = g(x, z, u, p, q, t)
```

Es treten zusätzliche Zustandsvariablen `z` oder neue Kopplungen auf.

#### B. Parameterdynamisierung

```text
x'(t) = f(x, u, p(t), t)
p'(t) = r(x, u, p, t)
```

Bisher feste Parameter werden zu langsam veränderlichen Größen.

#### C. Änderung von Inputs oder Randbedingungen

```text
x'(t) = f(x, u_path(t), p, t)
```

Der Krankheitsprozess wirkt primär über pathologisch veränderte Inputs, Belastungen oder Steuergrößen.

#### D. Regime- und Attraktorwechsel

Hier bleibt die Form des Modells unter Umständen gleich, aber die qualitative Dynamik ändert sich.

Zu prüfen sind

- Existenz mehrerer Attraktoren
- Schwellen für Regimewechsel
- Oszillationen
- Bifurkationen
- Hysterese

### 6.3 Erweiterte Modellformen

Nicht jeder Krankheitsprozess ist mit einem glatten ODE-System vollständig beschrieben. Für viele Prozesse reichen ODE-basierte oder lumped-parameter-Modelle aus, während in anderen Fällen zusätzliche Modellklassen erforderlich sind.

Zusätzliche Modellbausteine können erforderlich sein bei

- diskreten Ereignissen
- Schaltvorgängen
- stochastischen Triggern
- Verzögerungen
- räumlicher Ausbreitung
- Populationsdynamik
- Agenteninteraktionen

Dann können etwa benötigt werden

- hybride Modelle
- Delay-Differentialgleichungen
- PDE-Modelle
- stochastische Modelle
- agentenbasierte Modelle

Die ODE-nahe Sprache bleibt jedoch als Grundgerüst nützlich, weil sie zur expliziten Benennung von Zustandsgrößen, Parametern, Inputs und Outputs zwingt.

---

## 7. Modellierungsvorschrift aus einer Krankheitsprozessbeschreibung

Aus einer textlichen Beschreibung eines Krankheitsprozesses soll möglichst systematisch eine Modellierungsvorschrift abgeleitet werden können.

### 7.1 Schritt 1: Systemgrenzen festlegen

- Welches Funktionssystem wird modelliert?
- Welche Umweltgrößen werden nur als Input behandelt?
- Welche benachbarten Systeme werden explizit mitmodelliert?

### 7.2 Schritt 2: Zustandsgrößen identifizieren

Zu fragen ist

- Welche Größen speichern den aktuellen Systemzustand?
- Welche Größen verändern sich dynamisch?
- Welche Größen sind für die klinische Störung entscheidend?

Beispiele sind

- Konzentrationen
- Volumina
- Drucke
- Spannungen
- Öffnungszustände
- Erregbarkeiten
- Zellzahlen
- Reservoirgrößen

### 7.3 Schritt 3: Parameter identifizieren

Zu fragen ist

- Welche Eigenschaften bestimmen das Verhalten, ohne im Grundmodell Zustandsgrößen zu sein?
- Welche dieser Eigenschaften ändern sich im Krankheitsprozess?

Beispiele sind

- Compliance
- Leitfähigkeit
- maximale Enzymaktivität
- Rezeptordichte
- Gewebesteifigkeit
- Schwellwerte
- Diffusionskoeffizienten

### 7.4 Schritt 4: Inputs und Randbedingungen identifizieren

Zu fragen ist

- Welche Belastungen treffen auf das System?
- Welche Steuergrößen kommen von außen?
- Welche Randbedingungen definieren die Betriebsweise?

### 7.5 Schritt 5: Kausalkette formulieren

Für jede relevante Aussage soll geprüft werden

- Welche Größe verändert welche andere Größe?
- In welcher Richtung?
- Über welchen Mechanismus?
- Mit welcher Zeitcharakteristik?

### 7.6 Schritt 6: Rückkopplungen markieren

Es soll ausdrücklich benannt werden

- welche Schleifen negativ rückkoppeln
- welche Schleifen positiv rückkoppeln
- welche Schleifen kompensatorisch sind
- welche Schleifen zur Dekompensation beitragen

### 7.7 Schritt 7: Ereignisse, Schwellen und Regimewechsel markieren

Zu prüfen ist

- Gibt es Schwellenüberschreitungen?
- Gibt es Zustandswechsel?
- Gibt es irreversible Kipppunkte?
- Gibt es hysteretische Umschläge?

### 7.8 Schritt 8: Beobachtbare Outputs definieren

Jede Modellierung soll explizit machen, welche Variablen klinisch oder diagnostisch beobachtbar sind.

Dazu gehören

- Symptome
- Vitalparameter
- Laborwerte
- Funktionsmessungen
- Bildgebungsmerkmale
- Belastungsreaktionen

### 7.9 Schritt 9: Zeitmaßstäbe trennen

Es soll unterschieden werden zwischen

- schnellen Zustandsänderungen
- mittleren Adaptationsprozessen
- langsamen Strukturprozessen

Diese Trennung ist zentral, weil viele Krankheitsprozesse nur dann sinnvoll modelliert werden können, wenn schnelle und langsame Dynamiken getrennt dargestellt werden.

---

## 8. Formale Darstellungslogik für PPM

Ein PPM soll nach Möglichkeit in einem einheitlichen Schema beschrieben werden. Das erhöht Vergleichbarkeit, Wiederverwendbarkeit und formale Anschlussfähigkeit.

### 8.1 Empfohlenes PPM-Schema

#### PPM-Name

Kurzer, mechanistisch sprechender Name des Moduls.

#### Referenzsystem

Welches Funktionssystem ist das primäre Bezugssystem?

#### Auslöser

Was startet das Modul?

#### Primäre Veränderung

Welche der Klassen 1 bis 4 liegt primär vor?

#### Relevante Zustandsgrößen

Welche dynamischen Größen sind zentral?

#### Relevante Parameter

Welche Systemeigenschaften bestimmen das Verhalten?

#### Inputs und Belastungen

Welche externen oder übergeordneten Einflüsse wirken auf das Modul?

#### Kaskadenkomponenten

Aus welchen benannten Kaskaden ist das PPM zusammengesetzt? (Wikilinks auf `Kaskaden/Kaskade – [Name].md`)

#### Zyklische Kopplung

Welche Kaskaden bilden Zyklen (neg. Feedback, pos. Feedback)? Wie sind sie verschaltet?

#### Mechanistische Kette

Welche gerichteten Beziehungen verbinden Auslöser, Zwischenzustände und Outputs (Gesamtblockdiagramm über alle Kaskaden hinweg)?

#### Rückkopplungen

Welche Schleifen stabilisieren, destabilisieren oder verstärken den Prozess (entstehen durch Kaskadenverkopplung)?

#### Schwellen oder Regimewechsel

Gibt es Kipppunkte, Trigger, Hysterese oder Multistabilität?

#### Klinische Outputs

Welche Symptome, Zeichen oder Messgrößen resultieren?

#### Reversibilität

Unter welchen Bedingungen ist das Modul reversibel oder persistiert es?

#### Modellhinweis

Welche Modellform ist mindestens erforderlich?

Beispiele sind

- ODE ausreichend
- ODE plus langsame Parameterdynamik
- hybrides Modell
- stochastisch getriggertes Regimewechselmodell

---

## 9. Abgrenzungen

### 9.1 Krankheitsprozess ist nicht gleich Krankheitseinheit

Eine Krankheitseinheit ist eine klinisch oder nosologisch benannte Entität.

Ein Krankheitsprozess ist dagegen der mechanistische Ablauf oder das pathologische Regime, das diese Entität erklärt oder mitträgt.

Eine Krankheitseinheit kann mehrere Krankheitsprozesse umfassen.

Ein Krankheitsprozess kann umgekehrt bei mehreren Krankheitseinheiten vorkommen.

### 9.2 Krankheitsprozess ist nicht gleich Symptom

Ein Symptom ist ein beobachtbarer oder berichteter Output.

Ein Krankheitsprozess ist die mechanistische Dynamik, die zu diesem Output führt.

### 9.3 Krankheitsprozess ist nicht gleich Risikofaktor

Ein Risikofaktor erhöht die Wahrscheinlichkeit, dass ein Krankheitsprozess auftritt oder fortschreitet.

Er ist nicht notwendig selbst schon der Krankheitsprozess.

### 9.4 Krankheitsprozess ist nicht gleich bloßer Befund

Ein Befund kann Ausdruck eines Krankheitsprozesses sein, ohne dessen Mechanismus vollständig zu beschreiben.

---

## 10. Heuristische Leitregeln für konsistente Beschreibungen

Damit Krankheitsprozessbeschreibungen zwischen Projekten konsistent bleiben, sollen die folgenden Regeln eingehalten werden.

### 10.1 Mechanistisch statt etikettenhaft formulieren

Nicht nur nennen, dass „Krankheit X vorliegt“, sondern angeben, **welche Veränderung im System** den Prozess ausmacht.

### 10.2 Richtung und Vermittlung angeben

Nicht nur sagen, dass zwei Größen zusammenhängen, sondern angeben

- in welcher Richtung die Beziehung wirkt
- über welchen Mechanismus sie vermittelt ist

### 10.3 Ursache, Verstärker und Folge trennen

Es soll unterschieden werden zwischen

- Auslösern
- aufrechterhaltenden Faktoren
- Verstärkern
- Folgephänomenen

### 10.4 Struktur, Parameter, Input und Dynamik nicht vermischen

Es soll ausdrücklich benannt werden, ob eine Aussage sich bezieht auf

- die Modellstruktur
- einen Parameter
- eine Zustandsvariable
- einen externen Input
- die Stabilitätslandschaft des Systems

### 10.5 Zeitlichkeit explizit machen

Zu jeder relevanten Veränderung soll nach Möglichkeit gesagt werden, ob sie

- akut
- subakut
- chronisch
- episodisch
- rezidivierend
- persistent

ist.

### 10.6 Beobachtbarkeit separat benennen

Es ist gesondert zu markieren, welche Größen

- mechanistisch zentral
- klinisch beobachtbar
- diagnostisch messbar

sind.

### 10.7 Terminologische Sparsamkeit wahren

Synonyme sollen nur verwendet werden, wenn sie einen echten Zusatznutzen haben. Für dieselbe Sache soll im selben Text möglichst nur ein Kernbegriff benutzt werden.

---

## 11. Kompakte Arbeitsdefinition für Skills und Agenten

Für knappe technische Kontexte kann folgende Kurzform verwendet werden.

> Ein Krankheitsprozess ist eine zeitlich geordnete mechanistische Veränderung eines Funktionssystems, bei der sich Struktur oder Topologie des Systems, Parameter, Eingänge, Zustandsdynamik oder Stabilitätsstruktur so verändern, dass klinisch relevante pathologische Zustände oder Störungsbilder entstehen, persistieren oder wiederkehren.

---

## 12. Kompakte Modellierungsdefinition für PPM

> Ein PPM beschreibt einen abgegrenzten Regulationszusammenhang als Komposition benannter Kaskaden so, dass Auslöser, Systemgrenzen, Zustandsgrößen, Parameter, Inputs, mechanistische Kopplungen (linear in Kaskaden, zyklisch im PPM), Rückkopplungen, Schwellen, Zeitmaßstäbe und klinische Outputs explizit benannt und formal modellierbar werden. Kaskaden beschreiben die linearen Teilketten; PPMs fügen sie zu zyklischen Regelkreisen oder komplexen Modulen zusammen.

---

## 13. Kurzbeispiele zur Orientierung

### Beispiel A: Bakterielle Invasion mit Toxinbildung

Primär liegt eine **Strukturänderung** vor.

- neue Prozesseinheit: Bakterienpopulation
- neue Zustandsgrößen: Keimzahl, Toxinkonzentration
- neue Kopplungen: Toxinwirkung auf Wirtsgewebe
- mögliche Folgedynamik: Entzündung, Gewebeschaden, Kreislaufreaktion

### Beispiel B: Chronische Druckbelastung mit Remodeling

Primär liegt eine **parametrische oder adaptive Veränderung** vor.

- steigende Wanddicke
- veränderte Compliance
- veränderte Relaxationseigenschaften
- langsame Umwandlung eines Parameters in eine Zustandsgröße

### Beispiel C: Akuter extremer Stresszustand

Primär liegt eine **Änderung des Betriebsregimes** vor.

- massive Änderung neurohumoraler Inputs
- veränderte Sollwertlage und Sympathikusaktivierung
- funktionelle Fehlleistung auch ohne initiale Strukturänderung

### Beispiel D: Epileptischer Anfall

Im Vordergrund steht ein **Regime- oder Attraktorwechsel**.

- das System verlässt einen normalen Aktivitätszustand
- ein pathologisches, sich selbst tragendes Erregungsmuster entsteht
- Trigger, Schwellen und Stabilitätsverhältnisse werden zentral

---

## 14. Schlussformel

Der Krankheitsprozessbegriff dient in SOFL und PiCA als **gemeinsamer mechanistischer Referenzbegriff**. Er verbindet

- klinische Störungsbilder
- physiologische und pathophysiologische Kaskaden (lineare Teilketten, DAG-Äste)
- PPMs als modulare Kompositionen von Kaskaden (zyklische Regelkreise möglich)
- formale Modellierung

in einer einheitlichen Sprache. Die Hierarchie lautet: **Krankheitsprozess → PPM-Netzwerk → PPM → Kaskaden**. Kaskaden sind die atomaren Bausteine; PPMs verkoppeln sie zu Regelkreisen; PPM-Netzwerke beschreiben das fault-Slot eines Illness-Scripts.

Sein Kern besteht darin, Krankheit nicht primär als Namen, sondern als **dynamische Fehlorganisation von Funktionssystemen** zu beschreiben.
