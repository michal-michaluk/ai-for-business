# 05 — Apply visual styling

Apply design tokens, fonts, logo, and visual polish to the enriched Excel.

## Input

- `enriched.xlsx` from step 04
- Design tokens (from [create-design-tokens.md](../reference/create-design-tokens.md) or [reference/bottega-design/](../reference/bottega-design/))
- Logo image (optional)

## Process

1. Define design tokens as Python constants:
   ```python
   PRIMARY_DARK    = '151C29'
   PRIMARY_NAVY    = '293250'
   ACCENT_ORANGE   = 'FF5D24'
   TEXT_MUTED      = '8292A4'
   TEXT_WHITE      = 'FEFEFE'
   NEAR_BLACK      = '0A0A0A'
   BORDER_DIVIDER  = '343D5A'
   LIGHT_BG        = 'EAEEF6'
   ```

2. Apply styling rules:
   - **Top header** (row 1): navy background (`PRIMARY_NAVY`), white text, larger Work Sans
   - **Section headers**: navy background, white bold text in Work Sans
   - **Sub-headers**: accent orange text on dark background
   - **Body text**: Open Sans, muted color (`TEXT_MUTED`) — **never use orange for body text**
   - **Bold text**: accent orange color (only for emphasis, codes, highlights)
   - **Table headers**: navy fill, white Work Sans
   - **Alternating rows**: base dark + hover navy for visual separation
   - **Borders**: subtle thin borders (`BORDER_DIVIDER`)
   - **Total rows**: navy background, orange bold font, PLN format

3. Logo placement:
   - Anchor logo to top-left cell of Offer Overview
   - Cap width at ~190px, maintain aspect ratio

4. Row height adjustments:
   - Calculate height based on text length and column width
   - Minimum 20pt, maximum 400pt per cell

## Important rules (from hard-won experience)

- **Body text is `#0a0a0a` (near-black)**, not orange
- **Only codes, headers, and bold highlights use orange**
- **Top header is navy**; section sub-headers use orange
- **Merge cells** where text needs space (e.g. "Dlaczego Bottega")
- **Adjust row heights** for headers in tool-heavy sheets (e.g. Narzędzia)

## Output

- `styled.xlsx` — fully styled Excel
- `preview.png` — screenshot of Offer Overview sheet for visual approval

## User approval required

- Visual review via screenshot
- May request tweaks: "bold → orange", "header navy → section orange", etc.

## Iteration loop

This step typically requires 3-5 refinement cycles:
1. Initial apply → user sees screenshot
2. Tweak colors/alignment → new screenshot
3. Adjust merged cells, row heights → final screenshot

## Reusable script

Copy the pattern from `enrich_kosztorys.py` — extract the styling functions into a reusable module:

```python
# styler.py
def set_cell(ws, row, col, value, font, fill, alignment, border): ...
def section_header(ws, row, text): ...
def body_cell(ws, row, col, text, col_width, highlight, bold): ...
def auto_height(text, col_width_chars, font_size=11): ...
def add_logo(ws, row, col, logo_path): ...
```
