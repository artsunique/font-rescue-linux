# FontRescue for Linux

Your old Mac fonts. Working again.

FontRescue converts classic Mac fonts — PostScript Type 1 printer fonts (LWFN), font suitcases and .dfont files — into OpenType or TrueType files that work in today's apps. Drop files or whole folders onto the window; the converted fonts appear in a new `Converted` folder next to your originals. Everything runs locally on your computer.

This repository only hosts the download. FontRescue is commercial software by [Arts Unique](https://store.arts-unique.com/product/fontrescue); the source code is not public.

## Download

**[fontrescue_2.0.0-1.ubuntu-noble_amd64.deb](https://github.com/artsunique/font-rescue-linux/releases)** · Ubuntu 24.04 LTS (and derivatives based on it), x86-64

SHA-256: `aba0acb6cdb3eefa94a709520712c1d6f0d1f20099e2ef297e6e85b98fb7b29b`

## Install

```bash
sudo apt install ./fontrescue_2.0.0-1.ubuntu-noble_amd64.deb
```

Then start **FontRescue** from the applications menu, or run `fontrescue` in a terminal.

To remove it: `sudo apt remove fontrescue`

## Old Mac fonts on Linux

Classic Mac fonts keep their data in a *resource fork*, which Linux file systems do not store. FontRescue can read them from:

- **ZIP archives made on a Mac** (Finder › Compress) — drop the ZIP itself, do not unpack it
- **MacBinary** files (`.bin`)
- `.dfont`, `.pfb` and `.pfa` files
- folders that still contain the `._name` companion files a Mac writes on foreign drives

A printer font that shows as a 0-byte file without such a companion has lost its data and cannot be converted.

## Trial and license

The download is the full app and converts three fonts for free. A lifetime license (€9.99, one-time) unlocks unlimited conversions on one computer:

**[Buy FontRescue](https://store.arts-unique.com/product/fontrescue)**

Enter your key under **License…** in the menu. To move the license to another computer, deactivate it there first.

## What it converts

| Input | Output |
| --- | --- |
| PostScript Type 1 printer fonts from classic Mac OS (LWFN) | OpenType (.otf) or TrueType (.ttf) |
| Font suitcases (FFIL) with TrueType | TrueType (.ttf) |
| .dfont files | TrueType (.ttf) |
| PostScript .pfb / .pfa, with optional .afm | OpenType (.otf) or TrueType (.ttf) |

- Type 1 fonts keep their original cubic outlines in .otf, unchanged.
- Kerning is read from the suitcase (FOND) or the .afm file and carried over.
- Family, style and weight are set so styles group correctly in font menus.
- Your original files are never changed.
- Every file is listed as converted or skipped, with the reason.

## Limits

- FontRescue converts fonts. It does not edit glyphs, rename families or repair damaged files.
- Type 1 hinting is not carried over.
- Bitmap-only screen fonts are listed but not converted; their outlines are in the matching printer fonts.
- Fonts that lost their resource fork while being copied cannot be recovered.
- Multiple Master fonts are not supported.

## Font licenses

FontRescue changes the file format of fonts. It does not grant you any rights to those fonts.

**Only convert fonts you are licensed to convert.** Many foundry licenses restrict modifying or converting font files. By using FontRescue you confirm that you are entitled to convert the fonts you process.

FontRescue does not include any fonts. Copyright, trademark and license information stored in the original fonts is carried over unchanged.

## Your data

Your fonts are never uploaded. When you activate the app, it sends your license key and an anonymous device ID to store.arts-unique.com to verify the purchase. There is no tracking and no analytics.

## Built on open source

fontTools (MIT), Qt 6 / PySide6 (GNU LGPL v3), Python (PSF License), truststore (MIT), Source Sans 3 (SIL Open Font License 1.1). The full license texts are in the app under **Acknowledgements**.

## Support

store@arts-unique.com · https://store.arts-unique.com

---

Mac and macOS are trademarks of Apple Inc. Windows is a trademark of Microsoft Corporation. Linux is a trademark of Linus Torvalds. PostScript is a trademark of Adobe. Font names are trademarks of their respective owners. FontRescue is an independent app by Arts Unique and is not affiliated with or endorsed by Apple, Microsoft, Adobe or any font foundry.

© 2026 Arts Unique. All rights reserved.
