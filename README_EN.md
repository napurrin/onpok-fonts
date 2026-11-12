# OnPok Fonts

**Fonts that match the widths of the characters listed in a width table to common Korean office fonts, so that line breaks come out the same in the same document.**

Most Korean office documents (HWP/HWPX) use Hancom or Microsoft fonts, which cannot be redistributed. Viewers without those fonts substitute other fonts, so character widths differ and lines break in different places.

OnPok fonts are based on free fonts (Noto, Baekmuk). For every character in the width table, the advance width is set to the width of the original font.
- The glyph shapes follow the base fonts, so they look different from the originals.
- Weights were chosen so that stroke density is close to PDFs saved by Hancom Office. Because the shapes differ, the weight is not identical.

The table in `README.md` lists which OnPok font has its widths matched to which original font.
- Font names in that table (Malgun Gothic, Human-, Hanyang-, HY-, HCR- …) are trademarks of their owners.
- OnPok is not affiliated with them. The names are used only to describe width compatibility.

**Width coverage**
- Width numbers are taken from the width tables of rhwp (MIT, Copyright (c) 2025-2026 Edward Kim). No glyph shapes are taken from rhwp.
- About 11,500 characters per font are in the width table (all 11,172 Hangul syllables, Latin, digits, punctuation, some Hanja and symbols). For every one of them that the font contains, the advance width equals the table width; the number of mismatches is 0 in every font (`CHECK_GLYPHS.md`).
- Characters outside the table keep the base font's width.
- A few rare characters in the table are not in the fonts yet, because neither the base fonts nor Noto have them (2 in the Baekmuk-based fonts, 33 rare punctuation and invisible characters in Mango Batang and Coco Dotum). They are drawn with another font.

**What was checked**
- Whether the table widths match Hancom's actual layout was compared on only 10 lines from public press releases (one line for each of 10 fonts). Line breaks and page breaks of whole documents were not checked.
- On those lines, the Hangul advances matched for 9 fonts; for OnPok Mango Batang only 14 of 21 pairs (67%) matched. See `samples/README.md`.
- Fonts without a comparison image (no Hangul-heavy line set only in that font was found): Sae Myeongjo 1·2, Jung Gothic 1·2, Kyun Myeongjo 1·2, Kyun Gothic 1·2, Gulim Che, Dotum, and the Bold styles of Ttogothic, Mango Batang and Coco Dotum. For these, only the match with the width table was checked.

**Added characters:** characters common in Korean public documents (dashes, quotes, document symbols, circled and parenthesized numbers, units, corner brackets, Hangul jamo, KS X 1001 Hanja, currency signs, middle dots, and the 59 bullet symbols that rhwp 0.9.0 uses when it redraws Hangul bullets) are present in every OnPok font. Missing ones were taken from Noto (Sans/Serif KR, Sans CJK KR, Sans Symbols, Sans Symbols 2, Sans Math). See `CHECK_GLYPHS.md`.

**Made by** napurrin · [github.com/napurrin](https://github.com/napurrin) — public-document tools built while working, and learning, in emergency medical services.

The build tools (renaming, glyph filling, checks) are not public. This repository contains the fonts, documentation and check results.

**License**
- All OnPok fonts: SIL Open Font License 1.1.
- Fonts based on Baekmuk (Gulim, Dotum, Batang families) also contain glyphs taken from Noto (dashes, circled and parenthesized numbers 16-20, currency signs, accented Latin letters and others), so they are distributed under OFL 1.1 as a whole while also following the Baekmuk license. Keep the copyright and permission notices, and include this acknowledgement: "Baekmuk Batang, Baekmuk Dotum, Baekmuk Gulim, and Baekmuk Headline are registered trademarks owned by Kim Jeong-Hwan."
- Some symbols come from Noto Sans Symbols, Noto Sans Symbols 2 and Noto Sans Math, and one Hanja (隙) from Noto Sans CJK KR — all OFL 1.1.
- Width numbers: rhwp width tables (MIT, Copyright (c) 2025-2026 Edward Kim) — `LICENSES/rhwp-MIT.txt`. No glyph shapes are taken from rhwp.
- See `LICENSES/` for details.

Modifications Copyright 2026 The OnPok Project Authors.
