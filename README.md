<h1>
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="logo/telaiojs-logo-dark.svg">
    <img src="logo/telaiojs-logo.svg" alt="TelaioJS" width="300">
  </picture>
</h1>

**A page-layout program for print shops. It is used the way QuarkXPress is used, and it makes PDFs ready for press.**

> *Telaio* is Italian for the chase: the iron frame in which movable type is set and then locked up for the press. The T of the name is the key that locks it.

This repository holds the installers of TelaioJS and their updates. The program's code is not here.

## Download

**[Try it first](https://telaiojs.contea.casa)**, in the browser, with nothing to install: each visitor gets a copy of TelaioJS of their own, with the two example jobs in it, for two hours. **Connect your own AI to it**: the blue strip at the top of the demo gives an address for your copy, which an AI assistant that speaks MCP (Claude, for instance) connects to, and then lays out pages with you while you watch. The demo takes up to four pictures of your own, 10 MB each, deleted with the copy, and no fonts; its PDFs say DEMO across every page.

**[TelaioJS for Windows](https://github.com/Fr4nZ82/telaiojs-releases/releases/latest)**: the installer, `TelaioJS-Setup-<version>.exe`, for Windows 10 and 11 (64-bit). Each release also carries the manual (`TelaioJS-Manual.md`) and the notices of the other authors' software. What each version changed is in the [changelog](CHANGELOG.md).

- **One installer for every computer of the shop.** On the computer that will run TelaioJS, choose *This computer runs TelaioJS*; on the others, *This computer uses TelaioJS running on another computer*.
- **Windows may stop it the first time** (*Windows protected your PC*): *More info*, then *Run anyway*. The installer is not signed with a certificate.
- **It updates itself** from this page: a new version is downloaded, checked against LNPrint's signature, and installed the next time the computer starts.
- **Two example jobs** come with it, in `Documents\Telaio\Examples`: a flyer and a business card to open and take apart.
- **It works for 14 days**, then with a key from LNPrint, typed in `Preferences > Program`. Without a key the jobs still open and can be looked at; nothing is lost.
- **For a key**, or anything else about TelaioJS, write to LNPrint: [fr4nz82@gmail.com](mailto:fr4nz82@gmail.com).

## How it is used

TelaioJS runs on one computer of the shop and has no window of its own: it is used in the browser. At first it answers only the computer it runs on. Once someone there opens it to the network, in `Preferences > Network`, with a password, the other computers of the shop open its address in their browser and work on the same jobs.

## What it does

- **Pages:** long documents, facing pages, master pages with automatic page numbers, margins, bleed and guides. Pieces laid on a press sheet, each with its trim box and its crop marks, repeated with Step and Repeat.
- **Boxes and lines:** rectangles, rounded rectangles, ovals, polygons, stars, and free shapes drawn with a pen that behaves as Illustrator's does. Moved, resized and turned by hand or by the numbers, about a nine-point reference grid. Grouping, stacking, alignment and locking. Blends, frames, shade and opacity, drop shadows.
- **Text:** set with the font's own measurements, so the screen and the PDF break lines in the same places. Justification and hyphenation in four languages, tabs, paragraph and character style sheets. One story runs through linked boxes across pages and around the items in front of it; a picture can sit in the line and move with the text.
- **Tables:** drawn on the page or set in the text, where a long one breaks across columns and pages with its header and footer repeated. Cells take text or a picture, with lines, fills, alternate rows and alignment on the decimal comma. Selected text, or cells copied from a spreadsheet, become a table.
- **Fonts:** the shop's own TrueType and OpenType faces are uploaded once, and every document has them.
- **Pictures:** JPEG, PNG, TIFF and the like; PDF and Illustrator files, placed by a page and a box and carried into the PDF as vector; EPS, through Ghostscript, which the installer offers to install. A light preview on screen, the original at full resolution in the PDF.
- **Colour:** CMYK process colours and named spot inks, for one printing condition, FOGRA39 (offset on coated paper): a colour picked on screen becomes the recipe that press prints it with, and every ink is shown on screen as it prints.
- **Overprint and the plates:** a colour overprints when its box is ticked — Black does in a new document, so black text leaves no white halo — and the Separations palette shows the page plate by plate, as the PDF prints it, a placed PDF's own inks included.
- **The PDF for press:** set by the same typesetter as the screen; fonts embedded; pictures at full resolution, CMYK kept as CMYK, RGB converted through FOGRA39; every spot ink on a separation plate of its own; bleed written into the file; facing pages as single pages, reader spreads, or printer spreads for a folded booklet; PDF/X-4 for the printer when it is asked for.
- **The shop's archive:** Save writes the job as a `.telaio` file into the customer's folder, on the computer or on a shared disk, with the pictures it uses beside it. Open from Disk brings it back. Unsaved work is copied automatically as you go.
- **Two hands on one job:** the same job open on two computers shows each one's work in the other as it is made. Each person has their own undo.
- **An AI that lays out the page:** an AI assistant that speaks MCP (the standard way an assistant uses outside tools; Claude, for instance) connects to the program and makes documents with it, while a person watches and works alongside. It can do what the editor can, and it looks at its own pages before exporting. TelaioJS holds no AI key and makes no AI calls: the assistant is your own.

## What it does not do

- PDF/X-4 only: no PDF/X-1a or X-3, which forbid transparency.
- One printing condition, FOGRA39: no other, and no choice of rendering intent.
- No crop marks round a page, on purpose: where they go depends on the press and the finishing. Pieces laid on a press sheet get them from their trim boxes.
- On the shop's network the program speaks plain http: the password and the documents cross the network unencrypted.

## Licence

TelaioJS is proprietary software, © 2026 LNPrint: see [LICENSE](LICENSE). It includes software by other authors under their own licences, listed with each release.
