# enrich-excel — Basic eval

## Prerequisites

- Python 3.10+ with `openpyxl` installed
- A test `.xlsx` file (e.g. `test-kosztorys.xlsx`)
- *(optional)* A logo image

## Test: Pipeline executes end-to-end

1. Run `01-analyze-excel` on the test file → verify `structure.md` is produced
2. Create a brief → verify `brief.md` covers the required sections
3. Generate content → verify `content.md` has all sections
4. Apply content → verify `enriched.xlsx` has new columns/sheets
5. Apply styling → verify `styled.xlsx` has colors/fonts/logo, `preview.png` exists
6. Finalize → verify final file is saved

## Test: Design tokens apply correctly

1. Load `template-styled.xlsx` from `reference/bottega-design/`
2. Verify:
   - Sheet "Offer Overview" exists
   - Top header has navy background, white text
   - Section headers have navy background
   - Sub-headers have orange text
   - Body text is near-black (`#0A0A0A`)
   - Borders are thin, color `#343D5A`
   - Logo is present in cell A1

## Test: Circular reference detection

1. Create a test Excel with cross-sheet formulas
2. Run the apply-content step
3. Verify no `#REF!` or circular reference errors in resulting formulas

## Test: Template is clean

1. Open `template-styled.xlsx`
2. Verify no client-identifiable data is present
3. Verify styling examples are visible
4. Verify only 2 sheets exist (Offer Overview, Podsumowanie)

## Known limitations

- openpyxl cannot render fonts natively in preview screenshots
- Formula references may need manual repair after column insertions
- Row auto-height is heuristic-based, not pixel-perfect
