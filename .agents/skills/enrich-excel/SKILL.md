---
name: enrich-excel
description: new skill
---

# enrich-excel

Transform a raw Excel spreadsheet (cost estimate, proposal, etc.) into a polished, boardroom-ready document by adding narrative descriptions, value propositions, executive summary, and a consistent visual design language.

## Pipeline overview

```
[Excel] ──► 01-analyze ──► 02-brief ──► 03-content ──► 04-apply ──► 05-style ──► 06-finalize ──► [Output]
               │              │             │              │             │
               ▼              ▼             ▼              ▼             ▼
         structure.md     brief.md     content.md     enriched.xlsx  styled.xlsx
                                                          + screenshot
```

Each step produces a **reviewable artifact** — the user approves before the next step begins.

## Steps

| Step | What happens | Artifact |
|------|-------------|----------|
| [01-analyze-excel](steps/01-analyze-excel.md) | Read Excel structure, list sheets, columns, totals | `structure.md` |
| [02-create-brief](steps/02-create-brief.md) | From source (PDF/website/client email), define scope | `brief.md` |
| [03-generate-content](steps/03-generate-content.md) | Write narrative descriptions, executive summary, VP | `content.md` |
| [04-apply-content](steps/04-apply-content.md) | Insert content into Excel via openpyxl | `enriched.xlsx` |
| [05-apply-styling](steps/05-apply-styling.md) | Apply design tokens, fonts, logo, screenshot | `styled.xlsx` + `preview.png` |
| [06-finalize](steps/06-finalize.md) | Clean up, commit, deliver | final file |

## Reference

- [create-design-tokens.md](reference/create-design-tokens.md) — [OPTIONAL] extract design tokens from a live website
- [bottega-design/](reference/bottega-design/) — reference design tokens, assets, and a styled template

## Design tokens (Bottega AI-SDLC)

```
primary-dark   #151C29   body bg, dark sections
primary-navy   #293250   cards, secondary bg
accent-orange  #FF5D24   CTAs, highlights
text-muted     #8292A4   body text
text-white     #FEFEFE   headings on dark
near-black     #0A0A0A   strong text
border-divider #343D5A   borders
light-bg       #EAEEF6   light sections
```

**Fonts:** Work Sans (headings), Open Sans (body)

## Prerequisites

- Python 3.10+ with `openpyxl` installed
- Input Excel file (`.xlsx`)
- *(optional)* Source materials (PDF, website URL, client notes)
- *(optional)* Logo image, design tokens

## Example

See [reference/example-outputs/](reference/example-outputs/) for artifacts from a real enrichment run.
