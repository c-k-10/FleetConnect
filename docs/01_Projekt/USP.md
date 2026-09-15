# USP – FleetConnect

| | |
|---|---|
| **Projekt** | FleetConnect – Dispositionssystem für kleine Speditionen |
| **Dokument** | Alleinstellungsmerkmale (USP) |
| **Stand** | 15.09.2026 |
| **Grundlage** | [[Marktanalyse]] |

## Kernaussage

**FleetConnect bringt Disponent und Fahrer ohne Sprachbarriere zusammen und nimmt dem Disponenten Routinekommunikation ab, ohne ihm die Entscheidung abzunehmen.**

## Die zwei Alleinstellungsmerkmale

### USP 1 – Mehrsprachigkeit gegen den Fahrermangel

- Oberfläche und Chat werden automatisch übersetzt: **Deutsch, Englisch, Polnisch**.
- Das Original bleibt jederzeit abrufbar. Bei Unklarheiten zählt, was wirklich geschrieben wurde.
- Jeder schreibt in seiner Sprache und liest in seiner Sprache.
- **Nutzen:** Fahrer mit wenig Deutschkenntnissen verstehen Aufträge und Anweisungen sicher. Das erweitert den Kreis der Fahrer, die eine Spedition einsetzen kann.

### USP 2 – Winston gegen den Disponentenmangel

- Der KI-Co-Disponent **erkennt Verspätungen** anhand von Position und Tourplan.
- Winston **entwirft passende Nachrichten**, zum Beispiel an den Kunden oder an den Fahrer.
- **Human in the Loop:** Ohne Freigabe durch den Disponenten wird nichts gesendet.
- **Nutzen:** Ein Disponent betreut mehr Touren, ohne die Kontrolle abzugeben.

## Marktposition

| Versprechen | Bedeutung für den Kunden |
|---|---|
| **Kein Einbau** | Smartphone-App statt Fahrzeuggerät |
| **Keine Schulung** | Statusmeldung mit einem Tipp, selbsterklärender Leitstand |
| **Monatlich kündbar** | kein Risiko durch lange Verträge |
| **DSGVO by Design** | Ortung nur während aktiver Tour, Pause = Tracking aus |

## USP-Tabelle: Konkurrenz und eigene Lösung

| Merkmal | Webfleet | Vimcar Fleet | Status quo | **FleetConnect** |
|---|---|---|---|---|
| Einstieg | LINK-Gerät, 24 Monate Laufzeit | OBD-Stecker oder Box, 12 Monate Laufzeit | sofort, aber ungeordnet | **App, monatlich kündbar** |
| Kommunikation Disponent–Fahrer | Nachrichten an das PRO-Terminal | – | Telefon, WhatsApp | **Chat je Tour** |
| Sprachbarriere | – | – | bleibt bestehen | **automatische Übersetzung DE/EN/PL** |
| Umgang mit Verspätungen | voraussichtliche Ankunftszeit abrufbar | – | Anruf beim Fahrer | **Winston erkennt sie und entwirft Nachrichten** |
| Kontrolle über KI-Nachrichten | – | – | – | **Versand nur nach Freigabe** |
| Ortung | über Fahrzeuggerät | über Stecker oder Box | keine | **nur während aktiver Tour** |

„–“ = in den ausgewerteten Quellen nicht genannt. Quellen und Details: [[Marktanalyse]].

## Rückverfolgbarkeit

| USP | Anforderungen | User Story |
|---|---|---|
| Mehrsprachigkeit | FA-07, FA-14, NFA-05 | US-05 |
| Winston | FA-15, NFA-03 | US-06 |
| DSGVO by Design | FA-05, NFA-02 | US-03 |
| Keine Schulung | NFA-04, NFA-06 | US-02, US-03 |
| Kein Einbau | NFA-08 | US-03 |
