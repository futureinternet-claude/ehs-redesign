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
- Latest Initiatives: image-led cards in 4 columns (`Pattern / Initiative image card`).
- Prevention check-ups (new section, not on the live site), placed after Latest
  Initiatives: stacked deck, state 1 of 4 shown (card 1 on top, two plain cards behind).
  Content comes from the user's brief. Open: clinical sign-off on ages and intervals, CTA
  link target, Arabic copy, card 4 meta text ("Ask your doctor").
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
