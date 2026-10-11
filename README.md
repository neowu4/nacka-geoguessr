# NackaGuessr 🗺️

GeoGuessr fast bara för **Nacka kommun**. Du släpps någonstans i Street View – Sickla, Boo, Saltsjöbaden, Fisksätra, Älta, Orminge… – och ska sätta en nål på kartan där du tror att du är.

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
- **Område:** spela hela Nacka eller välj en eller flera delar: Sickla, Nacka Forum, Jarlaberg, Ektorp & Duvnäs, Skuru, Björknäs, Tollare & Lännersta, Orminge & Boo öst, Saltsjöbaden & Fisksätra, Älta.
- **Tid:** ingen tidsgräns, 2 min eller 1 min per runda.
- **Låst vy (NMPZ):** du kan inte röra dig eller vrida kameran.
- **↺ Till start** tar dig tillbaka till startpunkten, **⇄ Byt plats** om en bild inte laddar.
- Mellanslag = gissa / nästa runda. Ditt rekord sparas i webbläsaren.

## Valfritt: dölj vägnamnen

Utan nyckel används Googles vanliga Street View-inbäddning, som visar vägnamn i bilden. Med en egen **Google Maps API-nyckel** (Maps JavaScript API aktiverat) döljs vägnamn och adress. Klistra in nyckeln i fältet på startskärmen – den sparas bara i din egen webbläsare.

## Data

- 389 platser (minst 30 per område), framtagna ur Googles Street View-täckning inom Nacka kommuns gräns, med vägnamn från OpenStreetMap (via OSRM).
- Kommungränsen kommer från OpenStreetMap (© OpenStreetMap-bidragsgivare, ODbL).
- Allt ligger inbäddat i `index.html`; `data.json` är samma data i separat fil.
