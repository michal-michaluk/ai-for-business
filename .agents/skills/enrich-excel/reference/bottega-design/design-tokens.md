# Bottega AI-SDLC — Design Tokens Reference

Extracted from `https://bottega.com.pl/ai-sdlc`.

## Color Palette

| Token | Hex | Usage |
|-------|-----|-------|
| primary-dark | `#151C29` | body background, dark sections |
| primary-navy | `#293250` | cards, secondary backgrounds |
| accent-orange | `#FF5D24` | CTAs, highlights, links hover |
| text-muted | `#8292A4` | body text, secondary text |
| text-white | `#FEFEFE` | headings on dark, primary text |
| near-black | `#0A0A0A` | footer text, strong text |
| border-divider | `#343D5A` | borders, dividers |
| light-bg | `#EAEEF6` | light sections |
| hover-navy | `#242D4B` | hover, alternating rows |

## Typography

| Family | Usage | Weights |
|--------|-------|---------|
| **Work Sans** | Headings, display | 300, 400, 500, 600, 700 |
| **Open Sans** | Body text | 300, 400, 600, 700 |

## Excel Style Rules

| Element | Fill | Text | Font |
|---------|------|------|------|
| Top header | `#293250` | `#FEFEFE` (white) | Work Sans 18pt bold |
| Section headers | `#293250` | `#FEFEFE` (white) | Work Sans 14pt bold |
| Sub-headers | `#151C29` | `#FF5D24` (orange) | Work Sans 12pt bold |
| Body text | `#151C29` | `#0A0A0A` (near-black) | Open Sans 11pt |
| Bold / emphasis | `#151C29` | `#FF5D24` (orange) | Open Sans 11pt bold |
| Table headers | `#293250` | `#FEFEFE` (white) | Work Sans 11pt bold |
| Alternating rows | `#242D4B` | `#0A0A0A` | Open Sans 11pt |
| Totals | `#293250` | `#FF5D24` (orange) | Work Sans 12pt bold |
| Borders | `#343D5A` thin | — | — |

## Assets

- **Logo:** `assets/images/bottega_logo.png`
- **Fonts:** `assets/fonts/OpenSans-*.ttf` (Regular, Bold, Semibold, Light, Italic variants)
- **Fonts:** `assets/fonts/WorkSans-*.ttf` (Regular, Bold, Semibold, Medium, Light variants)

## Usage

Import into your styling script:

```python
PRIMARY_DARK    = '151C29'
PRIMARY_NAVY    = '293250'
ACCENT_ORANGE   = 'FF5D24'
TEXT_MUTED      = '8292A4'
TEXT_WHITE      = 'FEFEFE'
NEAR_BLACK      = '0A0A0A'
BORDER_DIVIDER  = '343D5A'
LIGHT_BG        = 'EAEEF6'
HOVER_NAVY      = '242D4B'
```
