# [OPTIONAL] Create design tokens from a live website

Use this step when you want to extract the visual design language from an existing website and turn it into reusable design tokens.

## When to use

- The client has an existing brand / website with a distinct visual identity
- You want the Excel styling to match the client's brand
- You have access to the website URL

## When to skip

- You already have design tokens (from a brand guide, design system, or previous project)
- The project doesn't need branded styling
- You want to use a pre-existing design reference (e.g. `reference/bottega-design/`)

## Process

### 1. Visit the website and capture visual assets

```sh
# Full-page screenshot
playwright screenshot --full-page https://example.com page.png

# Download CSS
curl -o style.css https://example.com/assets/css/style.css
```

### 2. Extract design tokens

Read the CSS / inspect the page to extract:

- **Colors** — primary, secondary, accent, text, background, borders
- **Fonts** — families, weights, sizes
- **Spacing** — padding, margins, grid
- **Border radius** — if distinctive
- **Images** — logo, icons, client logos (for potential embedding)

### 3. Save as structured JSON

```json
{
  "source_url": "https://example.com",
  "tokens": {
    "colors": [
      { "name": "primary-dark", "hex": "#151c29", "usage": "body background" },
      { "name": "accent-orange", "hex": "#ff5d24", "usage": "CTAs, highlights" }
    ],
    "font_families": ["\"Open Sans\", sans-serif", "\"Work Sans\", sans-serif"],
    "font_sizes": ["16px", "20px", "24px", "36px"]
  },
  "assets": [
    { "url": "https://example.com/logo.png", "local": "assets/images/logo.png" }
  ]
}
```

### 4. Provide as input to step 05

The design tokens JSON feeds directly into the styling script.

## Example

The [bottega-design/](bottega-design/) directory contains a complete reference extracted from `bottega.com.pl/ai-sdlc`, including:
- Full design tokens in JSON
- Documentation in Markdown
- All assets (logo, fonts, icons)
- A styled Excel template
