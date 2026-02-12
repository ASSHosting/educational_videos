# Lehrvideos – Übersicht

Diese Sammlung enthält Lehrvideos für drei Bereiche:

- VHS-Kurse
- BDS KI-Akademie
- Unterricht allgemein

Die Startseite `index.html` zeigt alle Videos kategorisiert an und verlinkt direkt auf die MP4-Dateien.

## Projektstruktur

```text
.
├── index.html
├── README.md
├── vhs/
├── bds/
└── educational/
```

## Funktionen der Übersicht (`index.html`)

- Kategorisierte Anzeige aller Videos
- Aussagekräftige Video-Titel statt nur Dateinamen
- Globale Suche über Titel, Kategorie und Dateipfad
- Kategorie-Filter nur bei Kategorien mit mehr als 3 Videos
- Button `Filter zurücksetzen` für Suche + alle aktiven Kategorie-Filter

## Neue Videos hinzufügen

Die Übersicht ist datengetrieben aufgebaut.

1. In `index.html` den Bereich `videoData` öffnen.
2. In der passenden Kategorie einen neuen Eintrag unter `videos` ergänzen:

```js
{
  name: "Titel des Videos",
  file: "ordner/datei.mp4"
}
```

3. Für eine neue Kategorie einen neuen Block in `videoData` ergänzen:

```js
{
  title: "Neue Kategorie",
  folder: "neuer-ordner/",
  videos: [
    { name: "Beispiel", file: "neuer-ordner/beispiel.mp4" }
  ]
}
```

## Lokal starten

Im Projektordner:

```bash
python -m http.server 8000
```

Dann im Browser öffnen:

`http://localhost:8000/`
