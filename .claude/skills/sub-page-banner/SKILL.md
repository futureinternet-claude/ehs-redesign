---
name: sub-page-banner
description: How to use the EHS local page-banner component (sub-page-banner, id 97:26409) on every EHS sub-page - properties, breadcrumb, missing subtitle, placement, height, background. Use when building any EHS page except Home and the Service detail template.
---

# EHS page banner (all sub-pages; Home and Service detail excluded)

The banner is a LOCAL COMPONENT. Use an instance of it on every sub-page; never rebuild
it, copy the frames, or detach it.
- Component: `sub-page-banner` (id 97:26409), on the "Local Components" page of the
  working file. The Services Directory frame uses an instance (1536 wide).
- Exposed properties: `Page Title` and `Page Subtitle` (text properties) and `Content` (a
  slot that holds the H1 and the subtitle). Set the two text properties from the live H1
  and live subtitle or intro line (Arabic: the real Arabic text, never invented). Do not
  add anything to the `Content` slot unless asked.
- Breadcrumb is inside the component: a `Breadcrumb` frame with 4 nested
  Aegov-Breadcrumb-Item instances (Home, then each parent, last item State=Current, all
  Separator=Slash). Sample labels are Home / Services / Services / Services Directory;
  override every item's `Label` text from the live page, and keep State=Current on the
  last visible item (earlier ones State=Link). If a page has fewer levels (2 or 3), hide
  the unused items (hide only; never delete or detach), put State=Current on the last
  visible item, and check the separators. More than 4 levels: stop and ask.
- If the live page has no subtitle, do not leave "This is subtitle": hide the
  `Sub title (2XL)` layer in the instance, check the banner, and tell the user.
- Placement: first element of the page body, directly below the Header (and the Alert
  when shown). Full width (Fill / 1536 at Desktop), no extra wrapper, padding or radius.
- Structure, for reference only (do not edit): vertical auto-layout, width 1536 fixed,
  height Hug, padding 80 / 24 / 80 / 24, item spacing 20; children `Breadcrumb` (frame,
  Fill width, 24 high) and `Content` (slot, Fill width, vertical, spacing 20) holding
  `Page title (H1)` and `Sub title (2XL)`. Background is the component's own gradient
  fill.
- Height: hugs content; expected about 310 at Desktop with a one-line title and subtitle
  (the master measured 270 on 2026-11-23). If a long title or subtitle makes it taller,
  tell the user; do not fix by hand. The Services Directory instance measured 396: confirm
  it is not carrying extra content.
- Background: keep the component's gradient fill. Do NOT use `assets/sub-page-bg.jpg`
  (2976 x 616) until the user says so; do not change the component or swap the background
  in an instance.
- Do not edit the component unless asked. A new property or variant (Tablet, Mobile,
  Arabic RTL) needs the user's OK first, with a proposal.
- Text contrast on the background must meet WCAG AA (in the EHSblue mode); if it fails,
  tell the user rather than changing the colour.
- Tablet (768) and Mobile (375), only when asked, reuse `assets/sub-page-bg.jpg`; size,
  padding and type sizes are decided at that step and shown to the user first.
