# 🚚 **FleetConnect – Projektübersicht**

## 🔵 **Willkommen bei FleetConnect**

FleetConnect ist eine moderne Plattform für Speditionen, Disponenten und Fahrer. Ziel: **Touren planen, Fahrerstatus sehen, Dokumente verwalten und Kommunikation vereinfachen – alles in einem System.**

Diese Startseite ist der zentrale Einstiegspunkt für alle Projektunterlagen.

## 🎯 **Worum es geht**

FleetConnect ist ein Dispositionssystem für **kleine Speditionen mit 2–20 Lkw und 1–3 Disponenten**. Im Mittelpunkt steht der Arbeitsablauf:

> Disponent plant Tour mit Stopps → weist Fahrer zu → Fahrer meldet Status mit einem Tipp → GPS läuft nur während der Tour → Disponent sieht Live-Karte → Chat mit Auto-Übersetzung → Winston schlägt bei Verspätung Nachrichten vor, der Mensch gibt frei.

- **USP 1 – Mehrsprachigkeit:** Oberfläche und Chat werden automatisch übersetzt (DE/EN/PL), das Original bleibt abrufbar.
- **USP 2 – Winston:** Der KI-Co-Disponent erkennt Verspätungen und entwirft Nachrichten, der Disponent gibt frei.
- **Rollen:** Fahrer, Disponent, Admin und Winston als KI-Akteur
- **Nicht im Umfang:** Fuhrparkverwaltung (Wartung, TÜV-Fristen, Tankvorgänge)

## 📁 **Dokumentationsstruktur**

### **Projekt & Organisation**

- [[00_Admin/]] – Team, Planung, Organisation
    
- [[01_Projekt/]] – Projektbeschreibung, Ziele, Vision
    - [[Marktanalyse]] – Wettbewerber, Marktlücke, Positionierung
    - [[USP]] – Alleinstellungsmerkmale im Vergleich
### **Fachliche Inhalte**

- [[02_Anforderungen/]] – Lastenheft, Pflichtenheft
    - [[Anforderungen]] – 5 Stakeholder, 15 funktionale und 8 nicht-funktionale Anforderungen, Abgrenzung
    
- [[03_UseCases/]] – Use‑Cases, User‑Stories
    - [[use-case.png|Use-Case-Diagramm]] ([[use-case.puml|Quelle]]) – 14 Use Cases, 4 Akteure
    - [[User-Stories]] – US-01 bis US-06 mit Akzeptanzkriterien und Rückverfolgbarkeit
    - [[Stakeholder-und-Personas]] – Stakeholdermatrix, Zielgruppencluster, 3 Personas, Rechte-Matrix
    
- [[04_Architektur/]] – Systemarchitektur, Diagramme
    - [[klassendiagramm.png|Klassendiagramm]] ([[klassendiagramm.puml|Quelle]]) – 11 Klassen, 4 Enums
    - [[sequenz-statusmeldung.png|Sequenzdiagramm Statusmeldung]] ([[sequenz-statusmeldung.puml|Quelle]]) – vom Tipp in der App bis zum Disponenten-Dashboard
    
- [[05_Datenbank/]] – ERM, Tabellen, Beziehungen
### **Design & Umsetzung**

- [[06_Design/]] – UI/UX, Mockups, Styleguide
    - [[prototyp.html|Klickprototyp]] – Leitstand, Fahrer-App, Winston, Sprachumschaltung (im Browser öffnen)
    
- [[07_Implementierung/]] – Code‑Struktur, Module, Klassen
    
- [[08_Tests/]] – Testfälle, Testpläne
### **Abschluss**

- [[09_Dokumentation/]] – Benutzerhandbuch
    
- [[10_Praesentation/]] – Folien, Pitch
    
- [[99_Anhaenge/]] – PDFs, Bilder, externe Dateien