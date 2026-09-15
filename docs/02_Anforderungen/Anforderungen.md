# Anforderungen – FleetConnect

| | |
|---|---|
| **Projekt** | FleetConnect – Dispositionssystem für kleine Speditionen |
| **Dokument** | Anforderungsdokument |
| **Version** | 0.1 |
| **Stand** | 15.09.2026 |
| **Vorgehen** | Requirements Engineering, Umsetzung nach Scrumban |

## 1. Zweck und Ziel

FleetConnect unterstützt kleine Speditionen (2–20 Lkw, 1–3 Disponenten) bei der täglichen Disposition. Im Mittelpunkt steht der Arbeitsablauf, nicht die Ortung:

> Disponent plant Tour mit Stopps → weist Fahrer zu → Fahrer meldet Status mit einem Tipp → GPS läuft nur während der Tour → Disponent sieht Live-Karte → Chat mit Auto-Übersetzung → Winston schlägt bei Verspätung Nachrichten vor, der Mensch gibt frei.

Markt und Alleinstellungsmerkmale: [[Marktanalyse]], [[USP]].

## 2. Stakeholder

| Nr. | Stakeholder | Interessen | Einfluss | Bedeutung des Produkts | Systemzugang |
|---|---|---|---|---|---|
| S1 | Inhaber/in der Spedition | Kosten im Griff, Kunden halten, einfache Einführung | hoch | hoch | Admin |
| S2 | Disponent/in | weniger Telefonate, jederzeit aktueller Stand, Kunden schnell informieren | hoch | hoch | Disponent |
| S3 | Fahrer/in | klare Aufträge in der eigenen Sprache, keine Anrufe während der Fahrt, keine Ortung in der Pause | gering | hoch | Fahrer |
| S4 | Fuhrparkmanager/in | Überblick, welches Fahrzeug wo eingesetzt ist | gering | gering | keiner (offen) |
| S5 | Kunde der Spedition (Auftraggeber, Empfänger) | pünktliche Lieferung, frühe Information bei Verspätung | hoch | gering | keiner |

Stakeholdermatrix, Zielgruppencluster und Personas: [[Stakeholder-und-Personas]]

> [!question] Offene Entscheidung
> Der Fuhrparkmanager hat im aktuellen Funktionsumfang keine Aufgabe. Führen wir ihn als Stakeholder ohne Systemzugang weiter oder streichen wir ihn?

## 3. Rollen im System

| Rolle | Aufgabe im System |
|---|---|
| **Fahrer** | nutzt die Fahrer-App: Tour ansehen, Status melden, chatten |
| **Disponent** | nutzt den Leitstand: Touren planen und zuweisen, Live-Karte, Chat, Vorschläge von Winston freigeben |
| **Admin** | verwaltet Benutzer, Rollen und Einstellungen der Spedition |
| **Winston** (KI-Akteur) | erkennt Verspätungen und entwirft Nachrichten, sendet nie selbstständig |

## 4. Funktionale Anforderungen

Priorisierung nach MoSCoW. Im Kanban-Board entspricht Must der Priorität P0, Should P1 und Could P2.

| ID | Anforderung | Beschreibung | MoSCoW | User Story |
|---|---|---|---|---|
| FA-01 | Benutzerverwaltung und Anmeldung | Anmeldung mit E-Mail und Passwort. Der Admin legt Benutzer an, vergibt Rollen und deaktiviert Konten. | Must | US-01 |
| FA-02 | Tourenplanung | Der Disponent legt Touren mit Datum, Fahrzeug und mehreren Stopps an (Adresse, Zeitfenster, Reihenfolge). | Must | US-02 |
| FA-03 | Tourzuweisung und Anzeige | Der Disponent weist eine Tour einem Fahrer zu, die Tour erscheint in dessen Fahrer-App. | Must | US-02 |
| FA-04 | Statusmeldung | Der Fahrer meldet seinen Status (Abfahrt, Angekommen, Entladen, Pause, Problem, Tour beendet) mit einem Tipp. | Must | US-03 |
| FA-05 | Positionsübermittlung | Die App übermittelt die Position nur während einer aktiven Tour, nicht in der Pause und nicht nach Tourende. | Must | US-03 |
| FA-06 | Live-Karte | Der Leitstand zeigt alle aktiven Fahrer mit letzter Position und Status auf einer Karte. | Must | US-04 |
| FA-07 | Chat | Nachrichten zwischen Disponent und Fahrer, zugeordnet zur Tour | Must | US-05 |
| FA-08 | Foto-Upload | Der Fahrer lädt Fotos zu einem Stopp hoch, zum Beispiel Lieferschein oder Schaden. | Should | – |
| FA-09 | Digitale Unterschrift | Der Empfänger bestätigt die Ablieferung per Unterschrift in der Fahrer-App. | Should | – |
| FA-10 | Dashboard | Übersicht im Leitstand: Touren des Tages, offene Meldungen, Verspätungen | Should | – |
| FA-11 | ETA | voraussichtliche Ankunftszeit je Stopp, berechnet aus Position und Plan | Should | – |
| FA-12 | Auswertungen | Pünktlichkeit und erledigte Stopps je Zeitraum | Could | – |
| FA-13 | Offline-Modus | Die Fahrer-App speichert Meldungen ohne Netz und sendet sie später. | Could | – |
| FA-14 | Automatische Übersetzung | Oberfläche und Chat in DE, EN und PL. Nachrichten werden in die Sprache des Empfängers übersetzt, das Original bleibt abrufbar. | Must | US-05 |
| FA-15 | KI-Co-Disponent Winston | Winston erkennt Verspätungen und entwirft Nachrichten. Versendet wird erst nach Freigabe durch den Disponenten. | Should | US-06 |

**Summe:** 8 × Must · 5 × Should · 2 × Could. Was nicht umgesetzt wird (Won't), steht in Kapitel 6.

## 5. Nicht-funktionale Anforderungen

| ID | Kategorie | Anforderung | Prüfung |
|---|---|---|---|
| NFA-01 | Performance | Eine Statusmeldung erscheint in **unter 3 Sekunden** im Leitstand. | Zeitmessung von Tipp in der App bis Anzeige im Leitstand |
| NFA-02 | Datenschutz | Positionsdaten werden **nur während einer aktiven Tour** übermittelt. Bei Pause und nach Tourende findet keine Positionsübermittlung statt. Positionsdaten werden nach 30 Tagen gelöscht. | Test: Pause melden, danach entstehen keine neuen Positionen |
| NFA-03 | Kontrolle der KI | **Ohne Freigabe wird nichts gesendet.** Jede Freigabe und Ablehnung wird mit Benutzer und Zeitpunkt protokolliert. | Test: Vorschlag ohne Freigabe, es erfolgt kein Versand |
| NFA-04 | Bedienbarkeit Fahrer-App | Eine Statusmeldung braucht **einen Tipp**. Schaltflächen sind mindestens 48 × 48 px groß. | Review der Oberfläche |
| NFA-05 | Mehrsprachigkeit | Alle Texte der Oberfläche liegen in DE, EN und PL vor. Eine übersetzte Nachricht erscheint in **unter 5 Sekunden**. | Sprachumschaltung prüfen, Zeitmessung |
| NFA-06 | Erlernbarkeit | Ein neuer Disponent legt **ohne Schulung** in unter 10 Minuten seine erste Tour an. | Usability-Test mit einer Testperson |
| NFA-07 | Sicherheit | Datenübertragung nur verschlüsselt (HTTPS), Passwörter nur gehasht, Zugriff nur gemäß Rolle | Code-Review, Test der Rechte-Matrix |
| NFA-08 | Plattform | Leitstand in aktuellen Browsern (Chrome, Edge, Firefox), Fahrer-App auf aktuellen Android- und iOS-Smartphones, **ohne Einbau von Hardware** | Test auf den Zielgeräten |

> [!note] Abstimmung im Team
> Die Zielwerte „30 Tage“ (NFA-02), „5 Sekunden“ (NFA-05) und „10 Minuten“ (NFA-06) sind Vorschläge und werden im Team bestätigt.

## 6. Abgrenzung (Won't)

Folgendes gehört **nicht** zu FleetConnect:

- **Fuhrparkverwaltung:** Wartung, TÜV-Fristen, Tankvorgänge, Fahrzeugstammdaten über Kennzeichen und Bezeichnung hinaus
- **Telematik-Hardware** und Einbau in Fahrzeuge
- **Navigation und Routenoptimierung** (der Fahrer nutzt sein Navigationsgerät)
- **Rechnungsstellung und Abrechnung**
- **Arbeitszeiterfassung, Lenk- und Ruhezeiten, Tachograph**
- **Kundenportal** für Auftraggeber

## 7. Abhängigkeiten

- FA-06 (Live-Karte) setzt FA-05 (Positionsübermittlung) voraus.
- FA-11 (ETA) setzt FA-02 (Stopps mit Zeitfenster) und FA-05 voraus.
- FA-15 (Winston) setzt FA-11 (ETA) und FA-07 (Chat) voraus.
- FA-14 (Übersetzung) benötigt einen externen Übersetzungsdienst.

## 8. Änderungshistorie

| Version | Datum | Änderung |
|---|---|---|
| 0.1 | 15.09.2026 | Erstfassung: 5 Stakeholder, 15 funktionale und 8 nicht-funktionale Anforderungen, Abgrenzung |
