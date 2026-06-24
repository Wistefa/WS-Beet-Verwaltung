# 🌿 WS Beet-Verwaltung

Einfache Verwaltung von Gartenbeeten und Pflanzungen – als **Single-HTML-App** ohne Server, ohne Installation, direkt im Browser.

**Live:** [wistefa.github.io/WS-Beet-Verwaltung](https://wistefa.github.io/WS-Beet-Verwaltung/)

---

## Features

### 🌱 Meine Beete
- Beete anlegen und bearbeiten (Name, Maße, Standort, Notizen)
- Automatische Flächenberechnung (m²)
- Standort: Volle Sonne / Halbschatten / Schatten
- Anzahl Pflanzungen je Beet wird angezeigt

### 🌿 Pflanzungen
- Pflanzungen anlegen, bearbeiten und löschen
- Schnellauswahl aus 46 gängigen Hochbeet-Pflanzen (Dropdown nach Kategorien)
- Freitext-Eingabe für eigene Pflanzennamen
- Status: Gesät / Wächst / Geerntet / Gescheitert
- Filter nach Beet und Jahr
- Aussaat- und Pflanzungsdatum

### 📅 Saison-Kalender
- Monats-Navigator (◀ Monat ▶)
- 4 Karten aus eigenen Pflanzungsdaten:
  - **Jetzt pflanzen** – Aussaaten dieses Monats
  - **Zur Ernte bereit** – Pflanzungen mit Status "Wächst" seit über 6 Wochen
  - **Gießen** – alle aktiven Pflanzungen
  - **Nächste Schritte** – Aussaaten im Folgemonat
- **Allgemeiner Pflanzkalender** mit 46 Pflanzen und Monats-Highlighting (Quelle: aussaatkalender.com)

### 📊 Statistik
- Jahr-Navigator (◀ Saison ▶)
- KPI-Zeile: Beete, Pflanzungen, Geerntet, Erfolgsquote
- Top-Pflanzen nach Erfolgsquote (Balkendiagramm)
- Beet-Auslastung (aktive Pflanzungen je Beet)
- Pflanzungen pro Monat (Balkendiagramm)

---

## Technologie

| | |
|---|---|
| **Typ** | Single HTML File |
| **Framework** | Vanilla JS – kein Build-Schritt |
| **Persistenz** | `localStorage` (`bv_beete`, `bv_pflanzungen`) |
| **CSS** | Inline – kein externes Stylesheet |
| **Abhängigkeiten** | keine |

---

## Lokale Nutzung

```bash
# Datei einfach im Browser öffnen:
open index.html
```

Oder direkt online: [wistefa.github.io/WS-Beet-Verwaltung](https://wistefa.github.io/WS-Beet-Verwaltung/)

---

## Datenschema (localStorage)

```json
{
  "bv_beete": [
    { "id": "abc123", "name": "Hochbeet Nord", "laenge": 3.0, "breite": 1.2, "standort": "sonne", "notizen": "" }
  ],
  "bv_pflanzungen": [
    { "id": "def456", "pflanze": "Tomaten", "beetId": "abc123", "aussaat": "2026-03-15", "pflanzung": "2026-05-10", "status": "waechst", "notizen": "" }
  ]
}
```

---

## Changelog

| Version | Datum | Änderungen |
|---|---|---|
| 1.1.0 | 2026-06-24 | Pflanzkalender mit 46 Pflanzen und Monats-Highlighting |
| 1.0.1 | 2026-06-24 | Pflanzauswahl-Dropdown mit Kategorien (Chrome-Klick-Fix) |
| 1.0.0 | 2026-06-24 | Erstveröffentlichung: 4 Tabs, CRUD, Statistik, responsive |
