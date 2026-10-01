# Changelog

What each version of TelaioJS changed, newest first. Every version is on the [releases page](https://github.com/Fr4nZ82/telaiojs-releases/releases), with its installer, its manual and the notices of the other authors' software. A TelaioJS already installed takes each new version by itself: it is downloaded, checked against LNPrint's signature, and installed the next time the computer starts.

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
- **A licence key:** the program says whom to write to: LNPrint at fr4nz82@gmail.com.

## 0.1.1 — 27 September 2026

The first release, for Windows 10 and 11 (64-bit).
