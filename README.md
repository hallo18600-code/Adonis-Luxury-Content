# ADONIS Slide-Studio

TikTok-Slideshows für Adonis Luxury, direkt im Handy-Browser. Gebaut nach dem Vorbild des Forma-Studios (`hallo18600-code/Forma/studio`).

## So funktioniert's

1. Seite öffnen (am iPhone: Teilen → „Zum Home-Bildschirm“).
2. Format wählen oder „Zufall“ lassen → „Neue Entwürfe“.
3. Entwurf antippen → „Alle in Fotos sichern“ → in TikTok als Foto-Slideshow posten.
4. „Text kopieren“ liefert die Caption mit Hashtags.

## Formate

Neu im Shop · Unter X € · Outfit-Ideen · Marken-Fokus · Welches? (A/B) · Old-Money-Regeln · Kollektion (4er-Raster) · Wie neu (Zustand)

Jeder Post: Titel-Slide → Teile → Abschluss-Slide („Link in Bio“). Drei Looks: Creme, Navy, Stein.

Bei Luxus-Hintergründen kommt etwa jedes 2. Mal die Handy-Abschlussfolie: „Link In Bio!“ über London im Winter (`assets/end_london*.jpg`, Unsplash, freie Lizenz) mit zwei iPhones, auf denen echte Shop-Screenshots zu sehen sind (`assets/shop_home.jpg` = Startseite, `assets/shop_grid1.jpg` = Produkte). Neue Produkt-Screenshots als `shop_grid2.jpg` … ablegen und in `SHOP_GRIDS` in `index.html` eintragen.

## Teile

- `products.json` ist ein Export der aktiven Shop-Produkte (Marke, Name, Art, Preis, Größe, Zustand, Bilder). Bilder kommen direkt vom Shopify-CDN.
- Verkaufte Teile unter „Teile“ antippen → werden ausgeschaltet.
- Eigene Teile mit Foto hinzufügen (bleiben nur auf diesem Gerät gespeichert).
- Neue Produkte: `products.json` neu exportieren (Claude: „aktualisiere products.json im adonis-studio aus dem Shop“).

## Technik

Eine Datei (`index.html`), kein Build. Slides werden auf Canvas gezeichnet (1080×1440 oder 4K). Freigestellte PNGs bekommen Schatten, Fotos mit Hintergrund werden als Karte gezeigt. Schriften lokal in `fonts/` (Open Font License).
