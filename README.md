# NackaVärmdöGuessr 🗺️

GeoGuessr fast bara för **Nacka och Värmdö**. Du släpps någonstans i Street View – Sickla, Boo, Saltsjöbaden, Gustavsberg, Ingarö, Djurö… – och ska sätta en nål på kartan där du tror att du är.

## Spela direkt

👉 **https://neowu4.github.io/nacka-geoguessr/**

## Kör lokalt

Kräver bara Python 3 (finns redan på Mac).

```bash
git clone https://github.com/neowu4/nacka-geoguessr.git
cd nacka-geoguessr
python3 -m http.server 8765
```

Öppna sedan **http://localhost:8765** i webbläsaren.

> Öppna inte `index.html` direkt som fil – Street View måste laddas via `http://localhost`.

## Så funkar spelet

- 5 rundor, max 5 000 poäng per runda. Ju närmare du gissar, desto fler poäng.
- **Område:** välj kommun i menyerna **Nacka** och **Värmdö** – hela kommunen, ett eller flera områden, eller båda kommunerna.
  - Nacka: Sickla, Nacka Forum, Jarlaberg, Ektorp & Duvnäs, Skuru, Björknäs, Tollare & Lännersta, Orminge & Boo öst, Saltsjöbaden & Fisksätra, Älta.
  - Värmdö: Gustavsberg, Mölnvik & Hemmesta, Ingarö, Mellersta Värmdö, Djurö & Stavsnäs, Norra Värmdö.
- **Tid:** ingen tidsgräns, 2 min, 1 min, 30, 15, 10 eller 5 sekunder per runda.
- **Ingen gång (NM):** du kan vrida dig (dra eller piltangenter) och zooma (scrolla) men inte gå. Utan API-nyckel laddas bilden om i nya riktningen när du släpper, så det tar en sekund innan den nya vyn syns.
- **Låst vy (NMPZ):** du kan inte röra dig eller vrida kameran.
- **↺ Till start** tar dig tillbaka till startpunkten, **⇄ Byt plats** om en bild inte laddar.
- Mellanslag = gissa / nästa runda. Ditt rekord sparas i webbläsaren.

## Valfritt: dölj vägnamnen

Utan nyckel används Googles vanliga Street View-inbäddning, som visar vägnamn i bilden. Med en egen **Google Maps API-nyckel** (Maps JavaScript API aktiverat) döljs vägnamn och adress. Klistra in nyckeln i fältet på startskärmen – den sparas bara i din egen webbläsare.

## Data

- 613 platser (403 i Nacka, 210 i Värmdö, minst 30 per område), framtagna ur Googles Street View-täckning inom kommungränserna, med vägnamn från OpenStreetMap (via OSRM).
- Kommungränserna kommer från OpenStreetMap (© OpenStreetMap-bidragsgivare, ODbL).
- Allt ligger inbäddat i `index.html`; `data.json` är samma data i separat fil.
