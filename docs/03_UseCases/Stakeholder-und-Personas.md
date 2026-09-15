# Stakeholder und Personas – FleetConnect

| | |
|---|---|
| **Projekt** | FleetConnect – Dispositionssystem für kleine Speditionen |
| **Dokument** | Stakeholdermatrix, Zielgruppencluster, Personas, Rechte-Matrix |
| **Stand** | 15.09.2026 |
| **Methodik** | Stakeholdermatrix → Zielgruppencluster → Personas → User Stories |

## 1. Stakeholdermatrix

Achsen: **Einfluss** der Stakeholder auf das Projekt × **Bedeutung** des Produkts für sie. Nummerierung wie in [[Anforderungen]].

| | **geringer Einfluss** | **hoher Einfluss** |
|---|---|---|
| **hohe Bedeutung** | **S3 Fahrer/in**<br>→ Bedürfnisse aktiv erheben | **S1 Inhaber/in**, **S2 Disponent/in**<br>→ eng einbinden |
| **geringe Bedeutung** | **S4 Fuhrparkmanager/in**<br>→ informieren | **S5 Kunde der Spedition**<br>→ zufriedenstellen |

**Einordnung**

- **Disponent und Inhaberin** stehen oben rechts. Sie nutzen das System täglich beziehungsweise entscheiden über die Anschaffung und werden deshalb eng eingebunden.
- **Der Fahrer** steht oben links: hohe Bedeutung, wenig Einfluss. Seine Bedürfnisse müssen wir aktiv erheben, weil er sie nicht von selbst durchsetzt.
- **Der Kunde** nutzt das System nicht, erwartet aber pünktliche Lieferungen und frühe Information. Das beeinflusst die Anforderungen (ETA, Winston).
- **Der Fuhrparkmanager** hat im aktuellen Funktionsumfang keine Aufgabe. Ob er als Stakeholder bleibt, ist noch offen.

## 2. Zielgruppencluster

| Gruppe/Rolle | Beschreibung im System | Bedürfnisse/Ziele | Probleme/Barrieren | Typische Nutzung |
|---|---|---|---|---|
| **Disponent/in** | plant, verteilt und überwacht Touren im Leitstand | aktueller Überblick ohne Telefonate, Kunden schnell informieren | Fahrern hinterhertelefonieren, Informationen verteilt auf Telefon, Messenger und Excel | ganztägig am PC, mehrere Touren parallel |
| **Fahrer/in** | erhält Touren und meldet Status in der Fahrer-App | vollständiger Auftrag vor Abfahrt, wenig Ablenkung, Verständigung in eigener Sprache | Sprachbarriere, Anrufe während der Fahrt, Sorge vor Dauerüberwachung | Smartphone, kurze Aktionen an Stopps und in Pausen |
| **Inhaber/in (Admin)** | verwaltet Benutzer und entscheidet über die Einführung | geringe Kosten, zufriedene Kunden, wenig Einführungsaufwand | keine IT-Kenntnisse, Angst vor langen Verträgen und Schulungsaufwand | gelegentlich am PC: Benutzer anlegen, Überblick verschaffen |

## 3. Personas

Die drei Personas arbeiten im selben fiktiven Betrieb: **Bachmann Transporte**, eine Spedition mit 12 Lkw bei Nürnberg.

### 3.1 Markus Reinhardt, 47 – Disponent

| | |
|---|---|
| **Grunddaten** | 47 Jahre, Kaufmann für Spedition und Logistikdienstleistung, seit 15 Jahren Disponent bei Bachmann Transporte, einziger Vollzeit-Disponent |
| **Verhaltensweisen** | arbeitet mit zwei Bildschirmen, Excel-Tourenplan und Telefon am Ohr; hält eine WhatsApp-Gruppe mit den Fahrern; notiert Rückrufe auf Zetteln |
| **Motivation** | Die Touren sollen laufen und die Kunden zufrieden sein. Er ist stolz darauf, immer den Überblick zu behalten. |
| **Ziele** | weniger Telefonate, Kundenanfragen wie „Wo ist meine Ware?“ sofort beantworten, Verspätungen früh erkennen |
| **Frustrationen/Pain Points** | ständiges Hinterhertelefonieren; Fahrer gehen während der Fahrt nicht ran; Missverständnisse mit Fahrern, die wenig Deutsch sprechen; Kunden erfahren zu spät von Verspätungen |
| **Zitat** | „Die Hälfte des Tages telefoniere ich Fahrern hinterher, nur um zu erfahren, wo sie gerade sind.“ |

**Hauptnutzer des Leitstands.** Leitet sich ab zu US-02, US-04, US-05 und US-06.

### 3.2 Tomasz Nowak, 38 – Fahrer

| | |
|---|---|
| **Grunddaten** | 38 Jahre, Muttersprache Polnisch, seit sechs Jahren Berufskraftfahrer in Deutschland; fährt Regionaltouren mit vier bis acht Stopps am Tag; Deutsch: Grundkenntnisse |
| **Verhaltensweisen** | nutzt privat ein Android-Smartphone, WhatsApp und eine Übersetzungs-App; telefoniert ungern während der Fahrt; fragt bei Unklarheiten selten nach |
| **Motivation** | zuverlässig arbeiten, pünktlich Feierabend machen, keinen Ärger wegen Missverständnissen bekommen |
| **Ziele** | Auftrag vollständig und verständlich vor der Abfahrt; Status melden, ohne anzurufen; in der Pause nicht geortet werden |
| **Frustrationen/Pain Points** | schnelle Anweisungen auf Deutsch am Telefon, von denen er nicht alles versteht; Anrufe während der Fahrt; das Gefühl, ständig überwacht zu werden |
| **Zitat** | „Wenn ich es auf Polnisch lese, verstehe ich es beim ersten Mal.“ |

**Begründet den Mehrsprachigkeits-USP.** Leitet sich ab zu US-03 und US-05.

### 3.3 Andrea Bachmann, 52 – Inhaberin und Admin

| | |
|---|---|
| **Grunddaten** | 52 Jahre, führt Bachmann Transporte in zweiter Generation, 12 Lkw und 15 Mitarbeitende, kaufmännische Ausbildung |
| **Verhaltensweisen** | entscheidet nach Kosten und Aufwand; nutzt E-Mail und Online-Banking, sonst wenig IT; lässt sich bei Software von Markus beraten |
| **Motivation** | den Betrieb zukunftsfähig halten, Fahrer und Disposition entlasten, Stammkunden halten |
| **Ziele** | eine Lösung ohne Einbau, ohne Schulung und monatlich kündbar; Datenschutz sicher einhalten |
| **Frustrationen/Pain Points** | keine IT-Kenntnisse; schlechte Erfahrungen mit Software, die lange Verträge und teure Einrichtung verlangt; Unsicherheit beim Datenschutz rund um die Ortung |
| **Zitat** | „Wenn wir dafür erst einen Techniker und eine Schulung brauchen, lassen wir es.“ |

**Entscheidet über die Anschaffung.** Leitet sich ab zu US-01.

## 4. Rechte-Matrix

✓ = erlaubt · – = nicht erlaubt

| Funktion | Fahrer | Disponent | Admin | Winston |
|---|:---:|:---:|:---:|:---:|
| Anmelden | ✓ | ✓ | ✓ | – |
| Benutzer anlegen, Rollen vergeben, deaktivieren | – | – | ✓ | – |
| Tour anlegen und bearbeiten | – | ✓ | – | – |
| Tour einem Fahrer zuweisen | – | ✓ | – | – |
| eigene Tour ansehen | ✓ | – | – | – |
| alle Touren ansehen | – | ✓ | ✓ | ✓ (lesend) |
| Status melden | ✓ | – | – | – |
| Position übermitteln (nur während aktiver Tour) | ✓ | – | – | – |
| Live-Karte ansehen | – | ✓ | ✓ | – |
| Chat mit Fahrer bzw. Disponent | ✓ | ✓ | – | – |
| Verspätung erkennen, Nachricht entwerfen | – | – | – | ✓ |
| Vorschlag freigeben, bearbeiten oder verwerfen | – | ✓ | – | – |
| Nachricht versenden | ✓ | ✓ | – | – (nur nach Freigabe durch den Disponenten) |
| Auswertungen ansehen (FA-12) | – | ✓ | ✓ | – |
