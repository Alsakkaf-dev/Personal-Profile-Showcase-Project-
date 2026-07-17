# Personal Profile Showcase

A responsive, semantic, single-page professional profile built with hand-written
HTML5 and CSS. No UI frameworks, no build step, no dependencies — open
`index.html` in a browser and it runs.

## Goals

This project exists to exercise the fundamentals that frameworks usually hide:

- **Semantic HTML5** — a correct document outline built from real landmarks
  (`header`, `nav`, `main`, `section`, `article`, `footer`) and a single `h1`.
- **The CSS box model** — spacing, borders, and sizing reasoned about
  explicitly, with `border-box` applied from the first commit.
- **Custom properties** — colour, typography, and spacing live as tokens in
  `:root`, so a media query can re-point one variable instead of rewriting
  every rule that depends on it.
- **Flexbox layout** — every arrangement on the page, including the skills
  grid, is flexbox. No CSS Grid, no float hacks.
- **Separation of concerns** — production markup at the root, assets in their
  own pipeline directory.

## Structure

```
index.html            the page itself
assets/
  css/style.css       tokens, reset, components, responsive layers
  images/             reserved for media
```

`style.css` is ordered deliberately: design tokens, reset, base, layout
utilities, components, then responsive and motion-preference layers last, so
later rules override earlier ones by source order rather than by specificity
escalation.

## Approach

The commit history is part of the artefact. Each commit touches exactly one
file and carries one logical change, so the log reads as the order the
decisions were actually made — tokens before the components that consume them,
one timeline card styled before the pattern was repeated, breakpoints only
after the base layout worked.

## Accessibility

- Every form control has an associated `<label for>`.
- Focus is always visible; where the default outline is removed it is replaced
  with a higher-contrast indicator.
- `prefers-reduced-motion` is respected.
- Dates carry machine-readable `datetime` attributes.

## Content

The profile currently uses a placeholder persona. Replace the text in
`index.html` — name, hero copy, milestones, skills, and footer — with real
details before publishing.

## Local preview

Open `index.html` directly, or serve the directory:

```bash
python -m http.server 8000
```

Then visit <http://localhost:8000>.
