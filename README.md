# The Blueprint Diagram Design System

*Design system · element sheet · v6 · 3 September 2026*

Five color tokens and a set of diagram roles, translated from a Pinterest moodboard of close-up textures — quartz, marble, fabric, sand, cloud, almost entirely warm neutrals aside from one charcoal-navy accent — into working values for field, guide layer, structure, cluster, focal point, and type.

This repo is the reusable, code-side version of the system: a static reference sheet (`index.html`), CSS custom properties (`tokens.css`), and the same values as plain JSON (`tokens.json`), so the palette, type scale, and spacing scale can be pulled into other projects without re-deriving them from the artifact each time.

## Live page

- [View the design system](https://arlandex.github.io/design-system/)

## Swatches (light to dark)

| Name | Hex |
|---|---|
| Milk Frost | `#F0EFEC` |
| Soft Ivory | `#EAE1D7` |
| Pale Sand | `#D8C9B6` |
| Fog Stone | `#6C6D6C` |
| Ink | `#0D1015` |

Supporting reading tone: body-copy ink (`#48494B`) is calibrated for long-paragraph contrast. It is documented separately because it is an accessibility token, not a sixth base swatch.

## Accents

Ink, off the node. Same rule wherever it lands: boldest thing in view, used sparingly, never as a background.

| Use | Treatment |
|---|---|
| Node | Solid Ink fill |
| Emphasis | Bold word weight, in Ink, inside body copy |
| Tag | Ink background pill, light text |
| Underline | Ink underline under a keyword |
| Icon stroke | Ink outline stroke |

## Typography

Work Sans (headings/body) paired with IBM Plex Mono (eyebrows/measurement labels).

| Role | Spec |
|---|---|
| Eyebrow | IBM Plex Mono 500, 11.5px, tracked +0.14em, Fog Stone |
| H1 | Work Sans 700, clamp 24–30px, Ink |
| H2 | Work Sans 600, 18.5px, Fog Stone |
| Body | Work Sans 400, 15.5px / 1.5 line-height, body ink (derived, `#48494B`), max 58ch measure |

## Spacing scale

Seven steps, each roughly one and a half times the last. Everything on the sheet snaps to one of these — nothing sits in between.

| Step | Value | Used for |
|---|---|---|
| Tight | 8px | Icon/label gaps, swatch-pill spacing, tag internals |
| Compact | 16px | Grid gaps, swatch/accent cell padding, spec-row gaps |
| Standard | 24px | Element-row padding, section notes, accent-cell padding |
| Comfortable | 32px | Page side margin, padding-scale strip padding |
| Rhythm | 48px | Type-card internal padding |
| Section | 64px | Space between major sections, page top padding |
| Page | 96px | Page bottom padding, page close |

## Diagram roles

The six roles every diagram illustration in this system draws from, numbered lightest to boldest:

1. **Field** — Milk Frost, Soft Ivory. The two lightest swatches, as the gradient ground — restrained enough that nothing competes with what's on top of it.
2. **Guide layer** — Pale Sand. Bounds arrows, axis, diagonal ticks. Light enough to recede, warm enough that it never reads as generic UI grey.
3. **Structure** — Fog Stone. Connector line, hub stroke, and measurement text all share this tone — doing triple duty as "this is deliberate, but it's not the point."
4. **Cluster satellites** — Pale Sand, Fog Stone (outline). Mixed solid-and-outline dots, the two mid tones only. No Ink here on purpose — it stays reserved for one job.
5. **Focal point** — Ink. The one swatch that appears nowhere else. Darkest, coldest, and the only element allowed that distinction — everything else stays lighter than this, always.
6. **Type, in diagram** — Fog Stone (measurements, data) / Ink (diagram labels).

## Provenance

Palette drawn from an "iPhone backgrounds" Pinterest moodboard (warm-neutral field/guide/cluster tones, a corrected cooler mid-tone called Fog Stone for structure). As of v4, Ink (`#0D1015`, cool near-black) replaced the original warm "Urban Espresso" as the focal-point accent — a deliberate shift from warm to cooler system character.

Design reference for the blog this system serves: Taplio's blog.

## Files

- `index.html` — standalone reference sheet, viewable directly or via GitHub Pages
- `tokens.css` — CSS custom properties (colors, type, spacing)
- `tokens.json` — the same tokens as plain JSON, for non-CSS tooling
