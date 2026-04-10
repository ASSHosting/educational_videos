# Lehrvideos – Übersicht

Browserbasierte Übersicht aller Lehrvideos, ausgespielt unter [videos.ki-lernarchitekt.de](https://videos.ki-lernarchitekt.de).
Die Videos sind nach **Thema** sortiert. Pro Video zeigt ein Tag die ursprüngliche Zielgruppe (VHS, BDS oder Allgemein).

## Projektstruktur

```text
.
├── index.html
├── README.md
├── ai-security/      KI verstehen und sicher einsetzen
├── cloud_data/       Cloud-Strategien und digitale Organisation
├── online_security/  Online-Sicherheit und Betrugserkennung
└── data-science/     Data Science und Datenvisualisierung
```

Die Themen-Ordnerstruktur ist analog zum Repo [`education_games`](https://github.com/arno-schimmelpfennig/education_games).

## Funktionen der Übersicht (`index.html`)

- Kategorisierte Anzeige nach Thema
- Audience-Tag pro Video (VHS / BDS / Allgemein)
- Globale Suche über Titel, Kategorie und Audience
- Kategorie-Filter bei Kategorien mit mehr als 3 Videos
- Lightbox-Player direkt in der Übersicht
- Button `Filter zurücksetzen`

## Neues Video hinzufügen

1. MP4-Datei in den passenden Themen-Ordner legen.
2. In `index.html` den `videoData`-Array öffnen, im passenden Thema einen Eintrag ergänzen:

```js
{
  name: "Titel des Videos",
  file: "ai-security/dateiname.mp4",
  audience: "VHS"  // oder "BDS" oder "Allgemein"
}
```

3. Für ein neues Thema einen neuen Block in `videoData` ergänzen:

```js
{
  title: "Neues Thema",
  videos: [
    { name: "Beispiel", file: "neuer-ordner/beispiel.mp4", audience: "Allgemein" }
  ]
}
```

## Lokal starten

```bash
python -m http.server 8000
```

Im Browser: `http://localhost:8000/`
