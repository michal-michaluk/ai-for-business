# 06 — Finalize

Deliver the final enriched Excel and commit the work.

## Input

- `styled.xlsx` from step 05
- All intermediate artifacts (brief, content, scripts)

## Process

1. Verify:
   - All sheets are present and correctly named
   - Formulas calculate correctly (no circular references, no `#REF!`)
   - Logo renders correctly
   - Row heights are appropriate
   - Print layout / page setup if needed

2. Clean up temporary files (backups, intermediate copies)

3. Commit to git:
   ```sh
   git add <final-file> <scripts> <artifacts>
   git commit -m "enrich <name>: add narrative content and styling"
   ```

## Output

- Final `.xlsx` — ready for delivery to client/board
- Git commit with descriptive message
- Summary of what was done (for handover)

## Summary template

```md
# Enrichment summary

## What was done
- Added "Offer Overview" sheet with: Executive Summary, Approach,
  Scope, Business Outcomes, Delivery Model, Risks, Why Botega
- Added "Opis oferty" column (G) to Podsumowanie
- Added "Value proposition" column (I) to all detail sheets

## Design applied
- Color palette: navy #293250, orange #FF5D24, dark #151C29
- Fonts: Work Sans (headings), Open Sans (body)
- Logo embedded in Offer Overview

## Files
- Final: Kosztorys.xlsx
- Script: enrich_kosztorys.py
- Preview: offer_overview.png
```
