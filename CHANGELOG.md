# Changelog

What each version of TelaioJS changed, newest first. Every version is on the [releases page](https://github.com/Fr4nZ82/telaiojs-releases/releases), with its installer, its manual and the notices of the other authors' software. A TelaioJS already installed takes each new version by itself: it is downloaded, checked against its author's signature, and installed the next time the computer starts.

## 0.8.0 — 4 October 2026

- **A picture remembers its file.** A picture taken from the program's folders keeps where its file is, how big it was and when it was last changed.
- **The Usage window**, a new list button near the gear at the top right, shows what a job uses.
  - **Pictures**: every picture of the job — in a box, a table's cell or the text — with its page, its kind and the status of its file. **OK**; **Modified**, when the file has changed since it was placed (the customer sent the photo again under the same name); **Missing**; or **No file**, for a picture sent from a computer or tablet, or placed before this version. **Show** goes to it, **More** says where the file is and what it was and is now, and **Update** takes the file again for the pictures chosen, or every modified one, keeping each picture's scale and place in its box. One Undo puts them back. A missing picture is found again in the folder window.
  - **When you open a job** whose pictures have changed in their folders, TelaioJS asks: Update, Usage, or Not Now.
  - **Fonts**: every font the job's text and style sheets use, the styles of it asked for, where, and whether TelaioJS has it — OK, or Missing and the font it is shown in meanwhile. **Replace…** sets every use of a font in another, bold and italic kept, one Undo.
  - **The program's fonts are now in Usage > Fonts**, under the job's, where a missing font can be added at once; Preferences no longer has a Fonts pane. Importing a PDF that lacks fonts still asks for them in Missing Fonts, with the same list.
- **The Open window**, in a program that embeds TelaioJS and names its folder (`disk.label`), shows a job saved inside it from that name down ("Cartelle dei clienti › ROSSI_MARIO pizzeria › Biglietto Rossi.telaio"). Without a name, unchanged.
- **The manual** has a section on Usage (6d), and section 9 says where the fonts are now.
- **The AI** lists what a job uses (`list_usage`), takes changed pictures again (`update_picture`), replaces a font (`replace_font`), and is told when it opens a job whose pictures changed (`filesChanged`, `filesMissing`).

## 0.7.1 — 4 October 2026

- **Import Picture in the program and the online demo** works as in 0.7.0: it opens the program's folders, with This Device… for the device in hand.
- **For programs that embed TelaioJS**, what was made for one host is now each host's choice, and leaving it out keeps the program as it was:
  - `disk.pictures` turns on Import Picture's folder window: thumbnails, pixels, dpi and mm, the search, the program reading the file itself, and the AI's `upload_picture` `file` and `list_folder` `pictures`, `details` and `search`. Without it, Import Picture opens the device's file dialog, as before 0.7.0.
  - `disk.label` gives the default folder a name of the host's own ("Cartelle dei clienti"). The folder window and the AI's places call it so. Where the program reaches that folder only (`disk.only`), the path at the top of the window reads from that name down ("Cartelle dei clienti › ROSSI_MARIO pizzeria") and a path can be typed that way too.

## 0.7.0 — 4 October 2026

- **Pictures from the program's folders.** Import Picture — a double-click on an empty box, the right button's Import Picture, a picture for cells or an anchored item — opens the folder window of Save and Open from Disk, with the pictures (JPEG, PNG, GIF, WebP, AVIF, TIFF, PDF, Illustrator, EPS) of the folders the program's computer reaches, the shop's shared disk among them. The program reads the file chosen where it is: nothing is sent from the computer or tablet you work on, so it is quick on Wi-Fi and the same from every device. **This Device…** in the window sends a picture from the device in hand, as Import did before.
- **Each picture shown before it is taken.** Every row has a thumbnail (a PDF's, Illustrator's or EPS's first page), the picture's pixels, dpi and size in mm — the size it arrives at in the box — and says in orange when the picture would print under 300 dpi made to fill the box. A folder of thousands opens at once; thumbnails come as rows come into view.
- **Search.** A field in the window finds pictures by words of their names, in the folder and every folder inside it, accents and capitals not counting.
- **One folder only, kept.** Where TelaioJS is set to reach a single folder (inside another program, or the online demo), nothing outside it is shown, taken or saved — a shortcut leading out of it included — and the refusal names the folder.
- **The example jobs** are made again: their Black overprints, as a new document's does.
- **The manual** says how pictures are taken from the folders (section 6c).
- **The AI** takes a picture from the program's folders by its path (`upload_picture` `file`) without its bytes passing through it, and `list_folder` lists a folder's pictures (`pictures`), with their pixels, dpi and size (`details`), and searches by name (`search`).

## 0.6.0 — 4 October 2026

- **Overprint.** Edit Color has an Overprint box: a colour ticked prints over the colours under it instead of knocking them out — text, backgrounds, frames, lines and tables wearing it — so black text leaves no white halo when the plates shift, and a die-line's or a varnish's ink cuts no white line into the artwork. A new document's Black is ticked. At a shade under 95 % a colour knocks out all the same (QuarkXPress's Overprint Limit), and White never overprints: its box is greyed. Blends, shadows and pictures never overprint; a placed PDF keeps its own overprints. A document made with an earlier version keeps its Black knocking out until its box is ticked. The PDF prints it, and the screen shows an overprint multiplied with what is under it: yellow over cyan shows green.
- **The separation preview.** The Colors palette's Separations button opens the document's plates — Cyan, Magenta, Yellow, Black and each spot ink — and shows one at a time, in grey as a film, as the PDF prints it, while the page goes on being edited: overprints and knock-outs, shades, opacity, blends, text and pictures, a CMYK photo with its own numbers and an RGB one as the export separates it. Its × gives the page back with every ink.
- **Placed PDF and EPS files in the separation preview** show their real plates, read by Ghostscript as the printer's software reads them — a logo in pure black only on Black, their own overprints, and their spot inks, listed as plates even when the colour list has no such colour. On a computer without Ghostscript they are estimated from their screen colours, and the palette says so.
- **The manual** says how overprint is set and how the plates are seen (section 6b).
- **The AI** sets a colour's overprint (`define_color` `overprint`, the built-in colours' too), `describe` reads it back, and its guide says when to use it.

## 0.5.0 — 3 October 2026

- **Tables.** A new Table tool: drag the table's size, and Table Properties asks how many rows and columns. The cells take text — a click puts the insertion point in one, Tab and Shift+Tab go from cell to cell, Tab in the last cell adds a row — and a row grows with its text. The Table tab, shown while a table is held, and the right button's Table submenu put rows and columns in and take them out; the line between two rows or two columns is dragged to size them. A table moves, resizes and turns as a box, and prints as it shows; Ctrl while resizing scales its text, insets and lines with it.
- **Choosing cells.** A drag across cells, or Shift+click, chooses them; a click just outside a table's left or right edge chooses a row, above or below it a column, a drag along the edge several. Combine Cells makes them one and Split Cell parts them again. The Character, Paragraph and Tabs tabs and the style sheets set the text of every chosen cell at once. Ctrl+C, Ctrl+X and Ctrl+V copy, cut and paste cells, also to and from a spreadsheet.
- **The look of a table.** Its lines are set all together, by kind (between rows, between columns, the border) or one by one, with a width, pattern, colour, shade and opacity. Cells take a fill, a text inset, a vertical alignment and alignment on the decimal comma, which lines a column's prices up; every other row can be filled.
- **Pictures in cells.** A picture dropped on a cell, or imported with a cell in hand, goes into it, fitted whole; the right button's Fill Box with Picture makes it cover the cell. The PDF prints it.
- **Tables in text.** Insert Table puts a table at the insertion point, flowing with the text. A long one breaks between rows into the next column or the next box of the chain, on another page if need be; its header rows repeat over each part and its footer rows under each part but the last, and the parts after the first can have their own version of the header ("Listino (segue)").
- **Text, tables and spreadsheets.** Convert Text to Table turns selected text into a table in its place, guessing what separates the columns; Convert Table to Text goes back. Cells copied from Excel, LibreOffice or Google Sheets and pasted on the page make a table.
- **Style sheets and tables.** Changing a style sheet refits at once the tables whose text wears it, in the same Undo.
- **The property bar** shows only the tabs with something usable in them, each in its usual place. Its fields no longer stand live over nothing before the first selection.
- **A right-click in text being typed** keeps the text and its selection, so the menu acts on it.
- **The manual** has a section on tables (5b).
- **The AI** can do all of it (`place_table`, `insert_table`, `set_table`, `convert_text_to_table`, `convert_table_to_text`, and the text and pictures of cells), `describe` reads it back, and `check` looks in the cells of tables for stand-in fonts, missing characters and coarse pictures. Its guide may now run longer, so as to be complete and clear.

## 0.3.3 — 1 October 2026

- **A group turns as one.** Turned by its corner, or given an angle in the property bar, a group turns as one piece: its frame and its handles turn with it, the angle shown is the group's own, and a side handle of a turned group stretches it along its own direction. A group made before keeps its items where they are.
- **Runaround on a group.** Set with a group selected, the runaround is the group's: the text goes round the whole group, as round one box, and no longer between its items (between a picture and its caption, say). A group given none still lets each of its items push the text by its own setting, so documents already laid out do not move. The Runaround tab shows the group's setting; on an item inside such a group it shows the group's, greyed, and says to select the group.
- **A double-click on a word** selects the word in every box of a linked chain. In the boxes after the first it opened the window to import a file.
- **The box's handles with the Content tool.** They resize the box, and the pointer over them now says so. On a picture box they now win over the picture lying under them; only the picture's own round handles win over them, as in XPress.
- **An item inside a hidden group** no longer pushes text away on screen; it never did in the PDF.
- **The AI** can turn, move and resize a group with `set_geometry`; `set_runaround` on a group is the group's, as in the editor; `set_appearance` on a group colours its items; and it is told that a new item's runaround is `stop`.

## 0.3.2 — 30 September 2026

- **PDF, Illustrator and EPS pictures on Windows.** 0.3.0 and 0.3.1 refused every one of them on Windows, saying the file was not a picture the server could read. They go in now, by a page and a box, and into the exported PDF as vector, as the manual says.
- **Icons on a see-through ground.** A grey picture with a transparent ground, such as an icon, showed in the editor as a black block; the exported PDF was right. It shows as it is again.

An automatic update does not install Ghostscript, which EPS pictures need: run the installer by hand, or install Ghostscript from ghostscript.com.

## 0.3.1 — 30 September 2026

- **A placed PDF's missing fonts.** A PDF can be saved with only the names of its fonts. Where TelaioJS has the very same font (the same name, the letters the same widths), it now goes into the PDF you export by itself.
- **Missing Fonts.** The fonts TelaioJS lacks are asked for when the PDF is imported, in a window that lists them and holds the Fonts pane of Preferences: upload them there, and each one that is the same font goes into the PDF and shows on the page. Or set a font in one TelaioJS has; the window warns that the letters keep the PDF's places and take the other font's shapes, so they will probably not fit their spaces. A font added later is used by every PDF already placed, at once.
- **A font left missing** shows on screen in a similar built-in font (it used to show as nothing), and in the exported PDF is the printer's to set: Export says so, and PDF/X-4 is refused.
- **The AI** is told which fonts a PDF lacks, can set one in a font TelaioJS has (`pdfFonts`), and `check` reports a placed PDF whose fonts are missing.

## 0.3.0 — 30 September 2026

- **PDF and Illustrator files as pictures.** Import asks which page, and which box it is cut to — CropBox (the page as Acrobat shows it, chosen to begin with), TrimBox, BleedBox or MediaBox — beside the page drawn. In the exported PDF the page goes in as vector: its text stays text, its CMYK and spot colours keep their numbers, its fonts go with it. A PDF under a password is refused; one that names fonts it does not carry is exported with a warning, and not as PDF/X-4.
- **EPS pictures**, converted to PDF by Ghostscript when they are imported, and PDFs from then on. Ghostscript is free software by Artifex and not part of TelaioJS: the installer offers to install it (a box, ticked, on the computer that runs TelaioJS), downloading Artifex's own installer from its site (about 65 MB; Windows asks for an administrator). An automatic update does not install it: on a TelaioJS already installed, run the installer by hand to be offered it, or install Ghostscript from ghostscript.com. Without it an EPS is refused, saying so.
- **TIFF from the editor:** a TIFF chosen or dropped on the page now goes in (it did nothing before), at the size it declares; a CMYK TIFF keeps its numbers.
- **Full Resolution Preview** shows a picture as it will print, as the page does.
- **A picture placed from another computer of the shop** while it was still being sent now appears when it arrives; it could stay missing until the page was reloaded.
- **The AI** can upload PDF, Illustrator and EPS files, and place a PDF's page in a box (`pdfPage`, `pdfBox`).

## 0.2.2 — 30 September 2026

- **Colours as the press prints them (FOGRA39, offset on coated paper).** A colour picked on screen becomes the ink recipe the FOGRA39 profile prints it with, with black only where the colour is nearly black itself (a violet picked as #6A1B9A is now C78 M98 Y0 K0, where it used to be C31 M82 Y0 K40). Every ink is shown on screen as that press prints it: the page, the colour list and the swatches. The numbers of colours already in a document do not change, so a colour picked before may now look duller or darker on screen: that is how it prints.
- **The colour picker is XPress':** its square shows the screen's colours, with the ones the press cannot print hatched; a Screen and a Print swatch side by side show the colour picked and how it prints; and it opens again on the point a colour was picked at. A drag past its edge no longer closes it.
- **PDF/X-4 for the printer:** a box in Export PDF. The file declares FOGRA39 as its printing condition and carries its profile, with everything PDF/X-4 asks for. A file that could not carry everything the document shows (a picture missing, a typeface unreadable) is not made, and the window says what is missing.
- **Pictures:** an RGB picture is now converted to CMYK through FOGRA39 in the PDF (Export PDF's "Convert RGB pictures to CMYK", ticked to begin with; unticked, the printer's software converts it). A CMYK picture keeps its numbers exactly: a colour mixed as C10 M40 Y20 K10 in Photoshop prints as a box of that ink does (a CMYK TIFF used to be re-separated). On screen every picture is shown as it will print.
- **The AI** can give a colour as a screen colour (`hex`) and the program separates it as the picker does; `export_pdf` takes `standard: "PDF/X-4"` and `rgbPictures`.

## 0.2.1 — 29 September 2026

- **The logo:** TelaioJS has its own: the T of the name is the key that locks the printer's chase. It is the icon of the installer, the program, its shortcuts and its tray, and of the editor's browser tab.
- **Word spacing:** a word is now given exactly the room it is printed in. Words with kerned letters ("Te", "Ty", "AV", "11"…) and words set with ligatures ("fi", "ffi") were drawn narrower than the room they were given, and a wider space was left after them, on screen and in the PDF alike. Text in documents already laid out may tighten a little, and a line can take one more word.
- **Tracked text** is set without ligatures, on screen and in the PDF alike, as XPress breaks them when letters are spaced.
- **The AI:** when it makes or changes a style sheet, the answer gives the tab stops in mm, as it gives every other length.

## 0.2.0 — 29 September 2026

- **Facing pages:** the text of a left-hand page runs round the items of the right-hand page that reach over the fold onto it, on screen and in the PDF.
- **An item can change page:** dragged wholly onto another page, or moved there by its X and Y, an item becomes that page's, on top of it. One Undo puts it back.
- **The page number** in the property bar is the first page in the window (on a spread, the left one), or the page of the item selected. The page strip scrolls to keep that page in sight.
- **Home** shows only the sections that can be used for what is selected, never a grey one. With nothing selected it shows the page: navigation, masters, margins and size.
- **Trim box:** a rectangle can be the finished size of a piece on a press sheet, with crop marks round it. Step and Repeat lays the pieces butted for one cut or apart for a double cut.
- **Picture tab:** the picture's fields have a tab of their own in the property bar.
- **Keep with Next and Keep Lines Together** can be set on a paragraph in the Paragraph tab, not only in a style sheet.
- **Space Before is no longer added at the top of a column**, where there is no paragraph above to part from. Text in documents already laid out may move up.
- **The AI:** a window on another document, or on none, can open the document the AI is working on; numbers the AI sends as text are read as numbers; a picture box is placed with its runaround.
- **A licence key:** the program says whom to write to: fr4nz82@gmail.com.

## 0.1.1 — 27 September 2026

The first release, for Windows 10 and 11 (64-bit).
