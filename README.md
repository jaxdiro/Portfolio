Jackie Diaz Portfolio is the visual system for Jackie Diaz's portfolio site: the home page, Work grid, About, Resume, Contact and the case studies. It reuses the colours of the Freelance Hub (warm grey ground, deep forest, lime) and adds one new voice: violet.

## Content fundamentals

- Write in first person, plain and specific. "I bridge the gap between marketing, design, and the people they're made for." "A zero-budget content system that reached 22x its own audience."
- Titles are sentences in sentence case, ending with a full stop. Section names are short nouns: The Approach, The System, The Results.
- Lead with the number when there is one ("120.3K organic views"), then say what it is compared to.
- Name the three practice areas exactly: Strategy & Planning, Creative Direction & Production, Paid Media & Analytics. A project that used no paid media does not list the third.
- No emoji. The only decorative glyph is the star ✳.
- Links that go somewhere end in an arrow: "View case study →", "← Back to Work".

## Visual foundations

- **Ground.** Pages sit on `bg`. Content that needs lifting goes on `panel` (white) with a `line` hairline, or on `card` (quiet grey). In dark, the same tokens swap and nothing else changes.
- **Colour roles.** `forest` is the one deep surface per screen (hero or featured stat). `lime` marks the single primary action or the single highlighted number. `violet` is the detail colour: links, the spinning star, the active nav underline, connector arrows, the focus ring. `lavender` and `lilac` are the soft purples: lavender for a hover fill or one highlighted tag, lilac for the pull quote wash. Keep purple small. If lime and violet are both large in one view, drop one.
- **Text colours.** `ink` for headings and body. `ink-soft` for secondary text on `card`. `muted` for captions on `bg` and `panel` only. On `forest` use `on-forest`, `forest-muted` and lime numbers. Never put `lavender` behind `muted` text; use `on-lavender`.
- **Type.** Manrope throughout. Headings at weight 800 with tight negative tracking (`display-xl`, `display-lg`, `h2`); body at 400; labels at 700. Eyebrows are capitals at `eyebrow` size. Use tabular figures for any number in a column.
- **Shape.** Large soft corners. Cards and panels use `radius-card`, inner steps `radius-sm`, every button and tag is a pill (`radius-pill`). Arrow discs are full circles.
- **Borders and shadow.** Hairlines separate sections. Shadows are for hover lift (`shadow-lift`) and dialogs (`shadow-pop`) only.
- **Spacing.** Steps from `space-1` to `space-8`. Cards pad `space-5`. Sections breathe at `space-8`. Keep a 16px gutter on phones.
- **Motion.** The ✳ star spins once every 4 seconds, in violet, in the wordmark and at the start of every "View case study" link. Copy fades up on load. Cards lift 2px on hover. All of it stops under `prefers-reduced-motion`.
- **States.** Hover on a project card fills it `lavender` and switches its text to `on-lavender`. Focus is a 2px solid `violet` ring with 3px offset; on `forest` it is `lime`. Status is always a pill with a word: Active (`ok`), Waiting (`warn`), Overdue (`bad`).
- **Placeholders.** Missing photos, video and metrics are dashed boxes on `track` with a small label ("photo", "reel", "metric pending"). Never fill them with stock imagery.
- **Layout.** Content max width 1180px. Work grid is three columns, one on phones. Case studies run as a single column of sections with hairlines between them.

## Iconography

No icon set. The star ✳ and the arrows → ← ↗ are text glyphs in the font. Arrow discs are a `chip` circle with a lime arrow, or an `on-lime` circle on a lime button.

## Components

Header, Button, Tag, ProjectCard, StatTile, FlowStep and Quote each have a live preview and a guideline. Their styles live in `components/bundle.css` and read every value from the tokens.
