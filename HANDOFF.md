# HANDOFF: EHS website redesign on UAE Design System (DLS) 4.0

Read this first, then read `CLAUDE.md` (the project rules; it is the source of truth for
rules, the component registry and all decisions). This file adds what `CLAUDE.md` does
not hold: history, current state, open items, Figma IDs and technical lessons.

## 1. Project in one paragraph
Redesign the Emirates Health Services (EHS) website (https://www.ehs.gov.ae/) in Figma on
UAE Design System 4.0 (previously 3.0). **Design only, no code.** The new homepage is a
showcase of what DLS 4.0 can do: simple, creative, task-led, with the same type, colour
and radius everywhere and the layout changing section by section. Custom containers
(cards and panels) are fine as long as everything inside them is DLS 4.0 and every value
is bound to DLS variables. The user is a UI/UX designer and front-end developer.

## 2. About the user (working style)
- Wants approval gates: plan first, build one pilot, screenshot, stop, wait for OK.
- Credit-sensitive: prefers Sonnet at low/medium effort, one page per request, reuse
  outlines and registry rather than re-querying.
- Works on two PCs (Windows). Project folder example:
  `D:\\Future Internet\\UAE-Design-System-4.0\\EHS` (older: `D:\\Claude\\DLS-4.0\\EHS`).
- Wants concise answers; wants rules learned on each page proposed as `CLAUDE.md` lines
  and added only after approval.
- Desktop (1536) EN only until approved; Tablet, Mobile and Arabic RTL come later.

## 3. Setup (new structure, 2026-11-23)
- Two repos: `toolkit/` (shared plugin `uae-ds4-toolkit`: skills, library keys, mapping)
  and `EHS/` (this project). Both sit in `D:\Future Internet\UAE-Design-System-4.0\`.
- Install the plugin once per PC (see `../toolkit/README.md`).
- Start design sessions in `EHS\design` (core rules) - root `CLAUDE.md` loads too.
- MCP servers (user scope): `figma` (https://mcp.figma.com/mcp, account with a Full seat)
  and `aegov` (https://designsystem.gov.ae/mcp). Optional `playwright` for page capture.
- Permissions: `.claude/settings.json` allows the figma and aegov MCP tools.
- Cost: Sonnet at low/medium effort for building; `/clear` between pages.

## 4. Figma files, pages and IDs
- Working file: https://www.figma.com/design/wAR2tIjblpYdLmfJh3JQnM/EHS-DLS-4.0
  (fileKey `wAR2tIjblpYdLmfJh3JQnM`).
- 4.0 library, the user's published copy (fileKey `1yvKuvJyvNNT9tTv8QmBI5`):
  https://www.figma.com/design/1yvKuvJyvNNT9tTv8QmBI5/UAE-Design-System-4.0--Community-
  Aegov-Card lives on its page node `149:3` (component set `149:437`, 108 variants).
- Original community kit (reference only):
  https://www.figma.com/community/file/1703011733577029978/uae-design-system-4-0
- Working-file pages: `Screens` (0:1, original), `Redesign (4.0)` (24:1143),
  `Local Components` (97:26387), `QA` (24:1144).
- Frames on Redesign (4.0):
  - `EHS / Home / Desktop / EN (v1)` 68:2863 (older Home with card patterns)
  - `EHS / Home / Desktop / EN (v2)` 125:8571 (the current Home design; do not edit,
    work on a copy `(v2 ...)`)
  - `EHS / Services Directory / Desktop / EN (V1)` 72:3605
  - `EHS / Service Detail / Desktop / EN (v2 html layout)` 93:3580
  - `EHS / Home / Health Care Facilities (new layout)` 155:4134 (selector + map design,
    Almadar selected) and `... - Alnahwa selected` 156:4227
  - `EHS / Home / Prevention check-ups (stacked deck)` 164:4313
  - `Card Pattern` component set 117:6259 (still on this page; tidy-up queue says move)
  - 2026-11-23 check: 155:4134, 156:4227 and 164:4313 were NOT found. Current frames
    also include `EHS / Home / Desktop / EN (1920) Sample` 162:16950 (holds the section
    `Check Ups` 162:17020, now Open Data content) and the copy
    `Check Ups (v2 open data)` 189:5075 (deck content applied, approved 2026-11-23).
- Component registry (also in `CLAUDE.md`):
  `sub-page-banner` 97:26409; `Pattern / Initiative image card` 145:4114;
  `Pattern / Facility selector item` set 153:4172; `Pattern / Facility details card`
  154:4171; `Pattern / Deck card` set 163:4316.

## 5. What has been done (chronological summary)
1. Defined the workflow, `CLAUDE.md` rules, the 10 page templates (with AR URLs) and the
   credit-saving settings; connected Figma + aegov MCPs.
2. Home page designed first; header/footer use the library instances; cards were first
   custom wrappers, then migrated to the slot-based `Aegov-Card` via the `Card Pattern`
   component set (Service, Initiative, News, Facility).
3. Library card (user edited their copy): slots `media`, `header`, `badges`, `footer`
   (was `actions`), `body-content` (holds title and body). Link got a trailing-arrow
   property. All 108 card variants audited as identical in structure.
4. Services Directory frame built; filters use Aegov-Label/Checkbox/Select.
5. Page banner became the local component `sub-page-banner`.
6. New design direction: showcase layouts with custom containers (rules in `CLAUDE.md`
   "Boxes", "Showcase direction").
7. Designed this session (all on new frames, Home v2 untouched):
   - Initiative image card (image placeholder + scrim + white text), 4-column preview.
   - Health Care Facilities: selectable list (name + location, Default/Hover/Selected),
     map placeholder with pins, details card inside the map (type badge, full hours,
     location, Directions and Call buttons, View Details).
   - Prevention check-ups: left column (eyebrow, H2, lede, 3 benefits, CTA) and a right
     gradient panel with a stacked deck (state 1 of 4), prev/next, "1 / 4", disclaimer.
8. `CLAUDE.md` updated with: file organisation, component registry, showcase direction,
   Home decisions for the new sections, tidy-up queue.

## 6. Waiting on the user / open items
Approvals pending:
- Facilities section design (155:4134): approve or change.
- Prevention deck section (164:4313): approve or change.
- Insert both into a **copy** of Home v2 (Prevention goes after Latest Initiatives).
- Add to the Home design anything missing from the user's latest full-page screenshot
  only if requested (alert strip and "EHS in Numbers" were not visible in that render).
Open design questions:
- Edge-to-edge image on `Aegov-Card` (news cards): options were inset image (works now),
  change the library card so `media` sits outside the padded area (needs approval; code
  already supports `is-padding="false"`), or a custom container.
- Tidy-up queue (needs OK): move `Card Pattern` to Local Components, rename its
  "Property 1" to "Type", group components into Sections, create an Archive page for v1.
Data and content still needed:
- Facilities: captured map image, each centre's coordinates, phone numbers, map links.
  Note: Abu Mousa may be an offshore island (check coordinates; map should recentre and
  zoom on the selected pin).
- Prevention: clinical sign-off on every age/interval, CTA link target (Itmi'nan page),
  Arabic copy, card 4 meta text ("Ask your doctor"), card 4 is not visible in state 1/4.
- Services Directory: last 4 cards (General Dentistry, Inpatient Services, Issue of a
  Birth Certificate, Issue of a Health Card) may still need their real text.
- Contrast checks pending: aeblack/500 at 12px (deck meta, disclaimer), gold selected
  pin on the grey map, small text over the Initiatives photos, pale hero sub-line.
Longer term:
- When pages are approved, split `CLAUDE.md` into skills (`redesign-page` workflow + QA,
  `sub-page-banner`) to cut per-message cost. `CLAUDE.md` is now about 460 lines.
- Next templates to design in the new direction: Service listing, Facility directory and
  detail, News, Careers/programmes, then Tablet, Mobile and Arabic RTL.
- Possible handoff to development later: the DS components are web components
  (`aegov-*`), Tailwind v4, JS registration required; static HTML only for non-interactive
  parts. This is a separate phase and a separate `CLAUDE.md`.

## 7. Content and design decisions worth remembering
- Home hero: slide 1 only (Home-only exception to "copy 100% of live content").
- Typos in live text: list for approval (example: "Alnahwa Helth Center" -> "Health").
- Truncated "..." text: use full text and Figma truncation, 2 to 3 lines; card bodies are
  a 3-line excerpt.
- Card look: Appearance solid, Variant neutral-min, Size lg, card and content Hug.
- Facility Type is shown as label + Aegov-Badge so the live text is preserved.
- Details-on-map card is fixed at the bottom-left of the map (not anchored to the pin);
  the left selector shows only name + location; actions live in the details card.
- Client wording: "built on DLS 4.0 tokens and components", never "fully compliant".

## 8-9. Technical lessons and library keys
Moved to the toolkit: `toolkit/skills/ds4-library/figma-api-lessons.md` and
`library-keys.md`. Full old text: `HANDOFF.old.md`.

## 10. Starter prompt (paste into Claude Code started in EHS\design)
```
Read ../HANDOFF.md. This continues the EHS website redesign on UAE DS 4.0 in Figma
(design only). Do not build anything yet. Check figma and aegov are connected, summarise
where we are in 10 lines, list pending approvals, then wait. Follow the redesign-page skill.
```

## 11. Session 2026-11-23: repo and plugin setup (context for the next chat)
Read this if you continue from a new chat; it replaces the conversation history.

**Figma check (read only, nothing changed)**
- Figma MCP account: "Future Internet", Full seat on Future Internet Team (Pro). aegov MCP works.
- Working file pages found: Redesign (4.0) 24:1143, Local Components 97:26387, QA 24:1144.
  The `Screens` page (0:1, originals) was NOT found: ask the user before relying on it.
- `Card Pattern` 117:6259 is already on Local Components; it has 3 variants not yet
  reviewed: Service Card V2, Variant7, Home Selection Cards. Property still "Property 1".
- `Pattern / Initiative image card` 145:4114 sits as variant `Property 1=Initiative image card`
  in a set `Pattern` 148:14476. `sub-page-banner` master measured 270 high.
- Redesign (4.0) frames were not re-checked in this session.

**Brand colours (decided)**
- One shared library for all clients (`1yvKuvJyvNNT9tTv8QmBI5`). A client brand is a MODE of
  the library's Color System collection; EHS = `EHSblue` (primary only). Custom components
  stay in each project's Figma file, never in the library.
- Existing EHS frames were built before EHSblue: change mode only on copies, when asked.
- Watch the Figma Pro limit on modes per collection; fallback = a small Brand collection.

**Repos (pushed, GitHub account `futureinternet-claude`, both private)**
- `uae-ds4-toolkit` = `D:\Future Internet\UAE-Design-System-4.0\toolkit`: Claude Code plugin
  with 9 skills (redesign-page, capture-reference, figma-build-rules, aegov-card,
  figma-file-organisation, qa-check, inner-page-layouts, page-from-content, ds4-library
  with library keys, library changes, 3.0→4.0 mapping, aegov MCP usage, Figma API lessons)
  plus `templates/` for new client projects.
- `ehs-redesign` = `D:\Future Internet\UAE-Design-System-4.0\EHS`: root CLAUDE.md (EHS facts,
  templates, registry, showcase direction, tidy-up queue), DECISIONS.md, design/CLAUDE.md
  (always-on core rules), web/CLAUDE.md (HTML placeholder), project skill sub-page-banner,
  references/, assets/. Old full files kept: CLAUDE.old.md, HANDOFF.old.md.
- Why this split: rules reused by every client live in the toolkit; project facts in the
  project repo; design and HTML are folders in ONE project repo (they share outlines,
  assets and decisions). Inner-page layouts are shared across clients; Home and custom
  content pages are per client (skill page-from-content).

**Plugin**
- Installed at user scope on this PC via CLI (the desktop Plugins page does not list
  private marketplaces): `claude plugin marketplace add futureinternet-claude/uae-ds4-toolkit`
  then `claude plugin install uae-ds4-toolkit@uae-ds4-toolkit`.
- After a toolkit change is pushed: `claude plugin marketplace update uae-ds4-toolkit` and
  `claude plugin update uae-ds4-toolkit@uae-ds4-toolkit`.
- Toolkit changes only when rules, the shared library, mapping or shared layouts change;
  Figma design work never needs a toolkit update.

**Working routine**
- Start design sessions in `EHS\design`. Sonnet low/medium for building, `/clear` between pages.
- GitHub Desktop on both PCs (home PC: clone both repos to the same paths, install plugin
  with the two commands above, connect figma + aegov MCPs). Pull before starting, commit
  and push before leaving.

**Still pending from the user** (unchanged): section 6 approvals (Facilities 155:4134,
Prevention deck 164:4313, insert both into a copy of Home v2), news card image option,
tidy-up queue, data/content gaps, contrast checks.
