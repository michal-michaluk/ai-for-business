# 01 — Analyze Excel structure

Open the Excel file with openpyxl and describe its structure.

## Input

- Path to the `.xlsx` file

## Process

1. Load workbook, list all sheet names
2. For each sheet:
   - Column headers (row ~4)
   - Number of data rows
   - Identify totals / subtotals rows
   - Identify codes (e.g. `TOTAL.01`, `IK.1`, `REF.1`)
   - Note any existing formulas
3. Present findings to the user

## Output

`structure.md` — a structured description of the Excel anatomy.

## Example (from real session)

```md
# Kosztorys.xlsx — Structure

## Sheets (5)
| Sheet | Rows | Columns | Description |
|-------|------|---------|-------------|
| Podsumowanie | 60+ | A-G (was A-F) | Summary with TOTAL.x rows and grand total |
| Central Banking | 948 | A-I (was A-H) | IK, EK, TL items for banking BU |
| Capital Markets | 284 | A-I | Same categories for CM BU |
| Refactor Capital Markets | 817 | A-I | REF items for CM refactoring |
| Narzędzia | 89 | A-I | Tools & licenses |

## Key patterns
- TOTAL rows: 01-06, each with subtotal at row +6
- Codes in column A: IK.1–IK.7, EK.1, TL.1–TL.32, REF.1–REF.6
- Column E = net value (PLN), column D = man-days
- Grand total: row 56, column E
```

## User approval required

- Confirm mapping between sheets and business domains
- Approve or adjust the list of items to enrich
