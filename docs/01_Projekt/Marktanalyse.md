# Marktanalyse – FleetConnect

| | |
|---|---|
| **Projekt** | FleetConnect – Dispositionssystem für kleine Speditionen |
| **Dokument** | Marktanalyse |
| **Stand** | 15.09.2026 |
| **Team** | Christina Kiesl, AceSaft296, Niklas Bäricke |

## 1. Zielmarkt

FleetConnect richtet sich an **kleine Speditionen und Transportunternehmen mit 2–20 Lkw und 1–3 Disponenten**.

- Im gewerblichen Güterkraftverkehr in Deutschland gibt es **46.902 Unternehmen** (Stichtag Oktober 2020). [1]
- Die Branche ist kleinteilig. Laut BAG-Strukturbericht (Datenstand November 2011) setzen **83 %** der gewerblichen Unternehmen weniger als 10 Fahrzeuge ein, 53 % sogar nur ein bis drei. [2]

In solchen Betrieben ist Disposition Handarbeit: Eine Person plant die Touren, telefoniert mit den Fahrern und beantwortet gleichzeitig Kundenanfragen.

## 2. Ausgangslage der Zielgruppe

### 2.1 Fahrermangel

- Laut BGL fehlen in Deutschland **über 70.000 Lkw-Fahrer** (Januar 2026). 2018 waren es rund 40.000. [3]
- Rund ein Drittel der Berufskraftfahrer ist älter als 55 Jahre. Jedes Jahr gehen 30.000–35.000 Fahrer in Rente, aber nur 15.000–20.000 kommen neu dazu. [3]
- Speditionen setzen deshalb vermehrt ausländische Fahrer ein: **23,6 %** der Berufskraftfahrer im Lkw-Güterverkehr hatten 2020 eine ausländische Staatsangehörigkeit. [4]

**Folge für die Disposition:** Disponent und Fahrer sprechen immer öfter nicht dieselbe Muttersprache. Telefonische Anweisungen werden missverstanden, Rückfragen kosten Zeit.

### 2.2 Belastung der Disposition

In kleinen Speditionen gibt es kaum Vertretung. Ist der Disponent im Dauertelefonat oder fällt aus, steht die Kommunikation still. Typische Zeitfresser sind:

- Fahrern hinterhertelefonieren („Wo bist du gerade? Wann bist du da?“)
- Kunden über Verspätungen informieren
- den aktuellen Stand aus Anrufen, Messenger-Nachrichten und Notizzetteln zusammensetzen

### 2.3 Status quo in kleinen Speditionen

| Werkzeug | Einsatz | Schwäche |
|---|---|---|
| Telefon | Status abfragen, Anweisungen geben | unterbricht Fahrer und Disponent, nichts ist dokumentiert |
| WhatsApp / Messenger | Fotos, kurze Absprachen | private Konten, keine Zuordnung zur Tour, datenschutzrechtlich heikel |
| Excel / Papier | Tourenplanung | kein Live-Stand, doppelte Pflege |

## 3. Wettbewerber

### 3.1 Webfleet (Webfleet Solutions)

Etablierte Telematik-Plattform für Flotten jeder Größe.

- **Hardware:** Die Ortung läuft über LINK-Fahrzeuggeräte, die Tarife sind an diese Geräte gebunden. [5]
- **Vertrag:** Vertriebspartner bieten die Tarife mit **24 Monaten Laufzeit** inklusive Datenflatrate an. Preise gibt es nur auf Anfrage. [5]
- **Disposition:** Aufträge versenden, Status und voraussichtliche Ankunftszeiten abrufen, Zwei-Wege-Nachrichten an das PRO-Fahrerterminal. [6]
- **Übersetzung:** In den ausgewerteten Produktinformationen findet sich keine Angabe zu automatischer Übersetzung zwischen Disponent und Fahrer.
- **Einordnung:** Funktional stark, für 2–20 Lkw aber aufwendig: Hardware, Vertragsbindung und Einarbeitung.

### 3.2 Vimcar Fleet

Anbieter mit Schwerpunkt auf Fahrzeugortung und digitalem Fahrtenbuch.

- **Hardware:** OBD-Stecker oder Box pro Fahrzeug [7]
- **Preise (netto pro Fahrzeug und Monat):** Fleet Geo 13,90 €, Fleet Fahrtenbuch 19,90 € im ersten Jahr und danach 24,90 €, Fleet Fahrtenbuch Pro 29,90 € [7]
- **Vertrag:** jährliche Zahlung im Voraus, automatische Verlängerung um 12 Monate, 30 Tage Geld-zurück-Garantie für Neukunden [7]
- **Funktionen:** GPS-Live-Ortung, Routendokumentation, finanzamtkonformes Fahrtenbuch, Fahrer-Apps [7]
- **Einordnung:** Günstig und schnell eingerichtet. Vimcar löst Ortungs- und Fahrtenbuchfragen, aber nicht die Disposition. Tourenplanung, Fahrer-Chat und Übersetzung werden in der Paketübersicht nicht genannt.

### 3.3 Status quo: Telefon, WhatsApp, Excel

Kostet nichts und braucht keine Einführung. Deshalb ist der Status quo der eigentliche Hauptkonkurrent. Die Kosten fallen versteckt an: als Telefonzeit, durch Missverständnisse und durch fehlende Dokumentation.

## 4. Vergleich

| Kriterium | Webfleet | Vimcar Fleet | Status quo | **FleetConnect** |
|---|---|---|---|---|
| Hardware im Fahrzeug | ja, LINK-Gerät | ja, OBD-Stecker oder Box | nein | **nein, Smartphone genügt** |
| Vertragsbindung | 24 Monate (Partnertarife) | 12 Monate, Zahlung jährlich im Voraus | keine | **monatlich kündbar** |
| Tourenplanung und Zuweisung | ja (Aufträge) | – | Excel oder Papier | **ja** |
| Statusmeldung durch den Fahrer | ja | – | Anruf oder Messenger | **ein Tipp in der App** |
| Live-Ortung | ja | ja | nein | **nur während aktiver Tour** |
| Kommunikation mit dem Fahrer | Nachrichten an das PRO-Terminal | – | Telefon, WhatsApp | **Chat je Tour** |
| Automatische Übersetzung | – | – | nein | **DE/EN/PL, Original abrufbar** |
| KI-Entwurf von Nachrichten bei Verspätung | – | – | nein | **Winston, Versand nur nach Freigabe** |

„–“ = in den ausgewerteten Quellen nicht genannt.

## 5. Marktlücke

Zwischen großen Telematik-Plattformen und dem Status quo fehlt ein Werkzeug, das

1. **ohne Einbau und ohne lange Vertragsbindung** startet,
2. den **Arbeitsablauf der Disposition** abbildet (Tour → Zuweisung → Status → Karte → Chat) statt nur Ortung oder Fahrtenbuch und
3. die zwei drängendsten Personalprobleme angeht: **Sprachbarrieren** durch internationale Fahrer und **überlastete Disponenten**.

## 6. Positionierung

> FleetConnect ist die Disposition für kleine Speditionen ohne Einbau und ohne Schulung: Touren planen, Status per Tipp, Live-Karte nur während der Tour, Chat mit automatischer Übersetzung – und Winston, der bei Verspätungen Nachrichten vorschlägt, die der Disponent freigibt.

- **Zielkunde:** Inhaber und Disponenten von Speditionen mit 2–20 Lkw
- **Nutzenversprechen:** weniger Telefonate, weniger Missverständnisse, Kunden früher informiert
- **Marktposition:** kein Einbau, keine Schulung, monatlich kündbar, DSGVO by Design (Ortung nur während aktiver Tour, Pause = Tracking aus)
- **Abgrenzung:** keine Fuhrparkverwaltung (Wartung, TÜV-Fristen, Tankvorgänge), keine Telematik-Hardware

## 7. Risiken und Hinweise

- **Der Status quo ist kostenlos.** FleetConnect muss seinen Nutzen in den ersten Tagen zeigen, sonst bleibt der Betrieb bei Telefon und WhatsApp.
- **Große Anbieter können nachziehen**, etwa mit Übersetzungsfunktionen. Unser Vorsprung liegt in der Einfachheit für kleine Betriebe.
- **Namensgleichheit:** Die *FLEET Connect GmbH* aus Leipzig ist Webfleet-Partner und bietet Telematik und digitales Auftragsmanagement an, also im selben Markt. [8] Für ein echtes Produkt müsste der Name rechtlich geprüft oder geändert werden.

## Quellen

Alle Quellen abgerufen am 15.09.2026.

1. BAG (heute BALM): *BAG veröffentlicht Unternehmensstatistik des Güterkraftverkehrs*, Pressemitteilung vom 06.10.2021. https://www.balm.bund.de/SharedDocs/Pressemitteilungen/DE/2021/2021_10_06_PM_52_BAG_veroeffentlicht_Unternehmensstatistik_des_Gueterkraftverkehrs_USTAT19.html
2. eurotransport: *BAG-Strukturbericht: Kleine und Mittelständler dominieren*, 30.03.2012. https://www.eurotransport.de/logistik/spedition-und-logistik/bag-strukturbericht-kleine-und-mittelstaendler-dominieren/
3. eurotransport: *Fahrermangel im Güterverkehr verschärft sich: Über 70.000 Lkw-Fahrer fehlen in Deutschland*, 29.01.2026. https://www.eurotransport.de/fahrer/bkf-news/fahrermangel-ueber-70-000-lkw-fahrer-fehlen-in-deutschland-2026/
4. VerkehrsRundschau: *Jeder vierte Berufskraftfahrer Deutschlands stammt aus dem Ausland*, 17.01.2022 (Studie des IW Köln). https://www.verkehrsrundschau.de/nachrichten/transport-logistik/jeder-vierte-berufskraftfahrer-deutschlands-stammt-aus-dem-ausland-3118294
5. euro-tel: *Webfleet-Tarife und Preise*. https://euro-tel.net/webfleet-tarife-und-preise.html
6. Webfleet: *WEBFLEET Mobile – Funktionen*. https://www.webfleet.com/de_at/webfleet/products/webfleet/features/mobile/features/
7. Vimcar: *Vimcar Fleet Pakete im Überblick*. https://www.vimcar.de/flottenmanagement/preise-pakete
8. FLEET Connect GmbH: Website. https://www.fleetconnect.de/
