# User Stories – FleetConnect

| | |
|---|---|
| **Projekt** | FleetConnect – Dispositionssystem für kleine Speditionen |
| **Dokument** | User Stories mit Akzeptanzkriterien und Rückverfolgbarkeit |
| **Stand** | 15.09.2026 |
| **Grundlage** | [[Anforderungen]], [[Stakeholder-und-Personas]], Use-Case-Diagramm [[use-case.puml]] |

Schema: *Als [Rolle] möchte ich [Funktion], damit [Nutzen].*
Jede Story lässt sich auf ihre funktionale Anforderung (FA) und ihren Use Case (UC) zurückführen. Die Akzeptanzkriterien stammen überwiegend aus den nicht-funktionalen Anforderungen und sind deshalb messbar. Priorität und Größe entsprechen den Feldern im Kanban-Board.

## Übersicht

| ID | Titel | Quelle | Prio | Size |
|---|---|---|---|---|
| US-01 | Benutzer verwalten und anmelden | FA-01 + UC12 | P0 | L |
| US-02 | Tour planen, zuweisen und in der Fahrer-App anzeigen | FA-02 + FA-03 | P0 | L |
| US-03 | Status melden und Position übermitteln | FA-04 + FA-05 | P0 | L |
| US-04 | Aktive Fahrer auf der Live-Karte verfolgen | FA-06 | P0 | L |
| US-05 | Chat mit automatischer Übersetzung | FA-07 + FA-14 | P0 | L |
| US-06 | KI-Co-Disponent Winston mit Freigabeprinzip | FA-15 | P1 | XL |

---

## US-01 – Benutzer verwalten und anmelden

**User Story**
Als **Inhaberin und Admin** möchte ich **Mitarbeitende mit ihrer Rolle anlegen und wieder deaktivieren**, damit **jeder nur die Funktionen sieht, die er braucht, und ehemalige Mitarbeitende keinen Zugriff mehr haben**.

**Akzeptanzkriterien**
- [ ] Der Admin legt einen Benutzer mit Name, E-Mail, Rolle (Fahrer, Disponent, Admin) und Sprache (DE, EN, PL) an.
- [ ] Benutzer melden sich mit E-Mail und Passwort an und landen in der Ansicht ihrer Rolle: Fahrer-App oder Leitstand.
- [ ] Ein Fahrer kann keine Funktionen des Leitstands aufrufen (siehe Rechte-Matrix).
- [ ] Ein deaktivierter Benutzer kann sich nicht mehr anmelden.
- [ ] Passwörter werden ausschließlich gehasht gespeichert (NFA-07).

Quelle: FA-01, UC01, UC12 · NFA-07 · Persona Andrea Bachmann · P0 · L

---

## US-02 – Tour planen, zuweisen und in der Fahrer-App anzeigen

**User Story**
Als **Disponent** möchte ich **eine Tour mit mehreren Stopps anlegen und einem Fahrer zuweisen**, damit **der Fahrer seinen Auftrag vollständig in der App hat und ich ihn nicht am Telefon durchgeben muss**.

**Akzeptanzkriterien**
- [ ] Der Disponent legt eine Tour mit Datum, Fahrzeug und mindestens einem Stopp (Adresse, Zeitfenster) an. Die Reihenfolge der Stopps lässt sich ändern.
- [ ] Die Tour kann genau einem Fahrer zugewiesen werden. Ihr Status wechselt von „geplant“ zu „zugewiesen“.
- [ ] Die zugewiesene Tour erscheint in **unter 3 Sekunden** in der Fahrer-App (NFA-01).
- [ ] Der Fahrer sieht die Stopps in Reihenfolge mit Adresse und Zeitfenster, die Oberfläche in seiner Sprache (NFA-05).
- [ ] Ändert der Disponent eine zugewiesene Tour, erhält der Fahrer einen Hinweis in der App.
- [ ] Ein neuer Disponent legt seine erste Tour **ohne Schulung** in unter 10 Minuten an (NFA-06).

Quelle: FA-02, FA-03, UC02, UC03, UC04 · NFA-01, NFA-05, NFA-06 · Personas Markus Reinhardt, Tomasz Nowak · P0 · L

---

## US-03 – Status melden und Position übermitteln

**User Story**
Als **Fahrer** möchte ich **meinen Status mit einem Tipp melden**, damit **ich während der Tour nicht telefonieren muss und der Disponent trotzdem Bescheid weiß**.

**Akzeptanzkriterien**
- [ ] Für Abfahrt, Angekommen, Entladen, Pause, Problem und Tour beendet gibt es je eine Schaltfläche. Eine Meldung braucht **einen Tipp** (NFA-04).
- [ ] Die Meldung erscheint in **unter 3 Sekunden** im Leitstand (NFA-01).
- [ ] Die Positionsübermittlung startet mit „Abfahrt“ und läuft nur während der aktiven Tour (FA-05).
- [ ] **Bei Pause keine Positionsübermittlung.** Die App zeigt deutlich „Ortung aus“ (NFA-02).
- [ ] Nach „Tour beendet“ werden keine Positionen mehr übermittelt.
- [ ] Jede Meldung wird mit Zeitstempel zur Tour gespeichert.

Quelle: FA-04, FA-05, UC05, UC06 · NFA-01, NFA-02, NFA-04 · Persona Tomasz Nowak · P0 · L

---

## US-04 – Aktive Fahrer auf der Live-Karte verfolgen

**User Story**
Als **Disponent** möchte ich **alle Fahrer mit aktiver Tour auf einer Karte sehen**, damit **ich Kundenanfragen sofort beantworten kann, ohne den Fahrer anzurufen**.

**Akzeptanzkriterien**
- [ ] Die Karte zeigt nur Fahrer mit aktiver oder pausierter Tour.
- [ ] Jeder Marker zeigt Name des Fahrers, letzten Status und Uhrzeit der letzten Position.
- [ ] Positionen aktualisieren sich ohne Neuladen der Seite, spätestens alle 30 Sekunden.
- [ ] Bei Pause erscheint keine neue Position. Der Marker zeigt „Pause – Ortung aus“ (NFA-02).
- [ ] Ein Klick auf den Marker öffnet die Tour mit ihren Stopps und dem Chat.

Quelle: FA-06, UC07 · NFA-01, NFA-02 · Persona Markus Reinhardt · P0 · L

---

## US-05 – Chat mit automatischer Übersetzung

**User Story**
Als **Fahrer mit polnischer Muttersprache** möchte ich **Nachrichten des Disponenten auf Polnisch lesen und auf Polnisch antworten**, damit **Anweisungen ohne Missverständnisse ankommen**.

**Akzeptanzkriterien**
- [ ] Der Chat ist der Tour zugeordnet. Disponent und Fahrer sehen denselben Verlauf.
- [ ] Nachrichten werden automatisch in die eingestellte Sprache des Empfängers übersetzt: DE, EN oder PL (FA-14).
- [ ] **Das Original bleibt abrufbar**, mit einem Tipp auf „Original anzeigen“.
- [ ] Eine übersetzte Nachricht erscheint in **unter 5 Sekunden** (NFA-05).
- [ ] Ist die Übersetzung nicht verfügbar, erscheint das Original mit einem Hinweis.
- [ ] Die Oberfläche der Fahrer-App lässt sich auf DE, EN oder PL umstellen.

Quelle: FA-07, FA-14, UC08, UC09 · NFA-05 · Personas Tomasz Nowak, Markus Reinhardt · P0 · L

---

## US-06 – KI-Co-Disponent Winston mit Freigabeprinzip

**User Story**
Als **Disponent** möchte ich, dass **Winston Verspätungen erkennt und mir passende Nachrichten vorschlägt**, damit **ich Kunden und Fahrer schneller informiere und trotzdem jede Nachricht selbst freigebe**.

**Akzeptanzkriterien**
- [ ] Winston meldet eine Verspätung, sobald die ETA eines Stopps dessen Zeitfenster um mehr als 15 Minuten überschreitet (setzt FA-11 voraus).
- [ ] Winston erstellt einen Nachrichtenentwurf mit Tour, Stopp und neuer voraussichtlicher Ankunftszeit.
- [ ] Der Entwurf erscheint im Leitstand mit den Aktionen „Freigeben“, „Bearbeiten“ und „Verwerfen“.
- [ ] **Ohne Freigabe wird nichts gesendet** (NFA-03).
- [ ] Freigaben und Ablehnungen werden mit Benutzer und Zeitpunkt protokolliert.
- [ ] Freigegebene Nachrichten an den Fahrer werden automatisch in seine Sprache übersetzt (FA-14).

Quelle: FA-15, UC11, UC13, UC14 · NFA-03 · Persona Markus Reinhardt · P1 · XL

> [!warning] INVEST
> Mit Größe XL ist US-06 nicht „Small“, also nicht klein genug für einen Sprint. Natürliche Teile wären **Erkennung**, **Entwurf** und **Freigabe-Oberfläche**. Laut Scrumban-Leitfaden wird ohnehin erst im Sprint Planning zerlegt. Die Entscheidung ist noch offen.

---

## Rückverfolgbarkeit

| Story | Funktionale Anforderung | Use Cases | Nicht-funktionale Anforderung | Persona |
|---|---|---|---|---|
| US-01 | FA-01 | UC01, UC12 | NFA-07 | Andrea Bachmann |
| US-02 | FA-02, FA-03 | UC02, UC03, UC04 | NFA-01, NFA-05, NFA-06 | Markus Reinhardt, Tomasz Nowak |
| US-03 | FA-04, FA-05 | UC05, UC06 | NFA-01, NFA-02, NFA-04 | Tomasz Nowak |
| US-04 | FA-06 | UC07 | NFA-01, NFA-02 | Markus Reinhardt |
| US-05 | FA-07, FA-14 | UC08, UC09 | NFA-05 | Tomasz Nowak, Markus Reinhardt |
| US-06 | FA-15 | UC11, UC13, UC14 | NFA-03 | Markus Reinhardt |

**Nicht als Story ausgearbeitet**, aber als Anforderung dokumentiert: FA-08 Foto-Upload · FA-09 Unterschrift · FA-10 Dashboard · FA-11 ETA · FA-12 Auswertungen · FA-13 Offline-Modus. UC10 (Ablieferung dokumentieren) gehört zu FA-08 und FA-09.

## Aufwand und Planung

- Aufwand grob: fünfmal L, einmal XL.
- Bei drei Personen und 2–5 Wochen je Sprint schaffen wir etwa zwei Stories pro Sprint, also rund **drei Sprints für den MVP**.
- Wird die Zeit knapp, ist **US-06 der erste Kandidat fürs Backlog**.

## Kartenformat im Kanban-Board

Jede Karte ist kompakt und trägt ihre FA-Nummer im Body:

```text
Titel:  US-03 – Status melden und Position übermitteln

Als Fahrer möchte ich meinen Status mit einem Tipp melden, damit ich während
der Tour nicht telefonieren muss und der Disponent trotzdem Bescheid weiß.

Akzeptanzkriterien
- [ ] Je eine Schaltfläche pro Status, ein Tipp
- [ ] Meldung erscheint in unter 3 Sekunden im Leitstand
- [ ] Bei Pause keine Positionsübermittlung

Quelle: FA-04, FA-05
```
