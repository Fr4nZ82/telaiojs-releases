# TelaioJS

**A page-layout program for print shops. It is used the way QuarkXPress is used, and it makes PDFs
ready for press.**

> *Telaio* is Italian for loom, or frame: the chase that holds movable type in a letterpress.

This repository holds the installers of TelaioJS and their updates. The program's code is not here.

## Download

There is no release yet.

## How it is used

TelaioJS runs on one computer of the shop and has no window of its own: it is used in the browser. At
first it answers only the computer it runs on. Once someone there opens it to the network, in
`Preferences > Network`, with a password, the other computers of the shop open its address in their
browser and work on the same jobs.

## What it does

- **Pages:** long documents, facing pages, master pages with automatic page numbers, margins, bleed and
  guides.
- **Boxes and lines:** rectangles, rounded rectangles, ovals, polygons, stars, and free shapes drawn with
  a pen that behaves as Illustrator's does. Moved, resized and turned by hand or by the numbers, about a
  nine-point reference grid. Grouping, stacking, alignment and locking. Blends, frames, shade and
  opacity, drop shadows.
- **Text:** set with the font's own measurements, so the screen and the PDF break lines in the same
  places. Justification and hyphenation in four languages, tabs, paragraph and character style sheets.
  One story runs through linked boxes across pages and around the items in front of it; a picture can
  sit in the line and move with the text.
- **Fonts:** the shop's own TrueType and OpenType faces are uploaded once, and every document has them.
- **Pictures:** JPEG, PNG, TIFF and the like; a light preview on screen, the original at full resolution
  in the PDF.
- **Colour:** CMYK process colours and named spot inks.
- **The PDF for press:** set by the same typesetter as the screen; fonts embedded; pictures at full
  resolution, CMYK kept as CMYK; every spot ink on a separation plate of its own; bleed written into the
  file; facing pages as single pages, reader spreads, or printer spreads for a folded booklet.
- **The shop's archive:** Save writes the job as a `.telaio` file into the customer's folder, on the
  computer or on a shared disk, with the pictures it uses beside it. Open from Disk brings it back.
  Unsaved work is copied automatically as you go.
- **Two hands on one job:** the same job open on two computers shows each one's work in the other as it
  is made. Each person has their own undo.
- **An AI that lays out the page:** an AI assistant that speaks MCP (the standard way an assistant uses
  outside tools; Claude, for instance) connects to the program and makes documents with it, while a
  person watches and works alongside. It can do what the editor can, and it looks at its own pages
  before exporting. TelaioJS holds no AI key and makes no AI calls: the assistant is your own.

## What it does not do

- The PDF is correct for press but does not claim PDF/X.
- A logo in PDF or EPS cannot be placed: pictures come in as pixels.
- No tables.
- No crop marks, on purpose: where they go depends on the press and the finishing, so they are drawn on
  the page by hand.
- On the shop's network the program speaks plain http: the password and the documents cross the network
  unencrypted.

## Licence

TelaioJS is proprietary software, © 2026 LNPrint: see [LICENSE](LICENSE). It includes software by other
authors under their own licences, listed with each release.
