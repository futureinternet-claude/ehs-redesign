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

## 3. Setup to recreate on the new account
1. Copy `CLAUDE.md` and this file into the project folder; start Claude Code **inside**
   that folder (`cd` there, then `claude`), so `CLAUDE.md` loads automatically.
2. MCP servers (add with `--scope user` so they work in any folder):
   - `claude mcp add --scope user --transport http figma https://mcp.figma.com/mcp`
     then `/mcp` > figma > Authenticate with the Figma account that can **edit** the files.
     The account needs a Full seat (a Dev or view seat is read-only for writes, even if the
     file's sharing says anyone can edit).
   - `claude mcp add --scope user --transport http aegov https://designsystem.gov.ae/mcp`
     (read-only DLS docs; used for guidance only).
   - Optional: `claude mcp add --scope user playwright -- npx @playwright/mcp@latest`
     for page capture. Disable unused connectors (for example Claude Docs) in `/mcp`.
3. Permissions: `.claude/settings.json` in the project:
   `{"permissions":{"allow":["mcp__Figma__*","mcp__aegov__*"]}}`. On the PC the Figma tool
   prefix may be `mcp__plugin_figma_figma__*`; add it if prompts continue.
4. Cost settings: `/model` Sonnet, `/effort` low or medium, `/clear` between pages.
5. The new account must have edit access to both Figma files below.

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

## 8. Technical lessons (Figma MCP / Plugin API in this project)
- Always `create_session` per file first and pass the sessionId. Never run two writing
  `use_figma` calls in parallel. Load the figma-use skill resource before writing.
- Writes failing with "read-only mode" = the connected account has no edit seat.
- Cloned slot nodes lose their property links and turn into plain frames. To add a slot
  to a variant use `component.createSlot()`, set `componentPropertyReferences =
  { slotContentId: <existing slot property key> }`, then delete the stray property that
  `createSlot` creates. Slot height/min-size cannot be overridden in an instance.
- A gradient stop bound to a colour variable resets its alpha to 100%: a fading scrim
  must use the token's colour value with stop transparency (documented exception).
  Opaque gradients (for example primary/50 > white > camel/50) can be bound.
- "Fill" height chains give stale heights after text overrides. Use Hug; toggle
  HUG then FILL to recompute if needed. Fixed row heights are static.
- Replacing or resetting the nested Aegov-Card inside a pattern wipes text overrides on
  every instance. Text in patterns is edited on the `title`/`body` layers directly.
- `isExposedInstance` only works once the instance is inside a component.
- A button label may not follow the `Text#2020:0` property; set the text node directly.
- `setTextStyleIdAsync` / `setRangeTextStyleIdAsync` apply library text styles (mixed
  bold in one text node works). Load fonts before any text edit.
- `get_screenshot` can return a stale render after edits: re-render with a different
  `maxDimension` or `contentsOnly: true`. Use `enableBase64Response: true` (curl to
  figma.com is blocked in the cloud session).
- `search_design_system` can return huge results saved to a file: parse the file with
  Python and print only name + key. Search with `includeLibraryKeys` for the 4.0 library.
- The cloud session could not reach ehs.gov.ae or designsystem.gov.ae: the user pasted
  the DS docs manually. If network access is needed, ask the user to allow hosts.
- Opening a section as a standalone frame next to Home v2 (not editing v2) is the safe
  pattern; `clone()` of a node inside an auto-layout parent adds the copy to that parent,
  so move it to the page immediately.

## 9. Appendix: keys used in scripts (import with `importVariableByKeyAsync`,
`importStyleByKeyAsync`, `importComponentSetByKeyAsync`)
Libraries: 4.0 = `lk-cd330742ecfb37e0fca8c1646beb1f06f871e8ba6728303d3d94bad84ba0cba7911957660b0188cef94be20cfaab8f77b3ff8f1e48d6e9864319e19bae745393`;
Phosphor = `lk-365b9ee65bb64dd89d4f69239658b2e1cece42f09976b9ea995aac6368a7cfd1a57156183c74ac6f2bc446e6e9d77714be6a2711e262ca8ac4475566d930c2a9`.
Component sets: Aegov-Card a2bee320390090e580f242f88faf06a4252a8e7f; Aegov-Link
dc6cfc3f7540a17eb3631680bb45ad12cc869767; Aegov-Button 86321fad1887f3675655f81c9c6aa955dfc07da7;
Aegov-Badge 2bd21d8d4cdbdfffc764ea6077493ca307605bc2.
Phosphor sets (variant "Format=Outline, Weight=Regular"; Fill for filled): MapPin
038a32cfb009e5f8f9d9874cbc4107655148642f; Phone 18515ff39ce97067330523293bce1d44d8d2b71f;
Stethoscope a1cb4a8efd4196bc13fb24b4ce9702fe17c89d99; TestTube
fd4b7f2a449920080d6b67d726ce22aea314c4f2; Drop e079d378695cf28ab9c8c6cac6b31c3f81831abf;
Heartbeat 9a75a99d790be0b30ce80f7f5b4b90f1f261a42e; ClipboardText
dfcc505b793749a970e52fdf926d7661397b4206; UsersThree 380ca4b73ef9493a581730a3ed23be3d98490840;
ArrowLeft 0db50eb761378e8d8ae566630236de4d6d1343fc; ArrowRight 4ade4a963c7168f55a7500710e758f401f17cd5b.
Property keys: Button `Text#2020:0`, `Leading icon#61:3204`, `Leading icon swap#61:4005`,
`Trailing icon#61:4806`, `Icon#61:6408` (icon-only); Badge `Label#80:0`; Link `Label#121:0`,
`Show Trailing Icon#2033:218`. Button variant example:
`Variant=primary, Appearance=outline, Size=sm, State=default, Shape=text`.
Variables: radius-xl 27c98d18e2623e5dd7a24171cae16c9dc8de6e4f (12); radius-2xl
305316024978604d706e2b834d2012f52b46c1d5 (16); spacing-1 b18dc7a67b9186f90a9bf1ccb3a4a93c002d62e8;
spacing-2 fcc865d844ef6b425b61ba4462b637a91c68b56a (8); spacing-3 2a371d6d0aaf658b5e97ada8073219f4b8812aea;
spacing-4 daf096312c68df848e17871b6010bd8e85997a1c; spacing-5 1354842c64ba873e619b430ce3656b4fa06fe663;
spacing-6 07d09101e87525220b3cc827b6ba3f88c8d2e5d6 (24); spacing-8 9c70893fd561c66eb34eb569b7ad69b00ce7b430;
spacing-12 1cf44817cf620c1e3d4d0a99e12311f1dd98d247 (48); spacing-16 e2fcc6b016b7690fed5293be3ad419eccc34ea00.
Colours: whitely/50 eb8789bc291ff8775506eea0a0b988caa12b38ba (white); aeblack/50
a01e1dee30fb2a7156a4d4004430ab2c3c6b3062; /100 2d6c9fb843bfecaac9d9fe8a498705dc60f280db; /200
b15b881c2f64b4011c573023e2503b305cc8659a; /300 c97ecbeb6d3ba5f5270d08282765e2b1031a9df5; /500
2536eeed73e794abd91c276e6484e2a0244881f3; /600 b28ce5a6eac68fe9e27ee9f8637095c4f7e4c3a0; /700
47029d335bbc587af7ea1a209b9e3cdb8069b64f; /800 7ef3d16d467fa3bed87bfaf0746ba968430063eb; /950
5e42515f212108a76d56bc5ef18c5ee0b56d486d; primary/50 dad2dd95563fc38008dfa956395488da9748398f;
/100 bf74b61c65cf038bd89882564a4c0cfbe362e45b; /600 45038a1afbadd308debf827b2040c1f7f5171bcf; /700
701d4976c80b564dc910146aba00040cdacc4316; camel/50 e4a490f960c77e290c8846114343eb1ef4bb02da; camel/100
8903cffa1b809b823bee33abf098ae02beb50be4; camel/700 a1fc69470e3561f12eb66bc7ecc94bf938e7e92c;
aegreen/100 9ac8d9a53309cd4affda7428a22d9dc1627a981e; aegreen/700 b013932edfb95ae179a0a4ab3ce83a59e80cd2e2;
seablue/100 7d4bb93fa8b63bc4f0b80ead7c269ed2d86abc8a; seablue/700 7cd81f58433dd5a706355c63e670f40b5b0cb0ea.
Text styles: EN/Heading/H2 42dca54929ecea271415f86f67d0dab6e645d7ba; Component 20/28 SemiBold
9fdc54b70ac927b8834872c877f5e106c63c4453; Component 18/28 SemiBold 96e17dcaea8a54f7797ddd6212ff58d3f7ac68d9;
Component 14/20 SemiBold 2a29abdea2296334ec7dd162053e0f6e19599e4a; Body LG Regular
424319f7dacac89dbb6bf416ef9d59d5e4b5f4a6; Body Base Regular e4205df13d94aedacd1577129aaefa5b9709e094;
Body Base Bold 550e01d18383f2ec9a0f8bf65577c7c661d8c85e; Body SM Regular
a57e813ccebbcac3088acb56888ef68212cc714b; Body SM Bold d0f4c9c8a731967fbc247d9c1b8eed6bb0d68fc3;
Body XS Regular 708163571acb84c9741ca30f91da68229a895807. Effect style shadow-xl
0a863c41865877bcfcc1774ab6fb202c31a72d65.

## 10. Starter prompt for the new account (paste into Claude Code in the project folder)
```
Read HANDOFF.md and CLAUDE.md in this folder. This continues the EHS website redesign
on UAE DS 4.0 in Figma (design only). Do not build anything yet.
1. Check /mcp: figma and aegov connected? Ask Figma "who am I" and confirm you can see
   the file wAR2tIjblpYdLmfJh3JQnM and its page "Local Components".
2. Summarise in 10 lines where we are, and list the pending approvals from section 6.
3. Then wait for my instruction. Follow CLAUDE.md: plan first, pilot, screenshot, stop.
```
