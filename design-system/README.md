# Jackie Diaz Portfolio — Design System

## Quick start

Add to every `<head>`, before your page styles:

```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Manrope:wght@400;500;600;700;800&display=swap">
<link rel="stylesheet" href="[path]/design-system/tokens.css">
<link rel="stylesheet" href="[path]/design-system/components/bundle.css">
```

Adjust `[path]` to the root: `design-system/` (root), `../design-system/` (depth 1), etc.

---

## Tokens (`tokens.css`)

All colours, radii, and the font stack live here as CSS custom properties. **Never write literal hex values in page CSS** — always reference a token.

### Surfaces
| Token | Role |
|---|---|
| `--bg` | Page ground |
| `--panel` | Elevated panel, input fills |
| `--card` | Card surface (explicit white) |
| `--forest` | **One** deep surface per screen |
| `--lavender` | Soft lavender fill |
| `--lilac` | Softer lilac fill |

### Brand
| Token | Role |
|---|---|
| `--lime` | **Single** primary action per page |
| `--violet` | Detail: links, spinning star, active nav, focus ring, arrows |

### Text
| Token | Use on |
|---|---|
| `--ink` | Primary text everywhere |
| `--ink-soft` | Secondary text on `--card` |
| `--muted` | Secondary text on `--bg` and `--panel` only |
| `--on-forest` | Text/icons on `--forest` |
| `--on-lime` | Text on `--lime` |
| `--on-lavender` | Text on `--lavender` |
| `--on-lilac` | Text on `--lilac` |

### Structure
- `--line` — subtle dividers
- `--line-strong` — stronger dividers, button borders

### Shape
- `--radius-card: 8px` — cards
- `--radius-tag: 4px` — tags, pills
- `--radius-btn: 4px` — buttons
- `--radius-input: 4px` — form fields

---

## Bundle (`components/bundle.css`)

Provides: reset, `.wrap`, base `section` padding, `header` / `.nav` / `.mark` / `.navlinks` (active underline = `--violet`, star = `--violet`), reveal animations, `.btn-lime`, `.btn-ghost`, `.tag`, `.ds-ph` / `.ph`, `.ds-ph-inline` / `.ph-inline`, `.forest-band`, `.back-row`, `.crumbs`, `.close-row`, `.close-link`, `.top-link`, `.section-title`, `.section-intro`, `.eyebrow`.

---

## Colour roles

- **`forest`** — one dramatic dark surface per screen (e.g. the contact footer on the home page). Use it once.
- **`lime`** — the single primary CTA per page (`btn-lime`). Do not use it more than once per view.
- **`violet`** — detail colour: links, spinning `✳`, active nav underline, focus rings, accent arrows. Keep it small.
- **`muted`** — secondary/supporting text, but only on `--bg` and `--panel` backgrounds.
- **`ink-soft`** — secondary text on `--card` (explicit white/dark card surfaces).

---

## Components

Each component in `components/<Name>/` has:
- `README.md` — rules and usage notes
- `preview.html` — copy-ready markup

Available: `Nav/`, `Button/`, `Tag/`, `Placeholder/`, `Card/`.

---

## Dark mode

Tokens automatically redefine themselves under `@media (prefers-color-scheme: dark)` and `:root[data-theme="dark"]`. Never set a colour outside the tokens.
