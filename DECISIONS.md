# EHS page decisions

Read only the section for the page you are working on. Add a section per page once the
user approves its decisions.

## Home
- Header and Footer: place the library Aegov-Header / Aegov-Footer instances as-is, do
  not customise or rebuild them (instances can't take extra children; footer holds 3
  columns / 5 socials only). Focus all effort and 100% of the content on the BODY.
- Services: every card shows "Start Service".
- "Alnahwa Helth Center" corrected to "Alnahwa Health Center"; truncated titles use full
  text.
- Voice input dropped; carousels get simple dots (Slick.js); logo strip is a carousel
  with dots.
- Hero: slide 1 only in the design, other slides listed in the outline. This exception is
  Home-only; no other page may drop content. (Mapping: hero slider = image banner +
  Aegov-Pagination-Compact + Aegov-Button; aegov-header-banner not used.)
- Reusing a section's layout for new content: change the card text, counter, disclaimer
  and icons together; no leftover text or icons from the old content.
- Latest Initiatives: image-led cards in 4 columns (`Pattern / Initiative image card`).
  Home v2 (user's redesign, then prototype built and approved 2026-11-23, taglines
  approved): one large
  slide (photo left; badge, title, description, Know More right) as the interactive
  `Pattern / Initiative slider` 218:5739 (instance 218:5758; old heading row 133:14341 and
  slide 195:6464 hidden). 4 live initiatives with live descriptions; photos from the
  "Initiative cards" frame (Tameni keeps the user's photo). Badge taglines are new copy
  for approval: Keeping Families Informed (user's), Empowering Young Talent, Building
  Future Nurses, Digital Health Services.
- Prevention check-ups (new section, not on the live site), placed after Latest
  Initiatives: stacked deck, state 1 of 4 shown (card 1 on top, two plain cards behind).
  Content comes from the user's brief. Open: clinical sign-off on ages and intervals, CTA
  link target, Arabic copy, card 4 meta text ("Ask your doctor").
- Open Data (2026-11-23): reuses the Prevention section layout (left column + gradient
  panel with `Pattern / Deck card`) and replaces its content on Home. Source:
  https://www.ehs.gov.ae/en/open-data (intro + 16 "Read more" links, no card descriptions
  on the live page). Option A (live text only) was chosen, then the user built the left
  column with the Option B copy, which stands as built (user's own edit):
  - Left: eyebrow "Open Data"; H2 "Open Data For Everyone" (new copy); lede = live intro
    verbatim; rows: Reports and statistics / Real time data / Propose Display or Request
    Data (bold labels and the "Can't find what you need? Ask for it." line are new copy);
    CTA "Explore Open Data" (new label) -> /en/open-data.
  - Deck: 6 datasets (Real Time Data - Outpatient Appointments, Numbers & Statistics,
    Geospatial Data - Hospitals, Open Data Charts, EHS Budget, EHS Research), order as
    listed but Numbers & Statistics on top (1 / 6). Approved card content (title / sub-line
    / badge / meta):
    1. Numbers & Statistics / Search by Category, SDGs and Date range / Statistics /
       Downloadable reports
    2. Real Time Data - Outpatient Appointments / Total appointments by citizenship / Real
       time / By facility, emirate and age group
    3. Geospatial Data - Hospitals / Hospitals on the map, with directions / Map /
       Outpatient and Inpatient Occupancy 2021 (live typo "InpatientOccupancy" fixed)
    4. Open Data Charts / Choose a topic to view the charts. / Charts / 2023, 2024, 2025
    5. EHS Budget / Budget Allocation, Revenues and Expenses / Finance / Budget 2022 to 2024
    6. EHS Research / Research Publications, Data Driven Reports and more / Research /
       4 resources
    Disclaimer: "Use of this data is subject to the Open Data Usage Policy." (links to the
    policy page). Each card links to its dataset page.
  - Approved 2026-11-23 on `Check Ups (v2 open data)` 189:5075. Later the same day
    (approved): left-column icons ChartBar / Pulse / ChatCircleText; deck
    replaced by the interactive `Pattern / Open Data deck` 209:5464 (instance 209:5489;
    old stage 189:5097 and controls 189:5101 hidden). Card icons: ChartBar, Pulse,
    MapPin, ChartPie, Coins, BookOpen (Fill weight); tones camel, aegreen, seablue,
    primary, camel, aegreen. Arrows disabled at 1/6 and 6/6 (no loop).
  - Placed in Home v2 as `Open Data (v2 deck)` 210:4734 (Home v2 padding); the
    Prevention `Check Ups` 162:19409 hidden, not deleted (answers the open question:
    Prevention is off Home v2 for now).
  - Open: whether the Prevention section stays anywhere on Home; client approval of the
    new copy.
- Services (2026-11-23, approved on `Services (v2 panel)` 193:5102, standalone frame).
  Placed in `EHS / Home / Desktop / EN (v2)` 125:8571 as `Services (v2 panel)` 197:5346
  (user's instruction to edit Home v2 directly); old `Services` 127:12902 hidden, not
  deleted. Home sample 162:16950 not changed. Pattern
  `services-panel-with-side-actions`, variant B (user's refs):
  - Heading "Services" (live) + "Search a service" field (copied from Services Directory).
  - "Most Used" badge + row of 4 `Card Pattern` Service cards (live Most Used items 1-4;
    the 5th, Submit Medical Complaints, via View all).
  - Category tabs: the 5 live categories only (All Services, Most Used, My Favourites
    dropped from this row); Health, prevention and periodic Screening selected.
  - Category panel = Aegov-Card lg: category name as title, no lede (none live), 4
    full-width rows in live tab order (no overlap with Most Used): title, 2-line excerpt,
    meta (duration live; fee and audience shortened = [new wording], approved), Start
    Service on the right; "View all Services" in the footer.
  - "Track your application" replaced by "Find a doctor" (gradient panel): Facility and
    Specialty selects + Search -> /en/services/doctors (380 doctors, no booking on the
    live page). "Need help?" Aegov-Card with live channels (Toll free call 8008877,
    Working Time 7:30 AM-3:30 PM, info@ehs.gov.ae, Tawasul 171) + Contact Us. No live chat.
  - Open: search field still shows the mic icon (copied as approved on the directory);
    client approval of the [new] copy.
  - Later the same day (user's redesign): category panel and Need help are plain boxes,
    not Aegov-Card (`Container / Category panel` 195:6024, `Container / Need help`
    198:5577, aegreen/700); rows are `Pattern / Service row` 198:5480 instances; Find a
    doctor is solid primary/600 with white text.
- Services Most Used cards (2026-11-23): a duration / fee / audience row was tried and
  REMOVED at the user's request (did not fit). Cards in Home v2 197:5346 now hug content
  at an equal height of 196 (was a fixed 214). Live values found, for later use:
  Pre- Employment Medical Examination 24 hours, 266 AED, applicants above 18;
  Pre-University Fitness Screening 3 working days, 250 AED, students planning to join a
  university.
- Our Updates (2026-11-23, approved): `Our Updates (v2 news)` 201:5499 in
  Home v2, old 162:19468 hidden. Pattern `news-carousel-image-cards` (user's ref).
  Eyebrow "Media Center" (live menu name, uppercase via text case), H2 "Our Updates"
  (live), no lede; "View all" outline button + arrows on the right; live tabs News /
  Events / E-Consultations kept; 4 live news as `Card Pattern` = News card v2 (3 full + a
  peek). Live dates corrected (03 Nov, 21 Oct, 16 Oct, 05 Oct 2026). Old News card
  variant kept for Home v1 and the 1920 Sample.
  - Open: 4th card image (Global Patient Safety Award 2026) not captured, grey
    placeholder.
  - Prototype (approved 2026-11-23): tabs + cards replaced by the interactive
    `Pattern / Our Updates carousel` 213:5856 (instance 213:5879); old tabs, card row and
    heading arrows hidden. Arrows moved to the tabs row (a click can only change its own
    component). Events tab: 4 live events (photos not captured, placeholders);
    E-Consultations tab: 5 live items on the new E-Consultation card (status badge
    Current = aegreen, Planned = neutral; "Closing/Opening dd/mm/yyyy").
- Health Care Facilities (2026-11-23, approved): `Health Care Facilities
  (v2 hours)` 206:4625 in Home v2, old selector + map section 150:14714 hidden. Pattern
  `facility-finder-hours-timeline` (user's ref). H2 + View All; emirate tabs "All" [new
  label] + the 6 live emirates (no Abu Dhabi on the live filter); `Container / Facilities
  panel` (white, radius-2xl, same shadow as the Services category panel) with 4
  `Pattern / Facility hours row` instances: live name, type · location, full live hours
  text, hours bar = main weekday range (Almadar 08-18, Alshrooq 07:30-22, Alnahwa 08-13,
  Abu Mousa 08-14), Directions (live map link on each detail page) + View Details.
  - Not shown (no real-time data): "open right now" line, Open now badge, now marker,
    "x of y shown". Map and `Pattern / Facility details card` no longer used on Home v2.
  - Aegov-Range was planned for the bar but its fill cannot be positioned per instance;
    replaced by a token-bound track (tell the user if a library fix is wanted).
- Health Care Facilities: selectable list on the left (name and location), map on the
  right with the details card inside it (type, full hours, location, Directions and Call
  buttons, View Details). Open: captured map image, each centre's coordinates, phone
  numbers and map links (not on the live cards).
- Facility Type is shown as label + Aegov-Badge so the live text is preserved.
- Details-on-map card is fixed at the bottom-left of the map (not anchored to the pin);
  the left selector shows only name + location; actions live in the details card.

## Header mega menus (all nav items except Home and AI)
- Live menu content: `references/main-navigation.md` (2026-11-23).
- Pilot built 2026-11-23 (awaiting feedback): `Pattern / Mega menu` 221:5771, Services
  only, on Home v2. The library has no mega menu (Aegov-Dropdown-Panel is a single list),
  so the panel is a custom container styled like it. The Aegov-Header is untouched; the
  menu is an overlay instance with hover areas.
- Services panel: "Service categories" [new heading] with the 5 live categories, Phosphor
  icon tiles, one-line descriptions [new copy] and live "View All ( n )" links; side
  column "Other services" and "Related links" [new headings] with live links; feature
  card "Doctors" (live label) + [new] line "Find EHS doctors by facility and specialty."
- User feedback: not full width. Panel hugs its content (left column 520, side column
  360, about 882 wide), start-aligned under its nav item; the open state's hover area is
  trimmed to the panel so leaving the panel closes it. Apply to every menu.
- All 6 menus built and approved 2026-11-23 (new copy approved), live links only,
  groupings as planned. New copy: eyebrows (Take part, Data sets, About EHS, Health
  topics), group titles (Real Time Data, Who we are, Strategies, Quality and policies),
  side headings (Contact and policies, Policies and plans, More about EHS, More topics),
  every one-line description, and feature cards (Contact the Director General, Bayanat.ae,
  Careers, Blood Donation). Open Data descriptions reuse the approved deck sub-lines.
  Media Center has no side column (3 links). Awareness Center panel is shifted left to
  stay inside the page.

## Services Directory
- Filter sidebar: Type, Gender, Age Group and Health Condition groups each use an
  Aegov-Label for the heading; options are Aegov-Checkbox instances; Age Group and Health
  Condition use Aegov-Select.
- Service cards use Card Pattern (Property 1 = Service card). The last 4 cards (General
  Dentistry, Inpatient Services, Issue of a Birth Certificate, Issue of a Health Card)
  still need their real text.
- v2 (2026-11-23, built, awaiting approval): `EHS / Services Directory / Desktop / EN
  (v2)` 214:5529, a copy of V1 72:3605 (V1 untouched).
  - Banner: `sub-page-banner` Layout=Search (new variant): left-aligned breadcrumb Home /
    Services / Services Directory, H1, no subtitle (none live), "Search a service" field;
    the toolbar search is hidden.
  - 8 live category tabs (All Services selected; the row is wider than the page, as live).
  - `Container / Filter panel` (white box, 336 wide, same shadow as the Home panels):
    approved filter groups + "Clear all" [new label]; Age Group heading fixed to the live
    "Age Group" (V1 read "Age Group Label").
  - List view active; `Container / Results panel` with the 12 live page-1 services as
    `Pattern / Service row`: live durations; fee and audience shortened = [new wording]
    for approval (Fee by case level, From 250 AED, Free for UAE locals with a health card,
    Free with a valid health card, Case by case, 65 AED, From 20 AED; Investors and
    businesses, Residents 18 and above, Parents of newborns, ...). Card grid kept, hidden.
  - Pagination: live 1-4, page 1 current, Previous disabled.
  - Not changed (from V1): header, feedback panel, footer (footer still shows sample
    text such as "Entity name" and info@entity.gov.ae).
- v3 (2026-11-23, built, awaiting approval): `EHS / Services Directory / Desktop / EN
  (v3 top filters)` 228:6126, a copy of v2 (v2 untouched). The user chose banner option 3
  and layout option A (top filter bar, no sidebar, full-width results).
  - Banner: `sub-page-banner` Layout=Centered Search: centred breadcrumb Home / Services /
    Services Directory, H1, no subtitle (none live, layer hidden), "Search a service",
    "Most used:" + 3 live Most used services as Aegov-Checkbox-Pill (Issue of a Health
    Card, Communicable disease service, Issue of a Birth Certificate), aurora background.
  - `Container / Filter bar` 228:7171 (aeblack/50 fill, aeblack/200 stroke, radius-2xl,
    padding spacing-4 / spacing-6): Type, Gender, Age Group, Health Condition, each an
    Aegov-Label + Aegov-Select (Type and Gender show "All" = [new] placeholder; Age Group
    "I am a" and Health Condition "I am feeling" live), "Clear all" [new], list/grid
    toggle on the right (grid active, as live). Old sidebar and toolbar hidden.
  - Results: 12 live page-1 services as `Card Pattern` Service card in a 3 x 4 grid at
    full width, titles and descriptions truncated at 2 lines; list panel and old grid
    hidden. Pagination unchanged.
  - States frame `EHS / Services Directory / Filter bar states (v3)` 230:5726: Type
    dropdown open (`Container / Filter dropdown (Type)` 230:5789, white, aeblack/200
    stroke, radius-xl, shadow-xl, 9 live Aegov-Checkbox, Patient checked) and the
    active-filter pills row (Aegov-Checkbox-Pill Checked + Clear all).
  - Card details: a duration / fee / audience `meta` row was tried on the v3 cards and
    REMOVED the same day at the user's request (it did not fit the card). Cards show
    title, 2-line description and Start Service only; cards in a row share the tallest
    card's height. Details stay in the list view (Service rows).
  - Open: filter bar and dropdown not yet saved as `Pattern / ...` (after approval);
    selects are single-select components shown for multi-select Type/Gender (no
    multi-select in the library); search still shows the mic icon.

- v4 (2026-11-23, built, awaiting approval): `EHS / Services Directory / Desktop / EN
  (v4 side filter)` 237:5850, a copy of v3 (v3 untouched). The user preferred a side
  filter over the v3 top bar (felt crowded) and chose the collapsible option.
  - Banner and category tabs as v3 (tabs show Style=simple, as found in v3).
  - `Container / Filter panel (collapsible)` 237:6778 (same box as v2's filter panel):
    "Filter" heading + Clear all [new], then 4 groups separated by an aeblack/200 top
    border. Each group header is a library Aegov-Accordion-Item (Heading = live group
    name, Divider off, content text hidden); the options sit under it because the item's
    content is text only. Type expanded: first 5 live options + "Show all (9)" [new
    label] (the other 4 are hidden in this default state, not dropped). Gender, Age Group
    and Health Condition collapsed (their checkboxes / selects are kept, hidden).
    Long labels wrap.
  - Results: list view active, the 12 live Service rows with duration / fee / audience
    (as v2); the v3 card grid and top filter bar are hidden. Pagination unchanged.
  - Prototype (2026-11-23, user's OK): the 4 groups are now instances of the interactive
    `Pattern / Filter group / ...` sets (Type starts Expanded, others Collapsed); click a
    header to open/close, "Show all (9)" opens all 9 Type options. Static groups kept,
    hidden. Flow starting point "Services Directory v4 (side filter)" added on the page.
  - Open: a selected-state frame (counts in headers, chips) not built; no "Show less".

## Service detail template
- Template for all service detail pages. Layout: NEW (not the 3.0 layout).
- No sub-page banner on this template. Breadcrumb, title and actions sit at the top of
  the body.
- Key facts (duration, service type, sub service type, target audience) go in an
  Aegov-Bento-Grid; this changes the order from the live page and is approved.
- Service Process uses Aegov-Timeline (vertical); FAQ uses Aegov-Accordion.
- Not designed (listed in the outline as "not designed"): chat launcher, sign-language
  launcher, survey / customer pulse widget.
- Typos in source text stay as live text until the user approves fixes (list in the
  outline).
- v3 redesign (2026-11-23, built, awaiting approval): `EHS / Service Detail / Desktop / EN
  (v3 summary card)` 245:6771, a copy of 93:3580 (untouched). New layout, live content
  of Child Health and Vaccinations only. Inspiration: the user's "appointment card"
  screenshot (eyebrow pill, status badge, title, date tile, dark panel), mapped to live
  content; floating elements left out.
  - Hero: aurora background (same glow as the banner), breadcrumb, badges Social /
    Variation (the leftover "Governmental facilities: Free" badge, not live for this
    service, is hidden), H1, intro, actions row under the intro (Start Service first, then
    share / print / download).
  - `Container / Service summary card` (white, aeblack/200 stroke, radius-2xl,
    shadow-xl, 600 wide): Service channels label + 4 badges; Target audience label +
    aegreen badge with the live fee; audience as title; Service Limitations line;
    `Container / Duration row` (tile "30 / mins", "Service completion duration", live
    timings line); `Container / Process preview` (primary/700, 4 numbered dots, first
    step text, "4 steps" = [new]).
  - Body: `Container / On this page` (vertical Aegov-Tab, Style=simple, 6 live section
    names; sticky in build) + main column: Service Process as 4 `Container / Step card`
    (aeblack/50, radius-2xl, equal height); `Container / Before you go panel`
    (aeblack/50) with Conditions & Requirements (CheckCircle icons) and a white
    `Container / Required Documents` box (FileText icons); Service locations with 6
    emirate pill tabs and `Container / Location chip` (MapPin) for all 54 live centres
    (Dubai shown, other emirates hidden per tab), timings line + Health Care Facilities
    link; FAQ's (5 live Aegov-Accordion-Items, first open) beside `Container / Help panel`
    (primary/600, EnvelopeSimple, live heading, "Click here to email us" button);
    Related Services moved in unchanged. Old key facts and columns hidden.
  - Declutter pass (user: "too much text in one area"): the summary card keeps only
    Target audience + title, the duration tile with the fee badge, and the Process
    preview dots ("4 steps"). Moved out, nothing dropped: Service channels = one Body SM
    line under the hero actions; Service Limitations = first row of Conditions &
    Requirements; the timings sentence stays under Service locations (hidden in the
    card); step 1 text hidden in the dark panel. FAQs all start collapsed; main column
    gap spacing-16; Before you go panel padding spacing-12; On this page tabs Size=sm.
  - User's own cleanup (2026-11-23): Start Service + share/print/download moved into the
    summary card, Process preview removed, On this page = floating card on the right,
    content in one white panel, Conditions and Required Documents stacked, Help panel
    under the FAQs.
  - Service Process (user's request): horizontal library Aegov-Timeline 253:7502
    (Style=default, Size=lg), 4 steps with the full live step text as Label, Description
    off, every step Status=active (no fake progress), all connectors dashed, steps fill
    the width equally (280 each). Step cards row hidden, not deleted.
  - Rule from the user: Clip content OFF on every auto-layout frame I create.
  - Replaces two approved decisions for this version (key facts in a bento grid,
    vertical Aegov-Timeline) - to be confirmed by the user.
  - Open: the moved `section/Related Services` frame has an unbound white fill (from the
    original); prototype (tabs, accordion, nav) not wired; reference screenshot not yet
    saved to the inspiration library (after approval).
