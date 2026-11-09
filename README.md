# Gründach-Audiowalk Osnabrück

Web-App für den Audiowalk zur Dachbegrünung in der Osnabrücker Innenstadt.
Fünf Stationen (Neumarkt → Nikolaiort → Rathaus → Domhof → Hase) plus Bonus-Station Campus Haste.

## Inhalte bearbeiten

Alle Texte stehen oben im Script-Teil von `src/page.html` im Block `STATIONS`:

- `title`, `where` – Name und Ort der Station
- `lat`, `lng` – Koordinaten (vor dem Einsatz vor Ort prüfen!)
- `look` – „Blick nach oben“-Aufgabe
- `text` – Sprechtext (wird ohne Aufnahme von der Computerstimme gelesen)
- `question` – Diskussionsfrage
- `audio` – Pfad zur eigenen Aufnahme, z. B. `"audio/01-neumarkt.mp3"`

Eigene Aufnahmen als MP3 in `public/audio/` legen. Danach:

```bash
./build.sh
```

## Online stellen (Vercel)

```bash
npx vercel          # Vorschau-Link
npx vercel --prod   # endgültiger Link
```

Beim ersten Mal fragt Vercel nach Login und Projektnamen.

## Funktionen

- Routenplan (maßstäblich, ohne externe Kartendienste)
- Standortanzeige und Hinweis, sobald man weniger als 35 m von einer Station entfernt ist
- Audio-Player: eigene MP3 oder Computerstimme als Platzhalter
- Fortschritt (erledigte Stationen) wird im Browser gespeichert
- Links zu OpenStreetMap je Station
