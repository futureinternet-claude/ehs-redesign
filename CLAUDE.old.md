# UAE DS 4.0 Redesign Project

## Goal
Redesign existing UAE DS 3.0 website pages in Figma using UAE Design System 4.0 only.
Design only, no code.

## Figma
- Working file: https://www.figma.com/design/wAR2tIjblpYdLmfJh3JQnM/EHS-DLS-4.0
- 4.0 library (my published copy, enabled in the working file):
  https://www.figma.com/design/1yvKuvJyvNNT9tTv8QmBI5/UAE-Design-System-4.0--Community-
- Original community source (reference only, do not build from it):
  https://www.figma.com/community/file/1703011733577029978/uae-design-system-4-0
- Pages in working file: Screens (original), Redesign (4.0), Local Components, QA.
  See "File organisation".

## File organisation (Figma file and project folder)
Figma pages
- `Redesign (4.0)`: page and section frames only. Name them
  `<Site> / <Page> / <Desktop|Tablet|Mobile> / <EN|AR> (vN)`; a new section built
  beside a page is `<Site> / <Page> / <Section> (new layout)`.
- `Local Components`: every local component and component set, and nothing else.
  Group them in Figma Sections by type (Banners, Cards, Maps, Panels; add a section
  when a new group is needed). Put each new component in its group, never loose on
  the page.
- `QA`: review boards and checklist screenshots.
- Retired frames (v1 and similar) go to an `Archive` page (create it only when I ask).
  Never delete originals.
Naming
- Composed local patterns: `Pattern / <Name>`. Custom containers inside a frame:
  `Container / <Name>`. Variant properties describe their meaning (State, Tone,
  Type), never "Property 1".
- Layers are named by purpose; no "Frame 123" or "Rectangle 4" left behind.
- Every new component gets a description: what it is, its properties, and a short
  developer note.
Registry
- Check the Component registry below before building anything new. When you create
  or change a component, add or update its registry row (ID, page, properties) in
  the same turn and tell me.
Project folder
- `CLAUDE.md`; `references/<page>.md` plus `references/<page>/` (screenshots);
  `assets/` (images used in designs); `.claude/settings.json` (permissions).
Tidy-up queue (needs my OK before doing any of it)
- Move `Card Pattern` to the Local Components page and rename its "Property 1" to
  "Type"; group components into Sections; create the Archive page for v1 frames.

## UAE Design System MCP (aegov)
- Server: aegov (https://designsystem.gov.ae/mcp). Read-only, no auth.
- This is a DESIGN project. Use it only for guidance, never to generate code:
  - aegov_get_guidelines: rules (typography, colour, spacing, forms, accessibility,
    RTL, button hierarchy). Read the guidelines once at the start of a session.
  - aegov_search_components: find the right 4.0 component, or learn that none
    exists (e.g. no table) and what to use instead.
  - aegov_get_component (response_format: concise): usage rules and variants.
  - aegov_get_pattern: UAE patterns (Emirates ID, address, contact number,
    name, date, dirham symbol).
  - aegov_get_tokens: colour, type, and breakpoint values.
- Never call: aegov_get_setup, aegov_get_examples, aegov_get_component_api,
  or the setup-project / make-rtl / test-accessibility prompts.
- Query once per component type, then save the result in the mapping table.
  Do not re-query the same component.
- Source of truth for BUILDING is the Figma 4.0 library. If the MCP and the
  Figma library disagree, stop and tell me.
- If the MCP says no component exists, do not invent one. Ask me.
- Check for 4.0 components before going custom: DLS 4.0 added new components
  that 3.0 did not have. While planning a page, if a layout looks custom-made
  (anything not an existing mapped component, e.g. stats row, steps, timeline,
  accordion, banner, list, callout, pagination, file/download item), run
  aegov_search_components for it first, then confirm it exists in the Figma
  library (search_design_system). If one fits, propose it in the plan and use it
  instead of a custom frame. If none fits, list it under Open items. Add each
  new finding to the 3.0 → 4.0 mapping table once I approve it.

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

Other About detail pages (same template as #8, use only to check content variations):
- https://www.ehs.gov.ae/en/about-us/organization-structure
- https://www.ehs.gov.ae/en/about-us/health-knowledge-management-strategy

All other pages follow one of these templates. Do not design individual pages
beyond these unless I ask.

## Reference handling
- There is NO reference in Figma. The live URLs are the reference.
- Capture each page once at 1536 wide (full page, in sections if long) and save
  it in `references/`. Capture tablet and mobile only when I ask for them.
  Reuse saved files; never recapture unless I ask.
- Before designing, write a content outline to `references/<page>.md`:
  sections, headings, key text, CTAs, forms, links, item counts.
  Design from the outline plus the screenshots.
- If an Arabic version exists, use its real text. Never invent translations.
- Do not copy 3.0 visuals. Keep the content and information architecture,
  rebuild the visuals with 4.0 components.
- If a page can't be captured (login, bot protection), ask me for screenshots.

## Rules
- Use 4.0 library component instances, variables, and text styles. Slots may also
  hold text (library text styles), image fills, and auto-layout frames named by
  purpose, but never a hand-drawn copy of something the library already has.
- Before building, call search_design_system / get_libraries. If no library
  component exists for something, stop and ask me. Exception: boxes, panels and
  containers (see the Boxes rule below).
- No hardcoded colors, spacing, or fonts. No detached instances.
- No background fills on layout frames. Figma gives every new frame
  (`createFrame`, `createAutoLayout`) a white fill by default. Layout frames
  (section/..., row, grid, column/..., group frames such as `<Name> group`, filter
  sidebars and their groups, hero-actions, and similar wrappers) must have NO fill:
  set `fills = []` in the same script that creates the frame. Only add a fill when
  I ask for it or the live design clearly needs a panel, and then bind it to a
  library colour variable, never white or any hex value. Backgrounds come from
  library components (Aegov-Card, the page banner, and so on) or from a custom
  container (see the Boxes rule below), not from my layout frames.
  Do not add fills to existing frames either.
- Boxes, panels and containers when redesigning from a reference (screenshot or
  site): match the reference's structure. Use a library component when one
  naturally fits (Callout, Banner, Footer-Highlights, Card); otherwise build a
  custom container without asking: a named auto-layout frame
  `Container / <Name>` with every radius, padding, gap, fill and stroke bound to
  existing DLS 4.0 variables, and library text styles and instances inside.
  Aegov-Bento-Grid is layout only (positions and spans); the boxes inside it are
  cards or custom containers. Never hardcode a value or copy the reference's
  brand colours or fonts. If no exact variable exists, use the nearest one and
  list it under Open items. Always meet WCAG AA (text 4.5:1, large text and
  meaningful icons or borders 3:1), including text over coloured fills and
  images; if the reference fails contrast, use the nearest compliant DLS pair and
  tell me. Save each reused container once as `Pattern / <Name>` and add it to the
  Component registry.
- Images are the one exception to "library instances only": place photos as an
  image fill (fill mode: Fill) in the `media` slot. Use the live page's own image;
  otherwise a neutral grey placeholder. No AI-generated images unless I ask.
  Name the layer `image: <short description>` (this becomes the alt text).
- Keep designs code-convertible: nest components inside container components
  (slots), never detach instances, never flatten or outline layers, name layout
  frames by purpose (section/..., row, grid), and keep property names as in the
  library.
- Build each page as new frames on the Redesign (4.0) page. Don't edit frames
  I didn't ask you to touch.
- Scope: build Desktop (1536) EN only, unless I explicitly ask for more.
  Tablet (768), Mobile (375) and Arabic RTL are separate steps that start only
  after I approve the Desktop design. Never create them on your own.
- RTL (when requested): mirror layout, alignment, direction-sensitive icons
  (including link arrows), and reading order.
- WCAG AA contrast. Minimum touch targets per DS guidance.
- Frame names: `<Site> / <Page> / <Desktop|Tablet|Mobile> / <EN|AR>`
- Header and footer: use the library's Aegov-Header and Aegov-Footer instances.
  Do not rebuild them. Fill them with the live page's nav items, logos, links,
  contact details and social links, using the library's own variants and slots.
- Content: copy 100% of the live page content (text, headings, links, image
  slots, counts of items). Do not drop, merge, summarise, or invent content.
  The only exception is the Home hero (see Decisions).
- Where the live page has a pattern with no 4.0 component (carousel, logo strip,
  voice input, mega menu, third-party widgets): do not decide alone. Keep all
  the content, use the closest library components and layout, mark it in a
  short "Open items" list, and let me choose.
- Third-party overlays (chat, customer pulse, sign-language launcher) are not
  designed. List them in the outline as "not designed".
- Pages with tabs or accordions: capture the default state, then note the other
  tabs in the outline. Design the tab component once and reuse it.
- Form fields: every input, select, textarea, checkbox or radio group gets its
  label from an Aegov-Label instance, never a plain text layer. Use the live
  label text exactly (no placeholder "Label" left). Group each field with its
  label in a frame named `<Name> group`. Group headings in a filter sidebar
  (e.g. Type, Gender, Age Group, Health Condition) follow the same rule.
- Free text (page titles, section headings, helper sentences) is allowed only
  with a library text style; never hand-set font, size or colour.
- Truncated text: if the live page shows "..." at the end of a text, do not type
  the ellipsis. Use the full live text if it is available, and set the text to
  truncate with an ending ellipsis, limited to 2 or 3 lines.
- Typos: fix obvious typos in source text only after listing them for my
  approval (for example "Helth" to "Health").
- Changing existing frames: work on a copy named `<original name> (v2 ...)`.
  Never delete originals, old components or loose nodes; list what is now unused
  so I can delete it myself.

## Aegov-Card (container; use for service, initiative, news, blog, event, facility, and similar cards)
Regions, top to bottom inside the card: `media` (slot) → `header` (slot) →
`body-content` (slot, holds `title` (text) → `body` (text)) → `badges` (slot) →
`footer` (slot, formerly `actions`). (`footer` sits after the `content` frame; the
others are inside it.) Different card types are built by filling the slots, never by creating new
card components.
- `body-content`: vertical slot that wraps `title` and `body`. Add content that must
  stay vertically aligned with the text (e.g. Facility hours and location rows,
  key-value lines, icon + label rows) inside it, after `title` and `body`. Library
  instances, text styles and frames named by purpose only; never detach. Do not use
  it for tags above the title (`header`), chips below the body (`badges`) or links
  and buttons (`footer`).
- `media`: only if the live card shows an image or icon. Image fill per the image
  rule above. If the live card has none, delete the slot's placeholder content
  (the "Text 1" layer) and confirm the slot leaves no gap; if it does, tell me.
- `header`: only if the live card has tags or meta above the title. Aegov-Badge
  for categories and audience tags; date or event meta (date, time, location)
  as small text using library text styles.
- `badges`: only if the live card has tags or status chips that sit below the body
  text. Aegov-Badge instances with the live text. `header` stays for tags and meta
  above the title; never put the same badge in both. If the card has no badges
  below the body, hide the slot and confirm it leaves no gap.
- `title`: the live text, in full; it wraps to the card width.
- `body`: always an excerpt, clamped to 3 lines with an ending ellipsis, so cards
  stay even. Use the live text; do not shorten it by hand. If the clamp hides
  important content (e.g. Facility working hours and location), put that content in
  `body-content` instead of the clamped body text, and tell me.
- `footer`: the slot after the `content` frame. It is no longer only for actions: it
  can hold any library component (Aegov-Link, Aegov-Button, Aegov-Timeline,
  Aegov-Accordion items, and so on), at the bottom of the card. Links and buttons
  still follow the same rules: Aegov-Link (text link, optional trailing arrow)
  and/or Aegov-Button; a share or similar icon must be an icon-only
  Aegov-Button/Link named `share`, never a bare icon. One primary action per card.
  Content that must stay aligned with the title and body goes in `body-content`,
  not here.
- Per type: Service = badges in header, Start Service link + share in footer,
  usually no media. News/Blog = media, date + category in header, Read more link.
  Event = media if shown, date/time/location in header, link in footer.
  Facility = type badge in header, hours/location in body, link in footer.
  Use the same layout for every card in one grid.
- Never override the card's radius, border, or padding; choose the closest
  Size/Variant/Appearance. Build the Default state only (Hover and Hover-Glow are
  interaction states).
- Never put another interactive element inside an Aegov-Link.
- Card look: Appearance=solid, Variant=neutral-min, Size=lg, Default state.
- Heights: the card and its `content` frame are Hug, never Fill. Do not give
  cards a fixed height; if rows look uneven, tell me instead of fixing heights.
- Repeated card layouts live in ONE local component set, `Card Pattern` (id
  117:6259, Redesign (4.0) page), with a variant property `Property 1`: Service
  card, Initiative card, News card, Facility card. Place `Card Pattern` instances
  and pick the type with that property; never rebuild a card and never create a
  separate `Pattern / <Type> card` component.
- New card type (Event, Blog, ...): add it as a NEW VARIANT of `Card Pattern`
  (`Property 1=<Type> card`), built only from Aegov-Card slots and library
  instances. Tell me before adding it. Do not create a standalone pattern
  component.
- Using a pattern: the nested card's Title and Body properties no longer drive
  the text (title and body now sit in the `body-content` slot). Edit the `title`
  and `body` text layers directly, the link label on the `link` layer, and the
  date and badge in the News card's `header`. Never replace, swap or reset the
  Aegov-Card inside the Card Pattern: that wipes the text on every instance.
- Text edits in slots: if a title still renders as "Card title" after setting
  `characters`, write it again (set a different value, then the real one) and
  re-check with a fresh screenshot.
- `clone()` of an instance that sits inside a slot puts the copy on the page, not
  in the slot; move it into the slot with `appendChild`. A wrapper instance (for
  example Aegov-Accordion) cannot take extra items; add standalone item instances
  to the slot instead.
- Image placeholders: Initiative and News patterns use a 176px grey placeholder
  in `media` (the library media slot is a fixed 120px and cannot be resized in
  an instance). Unused slots (`media`, `header`, `badges`) are hidden in the Card
  Pattern variants so they leave no gap.

## 3.0 → 4.0 mapping
Build during the first inventory (template 1, Home). For each 3.0 element:
1. find the 4.0 component with aegov_search_components,
2. confirm the matching component exists in the Figma library,
3. show me the proposed pair and wait for my OK,
4. save approved pairs below.

| 3.0 element | 4.0 component (aegov tag) | Figma library component | Notes |
|---|---|---|---|
| Header | aegov-header | Aegov-Header | Rows exposed: logo, emblem, nav items, actions |
| Alert strip | aegov-callout | Aegov-Callout | Danger variant, with controls |
| Hero slider | aegov-header-banner NOT used; image banner + aegov-pagination-compact | Aegov-Pagination-Compact + Aegov-Button | Home only: slide 1 shown, others in outline. Slick.js dots allowed |
| Service / initiative / news / facility card | aegov-card | Aegov-Card | Slot card, see the Aegov-Card section. Slick.js dots for carousels |
| Tabs | aegov-tabs / aegov-tab | Aegov-Tabs / Aegov-Tab | Scrollable row when long |
| Search field | aegov-input | Aegov-Input | Magnifying glass only, no voice |
| Primary / secondary buttons | aegov-button | Aegov-Button | |
| Text links (Start Service, View Details) | aegov-link | Aegov-Link | Text link mode; optional trailing arrow is slot content, not a DS prop |
| Category tag | aegov-badge | Aegov-Badge | |
| Form field label (inputs, selects, filter group headings) | aegov-label | Aegov-Label | Never plain text; label text from the live page |
| Checkbox / radio options in filters | aegov-checkbox / aegov-radio | Aegov-Checkbox / Aegov-Radio | One instance per option, live text |
| Select dropdown | aegov-select | Aegov-Select | Paired with an Aegov-Label |
| Newsletter field | aegov-input (Action slot = envelope button) | Aegov-Input | Panel is a layout frame, or an Aegov-Card with the input and button in its slots |
| Footer | aegov-footer | Aegov-Footer | Use Nav-Column, Social, Bottom-Bar, Tawasul-Logo parts |

## Library changes (my copy differs from the official DS)
- Aegov-Card: added slots `media`, `header`, `badges`, `footer` (renamed from `actions`; accepts any component, not only buttons), `body-content`; Title and Body are text layers. `title` and `body` now sit inside the `body-content` slot (vertical), no longer directly in `content`.
- Aegov-Link: optional trailing arrow ("Show Trailing Icon" property).
- Aegov-Card pattern fixes (override in the Card Pattern variants, not the library):
  title wraps to card width; body clamped to 3 lines.
- Custom containers and other local components are not library changes: see the
  Component registry.
Report any other library edit you make, and do not edit the library unless I ask.

## Component registry (local components; keep this table current)
| Component | Kind | Figma page | ID | Properties / variants | Used on |
|---|---|---|---|---|---|
| `sub-page-banner` | local component | Local Components | 97:26409 | Page Title, Page Subtitle, Content slot | all sub-pages |
| `Card Pattern` | component set | Redesign (4.0) (to move) | 117:6259 | Property 1 = Service / Initiative / News / Facility card | Home, Services Directory |
| `Pattern / Initiative image card` | custom container | Local Components | 145:4114 | Title, Body. Scrim = aeblack-950 value, 0 to 92% fade (a gradient stop bound to a variable loses transparency) | Home (Initiatives) |
| `Pattern / Facility selector item` | custom container set | Local Components | 153:4172 | State = Default / Hover / Selected; Name, Location | Home (Facilities) |
| `Pattern / Facility details card` | custom container | Local Components | 154:4171 | Name, Hours, Location; facility type badge exposed | Home (Facilities) |
| `Pattern / Deck card` | custom container set | Local Components | 163:4316 | Tone = camel / aegreen / seablue / primary; Title, Description, Meta, Icon; audience badge exposed | Home (Prevention) |
In-frame containers (not components): `Container / Stacked deck panel` (Prevention
section), `Container / Facility map` (Facilities section).

## Decisions (Services Directory)
- Filter sidebar: Type, Gender, Age Group and Health Condition groups each use an
  Aegov-Label for the heading; options are Aegov-Checkbox instances; Age Group and
  Health Condition use Aegov-Select.
- Service cards use Card Pattern (Property 1 = Service card). The last 4 cards (General Dentistry,
  Inpatient Services, Issue of a Birth Certificate, Issue of a Health Card) still
  need their real text.

## Page banner (all sub-pages; Home is excluded, it has its own hero)
The banner is now a LOCAL COMPONENT. Use an instance of it on every sub-page;
never rebuild it, copy the frames, or detach it.
- Component: `sub-page-banner` (id 97:26409), on the "Local Components" page of the
  working file. The Services Directory frame uses an instance of it
  (`sub-page-banner`, 1536 wide) as its banner.
- Exposed properties: `Page Title` and `Page Subtitle` (text properties) and
  `Content` (a slot that holds the H1 and the subtitle). Set the two text
  properties from the live H1 and live subtitle or intro line (Arabic: the real
  Arabic text, never invented). Do not add anything to the `Content` slot unless I
  ask.
- Breadcrumb is inside the component: a `Breadcrumb` frame with 4 nested
  Aegov-Breadcrumb-Item instances (Home, then each parent, last item
  State=Current, all Separator=Slash). The component's sample labels are Home /
  Services / Services / Services Directory; override every item's `Label` text on
  the instance from the live page, and keep State=Current on the last visible item
  (set the earlier ones to State=Link). If a page has fewer levels (2 or 3), hide
  the unused items in the instance (hide only; never delete or detach), put
  State=Current on the last visible item, and check the separators still look
  right. If a page has more than 4 levels, stop and ask me.
- If the live page has no subtitle, do not leave "This is subtitle": hide the
  `Sub title (2XL)` layer in the instance, check the banner still looks right, and
  tell me.
- Placement: first element of the page body, directly below the Header (and the
  Alert when shown). Full width (Fill / 1536 at Desktop), no extra wrapper, padding
  or radius around it.
- Structure inside the component, for reference only (do not edit): vertical
  auto-layout, width 1536 fixed, height Hug, padding 80 / 24 / 80 / 24, item
  spacing 20; children are `Breadcrumb` (frame, Fill width, 24 high) and `Content`
  (slot, Fill width, vertical, spacing 20) holding `Page title (H1)` and
  `Sub title (2XL)`. The background is the component's own gradient fill; the old
  `Sub-Page-BG` layer and ellipses are gone.
- Height: 310 at Desktop with a one-line title and subtitle (the component hugs its
  content). If a long title or subtitle makes the banner taller than 310, tell me;
  do not fix it by hand. After setting the properties, check the instance height;
  the Services Directory instance measured 396, not 310, so confirm it is not
  carrying extra content.
- Background: keep the component's gradient fill as it is. Do NOT use
  `assets/sub-page-bg.jpg` (2976 x 616) on sub-pages until I say so; do not change
  the component or swap the background in an instance.
- Do not edit the component unless I ask. If it needs a new property or variant
  (Tablet, Mobile, Arabic RTL), ask me first and list what you propose.
- Text contrast on the background must meet WCAG AA; if it fails, tell me rather
  than changing the colour.
- Breakpoints: this is the Desktop banner. Tablet (768) and Mobile (375), only
  when I ask, reuse `assets/sub-page-bg.jpg`; banner size, padding and type sizes
  for those breakpoints are decided at that step and shown to me first.
- Templates that do not use it: Home (own hero) and the Service detail template
  (no banner, see Decisions (Service detail template)).

## Decisions (Home)
- Header and Footer: place the library Aegov-Header / Aegov-Footer instances as-is,
  do not customise or rebuild them (instances can't take extra children; footer
  holds 3 columns / 5 socials only). Focus all effort and 100% of the content on
  the BODY.
- Services: every card shows "Start Service".
- "Alnahwa Helth Center" corrected to "Alnahwa Health Center"; truncated titles
  use full text.
- Voice input dropped; carousels get simple dots (Slick.js); logo strip is a
  carousel with dots.
- Hero: slide 1 only in the design, other slides listed in the outline. This
  exception is Home-only; no other page may drop content.
- Latest Initiatives: image-led cards in 4 columns (`Pattern / Initiative image card`).
- Prevention check-ups (new section, not on the live site), placed after Latest
  Initiatives: stacked deck, state 1 of 4 shown (card 1 on top, two plain cards
  behind). Content comes from my brief. Open: clinical sign-off on ages and intervals,
  CTA link target, Arabic copy, card 4 meta text ("Ask your doctor").
- Health Care Facilities: selectable list on the left (name and location), map on the
  right with the details card inside it (type, full hours, location, Directions and
  Call buttons, View Details). Open: captured map image, each centre's coordinates,
  phone numbers and map links (not on the live cards).

## Layout mode (same as reference or new layout)
- When I ask you to redesign a page and have not said which, ASK FIRST in the plan
  step: "same layout as the reference site, or a new layout?" Do not assume.
- If I say "new layout" (or ask directly to create a new layout), do not ask again.
  Propose a layout that makes the most of the 4.0 components (see "Check for 4.0
  components before going custom"), and show it in the plan before building.
- Either way, 100% of the live content is kept; only the layout changes.
- Icons: use the "Phosphor" library in Figma (icon components, never hand-drawn).
  Icons beside labels or inside icon-only buttons are allowed.
- Plain-text lists (bullets) are allowed as text with library text styles.

## Showcase direction (whole site)
- The new design is a showcase of what DLS 4.0 can do: simple and creative, with the
  same type, colour and radius everywhere and the layout changing from section to
  section. Custom containers are allowed on any page under the Boxes rule.
- Limit the whole site to four container types: standard Aegov-Card, image-overlay
  card (`Pattern / Initiative image card`), gradient panel (the stacked deck panel),
  and the details card on a map (`Pattern / Facility details card`). Ask before adding
  a fifth type.
- Rhythm: do not put more than two consecutive sections on a page in the same
  container style.
- Client-facing wording: "built on DLS 4.0 tokens and components", never "fully
  compliant" or "official components" for custom containers.

## Decisions (Service detail template)
- Template for all service detail pages. Layout: NEW (not the 3.0 layout).
- No sub-page banner on this template. Breadcrumb, title and actions sit at the top
  of the body.
- Key facts (duration, service type, sub service type, target audience) go in an
  Aegov-Bento-Grid; this changes the order from the live page and is approved.
- Service Process uses Aegov-Timeline (vertical); FAQ uses Aegov-Accordion.
- Not designed (listed in the outline as "not designed"): chat launcher,
  sign-language launcher, survey / customer pulse widget.
- Typos in source text stay as live text until I approve fixes (list in the
  outline).

## Workflow (per page)
1. Capture: screenshot the URL at 1536 wide, save to `references/`, write the
   content outline.
2. Plan: list each section, its 4.0 component, and anything with no equivalent
   (Open items). Do not build yet. Wait for my OK.
3. Build Desktop (1536) EN only, using the library Header and Footer instances.
4. Take one screenshot, self-check against the QA checklist, then STOP and wait
   for my approval.
5. Batch feedback: wait for my full feedback before editing.
6. Only after I approve Desktop: build Tablet, Mobile, or Arabic RTL, each only
   when I ask for it.
7. For any change that touches many instances (cards, labels, buttons), do one
   pilot, screenshot it, and wait for my OK before rolling out to the rest.
8. After each page, list the rules learned as proposed CLAUDE.md lines and wait
   for my OK before adding any.

## Credit-saving rules
- Work on one page per request. Never "redesign the whole site."
- Reuse saved screenshots and outlines; don't re-read the live site.
- Prefer the outline (.md) over re-reading images.
- Reuse `Card Pattern` variants and the mapping table; don't rebuild or re-query.
- Screenshots only at checkpoints, not after every small edit.
- Ask before doing anything large or repeated.

## QA checklist
- [ ] Desktop EN frame (1536 wide) exists; other breakpoints and Arabic only after approval
- [ ] All elements are 4.0 instances or allowed slot content; variables and styles used
- [ ] No fills on frames I created: scan them for visible solid fills and list any
  that exist (id, name, bound or not). Remove unbound ones I created; report the rest.
  `Container / ...` frames may have fills only if bound to library colour variables
- [ ] Custom containers: every value bound to DLS 4.0 variables, contrast checked
  (including text over images), saved as `Pattern / <Name>` and added to the
  Component registry
- [ ] No 3.0 leftovers or detached instances
- [ ] Cards: slots filled per the Aegov-Card section; no empty-slot gaps
- [ ] No clipped text: every title, body and label is fully visible, or intentionally excerpted
- [ ] No placeholder text left anywhere (Card title, Label, Text 1, Slot)
- [ ] No plain text that has a library equivalent: list every free text layer and confirm none should be an Aegov-Label, Badge, Link or Tab
- [ ] A sample of cards in each section (first, middle, last) has the real live text from the outline, not defaults or another card's text
- [ ] Content matches the live page (nothing missing or invented)
- [ ] Contrast meets AA
- [ ] Frame names follow the convention
