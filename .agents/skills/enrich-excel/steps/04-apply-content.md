# 04 — Apply content to Excel

Insert the approved narrative content into the Excel file using Python + openpyxl.

## Input

- Original Excel (`.xlsx`)
- `content.md` from step 03
- `structure.md` from step 01

## Process

1. Create a Python script that:
   - Loads the workbook
   - Creates **Offer Overview** sheet (insert at position 0)
   - Adds **Opis oferty** column (G) to Podsumowanie sheet
   - Adds **Value proposition** column (I) to detail sheets
   - Writes all content from `content.md` into appropriate cells
   - Sets column widths, text wrapping, basic alignment
   - Saves as `enriched.xlsx`

2. Script structure (reusable pattern):
   ```python
   import openpyxl
   from openpyxl.utils import get_column_letter

   wb = openpyxl.load_workbook('Kosztorys.xlsx')

   # --- Offer Overview sheet ---
   ov = wb.create_sheet('Offer Overview', 0)
   # ... sections with merged cells, narrative text ...

   # --- description column in summary ---
   ws = wb['Podsumowanie']
   ws.cell(row=4, column=7, value='Opis oferty')
   # ... fill per TOTAL.x row ...

   # --- value proposition in detail sheets ---
   for sheet_name, vp_map in value_propositions.items():
       ws = wb[sheet_name]
       ws.cell(row=4, column=9, value='Value proposition')
       # ... fill per item code ...

   wb.save('Kosztorys.xlsx')
   ```

3. **Watch out for:**
   - Circular references in formulas → use explicit references (`Podsumowanie!E11`)
   - Row heights that don't fit long texts → auto-height calculation
   - Merged cells across existing ranges

## Output

- `enriched.xlsx` — Excel with narrative content applied
- `enrich.py` — the reusable enrichment script

## User approval required

- Open the file and verify content is in the right places
- Check that formulas still work correctly

## Common pitfalls

| Problem | Fix |
|---------|-----|
| Circular reference in grand total | Use `=SUM(Podsumowanie!E11,Podsumowanie!E19,...)` |
| Text clipped in cells | Auto-calculate `row_dimensions[row].height` based on text length |
| Wrong column mapping | Double-check column indices in the user's Excel |
