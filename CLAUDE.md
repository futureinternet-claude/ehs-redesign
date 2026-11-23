# EHS redesign on UAE DS 4.0

Design sessions start in `design/` (core Figma rules there). HTML sessions start in `web/`
(not started). Shared rules and skills come from the `uae-ds4-toolkit` plugin
(`../toolkit`). History and open items: `HANDOFF.md`. Page decisions: `DECISIONS.md`.
Previous full rules file kept as `CLAUDE.old.md` (reference only).

## Goal
Redesign the Emirates Health Services (EHS) website (https://www.ehs.gov.ae/) from UAE DS
3.0 to UAE Design System 4.0 in Figma. Design phase first; HTML later.

## Figma
- Working file: https://www.figma.com/design/wAR2tIjblpYdLmfJh3JQnM/EHS-DLS-4.0
  (fileKey `wAR2tIjblpYdLmfJh3JQnM`).
- Shared 4.0 library: see the `ds4-library` skill (fileKey `1yvKuvJyvNNT9tTv8QmBI5`).
- Brand colour mode: `EHSblue` in the library's Color System collection (primary colour
  only; everything else as the default DS). Frames built before this mode existed may
  still show the default gold: change them only on copies, when asked.
- Pages: `Redesign (4.0)` 24:1143, `Local Components` 97:26387, `QA` 24:1144.
  (`Screens` 0:1, the original, was not found on 2026-11-23: ask before relying on it.)

## Identity: showcase direction (EHS only)
- The new design is a showcase of what DLS 4.0 can do: simple and creative, with the same
  type, colour and radius everywhere and the layout changing from section to section.
  Custom containers are allowed on any page under the Boxes rule.
- Limit the whole site to four container types: standard Aegov-Card, image-overlay card
  (`Pattern / Initiative image card`), gradient panel (the stacked deck panel), and the
  details card on a map (`Pattern / Facility details card`). Ask before adding a fifth.
- Rhythm: no more than two consecutive sections on a page in the same container style.
- Client-facing wording: "built on DLS 4.0 tokens and components", never "fully
  compliant" or "official components" for custom containers.

## Page templates (one representative URL per layout)
| # | Template | Representative URL (EN) | URL (AR) | Priority |
|---|---|---|---|---|
| 1 | Home | https://www.ehs.gov.ae/en/home | https://www.ehs.gov.ae/ar/home | 1 |
| 2 | Service listing | https://www.ehs.gov.ae/en/services | https://www.ehs.gov.ae/ar/services | 2 |
| 3 | Service detail (directory, has tabs: patient and others) | https://www.ehs.gov.ae/en/services/services-directory#patient | https://www.ehs.gov.ae/ar/services/services-directory#patient | 2 |
| 4 | Section landing (Digital Participation) | https://www.ehs.gov.ae/en/digital-participation | https://www.ehs.gov.ae/ar/digital-participation | 3 |
| 5 | Blog listing | https://www.ehs.gov.ae/en/digital-participation/blogs | https://www.ehs.gov.ae/ar/digital-participation/blogs | 3 |
| 6 | Blog detail | https://www.ehs.gov.ae/en/digital-participation/blogs/blog-details?id=1514 | https://www.ehs.gov.ae/ar/digital-participation/blogs/blog-details?id=1514 | 3 |
| 7 | About listing | https://www.ehs.gov.ae/en/about-us | https://www.ehs.gov.ae/ar/about-us | 3 |
| 8 | About detail (content page) | https://www.ehs.gov.ae/en/about-us/ehs-strategy/ | https://www.ehs.gov.ae/ar/about-us/ehs-strategy/ | 3 |
| 9 | Open data / policy detail | https://www.ehs.gov.ae/en/open-data/open-data-policy | https://www.ehs.gov.ae/ar/open-data/open-data-policy | 4 |
| 10 | Contact | https://www.ehs.gov.ae/en/contact-us | https://www.ehs.gov.ae/ar/contact-us | 4 |

Other About detail pages (same template as #8, only to check content variations):
- https://www.ehs.gov.ae/en/about-us/organization-structure
- https://www.ehs.gov.ae/en/about-us/health-knowledge-management-strategy

All other pages follow one of these templates. Do not design individual pages beyond
these unless asked.

## Component registry (local components; keep this table current)
| Component | Kind | Figma page | ID | Properties / variants | Used on |
|---|---|---|---|---|---|
| `sub-page-banner` | local component | Local Components | 97:26409 | Page Title, Page Subtitle, Content slot. Measured 270 high on 2026-11-23 | all sub-pages |
| `Card Pattern` | component set | Local Components | 117:6259 | Property 1 = Service / Initiative / News / Facility card; also found: Service Card V2, Variant7, Home Selection Cards (not yet reviewed) | Home, Services Directory |
| `Pattern / Initiative image card` | custom container | Local Components | 145:4114 | Title, Body. Scrim = aeblack-950 value, 0 to 92% fade (a gradient stop bound to a variable loses transparency). Sits as variant `Property 1=Initiative image card` in set `Pattern` 148:14476 | Home (Initiatives) |
| `Pattern / Facility selector item` | custom container set | Local Components | 153:4172 | State = Default / Hover / Selected; Name, Location | Home (Facilities) |
| `Pattern / Facility details card` | custom container | Local Components | 154:4171 | Name, Hours, Location; facility type badge exposed | Home (Facilities) |
| `Pattern / Deck card` | custom container set | Local Components | 163:4316 | Tone = camel / aegreen / seablue / primary; Title, Description, Meta, Icon; audience badge exposed | Home (Prevention) |
| `Pattern / Service row` | component set | Local Components | 198:5480 | Divider = Yes / No; Title, Body, Duration, Fee, Audience; Start Service link (Aegov-Link) | Home (Services) |

In-frame containers (not components): `Container / Stacked deck panel` (Prevention
section), `Container / Facility map` (Facilities section). Home v2 Services 197:5346:
`Container / Category panel` 195:6024 (whitely/50, radius-2xl, padding and gap
spacing-6, custom shadow kept by the user's choice),
`Container / Gradient panel (Find a doctor)` 197:5367 (now solid primary/600, white
text), `Container / Need help` 198:5577 (aegreen/700, white text).

Aegov-Card: use it only when the user asks for it. Boxes in a design are plain
containers (`Container / <Name>`, values bound to DLS variables), not Aegov-Card.

Card Pattern note: Initiative and News variants use a 176px grey placeholder in `media`.

## Tidy-up queue (needs the user's OK before doing any of it)
- Rename `Card Pattern`'s "Property 1" to "Type" (it is already on Local Components);
  review the 3 unlisted variants; group components into Sections; create the Archive page
  for v1 frames.
