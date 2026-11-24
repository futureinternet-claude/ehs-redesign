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

## Content page rules (templates 8 and 9; learned from the approved About detail, 2026-11-24)
- Content runs the full 1488 width (content frame padding spacing-6 left/right), not a
  narrow centred column.
- The first section pairs an image with its text side by side, image on the left
  (radius bound to a DLS radius variable), text vertically centred.
- `sub-page-banner`: leave the subtitle off when the live page has none.

## Component registry (local components; keep this table current)
| Component | Kind | Figma page | ID | Properties / variants | Used on |
|---|---|---|---|---|---|
| `sub-page-banner` | component set | Local Components | 214:5528 | Layout = Centered (97:26409, the original) / Search (214:5496: left-aligned, "Search a service" Aegov-Input in the Content slot; proposed for Services Directory v2, awaiting approval) / Centered Search (228:5982, added 2026-11-23: option 3 chosen by the user; centred breadcrumb, H1, subtitle, search and a "Most used:" row of Aegov-Checkbox-Pill quick links in the Content slot; background = primary/50 to whitely/50 gradient plus an absolute `Aurora glow` layer of 4 blurred token-bound ellipses (seablue/100, camel/50, aegreen/100, primary/100), like the Home v2 hero; 395 high with subtitle); Page Title, Page Subtitle, Content slot. Measured 270 high on 2026-11-23 | all sub-pages |
| `Card Pattern` | component set | Local Components | 117:6259 | Property 1 = Service / Initiative / News / Facility card; News card v2 201:5479 (plain container, not Aegov-Card: image 240 + white fade, date, category badge, title 3 lines, View Details; props News title, News date); also found: Service Card V2, Variant7, Home Selection Cards (not yet reviewed) | Home, Services Directory |
| `Pattern / Initiative image card` | custom container | Local Components | 145:4114 | Title, Body. Scrim = aeblack-950 value, 0 to 92% fade (a gradient stop bound to a variable loses transparency). Sits as variant `Property 1=Initiative image card` in set `Pattern` 148:14476 | Home (Initiatives) |
| `Pattern / Facility selector item` | custom container set | Local Components | 153:4172 | State = Default / Hover / Selected; Name, Location | Home (Facilities) |
| `Pattern / Facility details card` | custom container | Local Components | 154:4171 | Name, Hours, Location; facility type badge exposed | Home (Facilities) |
| `Pattern / Deck card` | custom container set | Local Components | 163:4316 | Tone = camel / aegreen / seablue / primary; Title, Description, Meta, Icon; audience badge exposed | Home (Prevention) |
| `Pattern / Service row` | component set | Local Components | 198:5480 | Divider = Yes / No; Title, Body, Duration, Fee, Audience; Start Service link (Aegov-Link) | Home (Services) |
| `Pattern / Open Data deck` | component set (interactive) | Local Components | 209:5464 | State = 1..6 (top card = dataset n, next two behind, counter "n / 6"); Next/Previous = Change to next/previous state, Smart Animate 300 ms ease out; arrows disabled at 1 and 6; cards are `Pattern / Deck card` | Open Data copy 189:5075 |
| `Pattern / Our Updates carousel` | component set (interactive) | Local Components | 213:5856 | Tab = News / Events / E-Consultations × Position (2, 2, 3); tab click = Dissolve 200 ms to Position 1; arrows = Smart Animate 300 ms, disabled at the ends; cards = Card Pattern News card v2 / E-Consultation card 212:5042 (props renamed Card title, Card date) | Home v2 Our Updates |
| `Pattern / Initiative slider` | component set (interactive) | Local Components | 218:5739 | State = 1..4 (Tameni, Youth Voice, Nursing Scholarships, Promotional Campaign for Telemedicine Services); heading row + clipped `viewport` with a `track` of all 4 slides (photo, badge, title, description, Know More), track offset per state so Smart Animate slides sideways; arrows = Smart Animate 300 ms, disabled at the ends | Home v2 Latest Initiatives |
| `Pattern / Mega menu` | component set (interactive) | Local Components | 221:5771 | State = Closed / Services / Digital Participation / Open Data / About Us / Media Center / Awareness Center; every state has hover areas for all 6 items (Mouse enter switches). Invisible hover areas over the Aegov-Header nav items (Mouse enter = open, Mouse leave on the open state = close); hovered item = Aegov-Navbar-Item State=Hover, Submenu on, on a white mask; panel `Container / Mega menu panel` (whitely-50, aeblack-200 border, radius-xl, shadow-xl) with categories left, tinted aeblack/50 side column, `Container / Menu feature card` (primary/700). Instance placed absolutely over the nav row (x 0, y 132) | Home v2 (221:5774) |
| `Pattern / Filter group / Type`, `/ Gender`, `/ Age Group`, `/ Health Condition` | component sets (interactive) | Local Components | 238:7883, 238:7916, 238:7947, 238:7978 | State = Collapsed / Expanded (Type also Expanded all: first 5 options + "Show all (9)" [new] in Expanded, all 9 in Expanded all). Header = Aegov-Accordion-Item (Divider off, content text hidden); options under it = Aegov-Checkbox / Aegov-Select; top border aeblack/200. On click header = Change to the other state, Show all = Change to Expanded all, Smart Animate 200 ms ease out | Services Directory v4 237:5850 |
| `Pattern / Service results` | component set (interactive) | Local Components (Interactive sections) | 264:9016 | View = List (264:8740: toolbar + `Container / Results panel` with the 12 live `Pattern / Service row`) / Grid (264:8741: same 12 services as Card Pattern Service card, 3 per row at 1092 wide, equal heights per row); Layout Filter toggle: active = Aegov-Button outline, inactive = soft; click the inactive button = Change to the other View, Dissolve 200 ms ease out | Services Directory v4 237:5850 (instance 264:9267) |
| `Pattern / Service category tabs` | component set (interactive) | Local Components (Interactive sections) | 273:9582 | Tab = Health prevention (273:8917) / Primary care / Specialized care / Certificates / Customer service; each = the Home v2 `Container / Category panel` layout (984 wide): Aegov-Tab row (that tab Selected; row scrolls sideways in the prototype, overflow horizontal, so tab 5 can be reached), title + icon tile (ShieldPlus, Stethoscope, FirstAid, FileText, Headset), 3-4 `Pattern / Service row` (last Divider=No), Aegov-Link "View All ( n )". Click a tab = Change to that Tab, Dissolve 200 ms ease out. Content: references/home-services-tabs.md | Home v2 Services (instance 273:9623) |
| `Pattern / Facility hours row` | component set | Local Components | 205:7125 | Divider = Yes / No; Name, Type · location, Hours; `Container / Hours track` (aeblack/100 track, primary/600 open segment; set the open range with the track's left/right padding = closed hours, because Aegov-Range's fill cannot be moved in an instance); Directions button, View Details link | Home (Facilities) |

In-frame containers (not components): `Container / Stacked deck panel` (Prevention
section), `Container / Facility map` (Facilities section). Home v2 Services 197:5346:
`Container / Category panel` 195:6024 (whitely/50, radius-2xl, padding and gap
spacing-6, custom shadow kept by the user's choice),
`Container / Gradient panel (Find a doctor)` 197:5367 (now solid primary/600, white
text), `Container / Need help` 198:5577 (aegreen/700, white text).

Aegov-Card: use it only when the user asks for it. Boxes in a design are plain
containers (`Container / <Name>`, values bound to DLS variables), not Aegov-Card.

Card Pattern note: Initiative and News variants use a 176px grey placeholder in `media`.

Card Pattern Service card (67:2853), lesson 2026-11-23: do NOT append anything to the
variant's `body-content` slot. It replaced the slot's default nodes, wiped the title and
body overrides on every instance that used the default content (V1 Services Directory),
and component properties cannot be bound inside the slot. The default title/body were
rebuilt (234:7148, 234:7149) and the 9 V1 cards re-filled with live text. Add extras
(for example the `meta` row) to each instance's own slot instead.

## Local Components sections (since 2026-11-24)
Every component lives inside a labelled Figma Section on `Local Components`; nothing loose:
- `Banners & navigation` 258:8278: sub-page-banner, Pattern / Mega menu
- `Cards` 258:8279: Card Pattern, Pattern (Initiative image card), Pattern / Deck card,
  Pattern / Facility details card
- `Rows & list items` 258:8280: Pattern / Service row, Pattern / Facility hours row,
  Pattern / Facility selector item
- `Filters` 258:8281: the 4 Pattern / Filter group sets
- `Interactive sections` 258:8282: Pattern / Open Data deck, Pattern / Our Updates
  carousel, Pattern / Initiative slider, Pattern / Service results,
  Pattern / Service category tabs
Rule: put each new component straight into the section it belongs to (to the right of the
last item, same spacing); add a new labelled section only when no existing one fits, and
tell the user.

## Tidy-up queue (needs the user's OK before doing any of it)
- Rename `Card Pattern`'s "Property 1" to "Type" (it is already on Local Components);
  review the 3 unlisted variants; create the Archive page for v1 frames.
