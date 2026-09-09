# CodeCreatures

Single-file HTML5 collectible / battle game. Scan barcodes or QR codes to unlock creatures and items, build a team of 3, and auto-battle.

**Play:** open `index.html` over HTTPS or `http://localhost` (camera needs a secure context). On `file://`, use **Manual Entry** or **Simulate Scan**.

> **Note:** In-app HTML previews often sandbox the page and block `localStorage`. The game still runs in memory there; open the [GitHub Pages site](https://garandwolf.github.io/CodeCreatures/) (or `localhost`) in a normal browser tab for lasting saves.

## Features

- Camera barcode scan (UPC / EAN / QR via ZXing CDN) + manual entry + Simulate Scan
- Deterministic pulls (FNV-1a) — same code → same reward (~⅔ creature / ~⅓ item)
- 24-hour cooldown per barcode
- 11 creatures across Ember / Tide / Growth (incl. Tide legendary **Krakensoul**)
- Items (weapon / armor / charm), equip one per creature
- Trading-card Collection UI, team of 3, auto-battles
- Export / Import save (`localStorage` key `codecreatures-save`)

## Quick start

```bash
python3 -m http.server 8080
# open http://localhost:8080/
```

Or open `index.html` directly and use Simulate Scan.

## Save format

Progress lives in `localStorage` under `codecreatures-save` (creatures, items, equipment, team, scanLog). Export/Import from the Collection screen.

## License

MIT
