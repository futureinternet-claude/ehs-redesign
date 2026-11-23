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
  - Approved 2026-11-23 on `Check Ups (v2 open data)` 189:5075. Not done: left-column
    icons still Prevention ones (suggested ChartBar / Pulse / ChatCircleText); icons of
    the cards behind the top card not swapped.
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
- Our Updates (2026-11-23, built, awaiting approval): `Our Updates (v2 news)` 201:5499 in
  Home v2, old 162:19468 hidden. Pattern `news-carousel-image-cards` (user's ref).
  Eyebrow "Media Center" (live menu name, uppercase via text case), H2 "Our Updates"
  (live), no lede; "View all" outline button + arrows on the right; live tabs News /
  Events / E-Consultations kept; 4 live news as `Card Pattern` = News card v2 (3 full + a
  peek). Live dates corrected (03 Nov, 21 Oct, 16 Oct, 05 Oct 2026). Old News card
  variant kept for Home v1 and the 1920 Sample.
  - Open: 4th card image (Global Patient Safety Award 2026) not captured, grey
    placeholder; Events and E-Consultations tab content not designed.
- Health Care Facilities: selectable list on the left (name and location), map on the
  right with the details card inside it (type, full hours, location, Directions and Call
  buttons, View Details). Open: captured map image, each centre's coordinates, phone
  numbers and map links (not on the live cards).
- Facility Type is shown as label + Aegov-Badge so the live text is preserved.
- Details-on-map card is fixed at the bottom-left of the map (not anchored to the pin);
  the left selector shows only name + location; actions live in the details card.

## Services Directory
- Filter sidebar: Type, Gender, Age Group and Health Condition groups each use an
  Aegov-Label for the heading; options are Aegov-Checkbox instances; Age Group and Health
  Condition use Aegov-Select.
- Service cards use Card Pattern (Property 1 = Service card). The last 4 cards (General
  Dentistry, Inpatient Services, Issue of a Birth Certificate, Issue of a Health Card)
  still need their real text.

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
