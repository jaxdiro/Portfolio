# Portfolio design system

This site uses the design system in `design-system/`. Read `design-system/README.md` first: it has the voice, colour roles, type, shape, motion and states.

- Link `design-system/tokens.css` (and `design-system/components/bundle.css` for the component classes) from every page, plus the Manrope font link noted at the top of `tokens.css`.
- Use the tokens (`var(--bg)`, `var(--violet)`, `var(--radius-card)` ...) for every colour, size and radius. Do not write literal hex values in page CSS.
- Colour roles: `forest` is the one deep surface per screen, `lime` is the single primary action, `violet` is the detail colour (links, spinning star, active nav underline, focus ring, arrows). Keep purple small.
- Text: `ink`, `ink-soft` on `card`, `muted` only on `bg` and `panel`; `on-forest`, `on-lavender`, `on-lilac` on those fills.
- Each component in `design-system/components/<Name>/` has a `README.md` (rules) and a `preview.html` (markup to copy). Match their class names and markup.
- Keep the dashed placeholder boxes (`.ds-ph`) for missing photos, reels and metrics.
- Support light and dark: never set a colour outside the tokens.
