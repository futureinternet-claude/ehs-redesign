# Services Directory (Template 3) — content outline

URL: https://www.ehs.gov.ae/en/services/services-directory
Capture: 1536 wide, full page (3032 px tall) → `references/services-directory/full.png`
Page title: Services Directory | Services | Emirates Health Services - UAE

## IMPORTANT finding
There is **no "patient" tab** on this page. `#patient` in CLAUDE.md does not match the live page.
"Patient" is one of the **Type filter checkboxes**. The real tabs are 8 service-category tabs (below).
Default state: tab "All Services" active, no filter checked. **Confirmed by user: "All Services" is the default.**

## Approved decisions (apply to this page and all future pages, no need to ask again)
- **Excerpts:** card descriptions (service / news / blog / event cards) are excerpts. Use Figma's text truncation (max lines = 2) on the description text. Keep the full available text in the layer and let Figma truncate.
- **Start Service:** every service card shows "Start Service" as an Aegov-Link (button-link). Live shows it on only 8 of 12; design all 12 with it.
- **Other tabs:** not captured and not designed. They share the same layout as "All Services" (card grid + carousel arrows). Design the tab component once.
- **Pages 2-4 of pagination:** not designed. Page 1 only.
- **Filter sidebar:** left column ~280 px, card grid beside it.
- **Search field:** use Aegov-Input with the "icon end" and "action" slots toggled on, giving 2 icons at the end of the field (magnifier + the second icon). Voice/mic is NOT used as a separate feature.
- **Icons (list/grid toggle, arrows, thumbs, etc.):** do not draw. Use the Phosphor Icons (Community) library.
- **Not designed (listed as such):** chat launcher, sign-language launcher, "Rate the new design" link / "New Design" toggle, customer-pulse widgets.

## Top to bottom (default state)

1. **Header** (library Aegov-Header, reuse from Home). Live nav: Home, Services, Digital Participations, Open Data, About Us, Media Center, Awareness Center, AI. Actions: search, user, accessibility, favourites (star), language.
2. **Alert strip** (Aegov-Callout danger, reuse from Home), with prev / pause / next / close controls.
   "Alert: We would like to inform you that dental treatment services at Al-Salama Health Center are temporarily stopped due to maintenance work. Accordingly, dental services will be moved from Al-Salama Health Center to Al-Khazan Health Center."
3. **Breadcrumb**: Home / Services / Services Directory (current).
4. **Page banner**: dark blue panel, H1 "Services Directory" (centered, white).
5. **Tabs row** (8 tabs, scrolls horizontally; last ones clipped):
   All Services (active) · Most used · My Favorites · Health, prevention and periodic Screening · Primary Health Care Services · Specialized health care Servicess [sic] · Certificates and Medical Records · Customer service
6. **Toolbar (right of tabs)**: list-view icon, grid-view icon (grid active), search field "Search a service" (magnifier + microphone icon → voice dropped per Home decision).
7. **Filter sidebar** (left column), heading "Filter":
   - **Type** (9 checkboxes): Individual, Professional, Government sector / private sector, Student or Post Grad, Patient, POD, Business, Researchers, None
   - **Gender** (2 checkboxes): Male, Female
   - **Age Group**: dropdown, placeholder "I am a"; options Child, Teenager, Adult, Old
   - **Health Condition**: dropdown, placeholder "I am feeling"; options Chronic Diseases, I feel unwell, Accident/injury, Pregnant, Feeing well [sic]
8. **Service card grid**: 3 columns x 4 rows = **12 cards**, page 1 of 4. Each card: title (link, clamped to 2 lines), description (truncated with "..."), "Start Service →" link (only on some cards).
   | # | Title (full) | Description (as shown) | Start Service |
   |---|---|---|---|
   | 1 | Request Occupational Radiation Monitoring service | This service allows private and governmental facilities to m... | no |
   | 2 | Cancel Rental of Assets and Vacant Spaces | This service enables parties leasing spaces or assets belong... | no |
   | 3 | Child Health and Vaccinations | This service enables children to obtain periodic health asse... | yes |
   | 4 | Communicable disease service | This service provides comprehensive care through communic... | no |
   | 5 | e-Etmnan (Periodic Health Screening) | This service provides customers with a comprehensive periodi... | yes |
   | 6 | Emergency Services | This service enables patients of all age groups of the commu... | no |
   | 7 | Examination of Medical Fitness for Residency Visa | This service enables citizens to obtain a medical fitness ce... | yes |
   | 8 | Family Medicine Services | This services enables patients to have a comprehensive clini... | yes |
   | 9 | General Dentistry | The service allows customers to receive general dental treat... | yes |
   | 10 | Inpatient Services | This service provides patients of all age groups to obtain s... | no |
   | 11 | Issue of a Birth Certificate | This service enables parents to issue an official, certified... | yes |
   | 12 | Issue of a Health Card | This service enables patients to apply for a health card, wh... | yes |
   Descriptions: 2-line truncation via Figma text truncation. All 12 cards show "Start Service".
9. **Pagination**: Previous · 1 (active) · 2 · 3 · 4 · Next. Pages 2–4 of All Services are not rendered in the DOM (loaded on click); their content is not captured.
10. **Feedback panel** (two columns):
    - Left: "Do you think this content is helpful?" + buttons "Yes" (thumbs up), "No" (thumbs down)
    - Right: "Have you used our services at our service center or digitally recently?" + button "Give us your feedback"
11. **Footer** (library Aegov-Footer, reuse from Home). Live: About this website (Privacy Policy, Disclaimer, Copyright, Terms & Conditions, Digital Accessibility Statement); Awareness Center (Gamification, Blood Donation, Procurement); Information and support (FAQs, Contact Us, Sitemap, Help & Accessibility); Quicklinks (Careers, UAE Government Charter, Archive, Glossary, Abbreviations); Tawasul 171, Toll free 800 8877; "© 2026 EHS. All rights reserved. Last updated on 15/11/2026 05:56 PM"; Follow us on: Facebook, Instagram, LinkedIn, X, YouTube, Telegram.

## Other tabs (NOT captured, NOT designed: same layout as All Services; titles below are for reference only)
- **Most used** (≥8 cards, carousel with Previous/Next): Issue of a Health Card; Communicable disease service; Issue of a Replacement for Lost Death Certificate; Issue of a Birth Certificate; Cancel Rental of Assets and Vacant Spaces; Renew Rental of Assets and Vacant Spaces; and others.
- **My Favorites**: personalised / empty until the user favourites services (content not captured; login-dependent).
- **Health, prevention and periodic Screening** (~8): Request Occupational Radiation Monitoring service; Child Health and Vaccinations; Communicable disease service; e-Etmnan; Examination of Medical Fitness for Residency Visa; Pre-Employment Medical Examination; Premarital Screening and counseling; Pre-University Fitness Screening; Preventive Vaccinations; Request for Technical Consultation and Measurements in Radiation Safety.
- **Primary Health Care Services** (3): Family Medicine Services; General Dentistry; Non-communicable Disease Clinic.
- **Specialized health care Servicess** (5): Emergency Services; Inpatient Services; Mental Health Services; Outpatient Specialized Clinics Services; Request for Provision of Blood Units and Components; Specialized Dental Services.
- **Certificates and Medical Records** (~10): Issue of a Birth Certificate; Issue of a Health Card; Replacement for Lost Birth Certificate; Replacement for Lost Death Certificate; Issue of Age Estimation Certificate; Authenticated Copy of Birth Certificate; Authenticated Copy of Death Certificate; Issue of Death Certificate; Modification of Birth Certificate Details; Renew of a Health Card; Request for a Medical Report.
- **Customer service** (5): Request to Appeal Against the Decision of Medical Liability Committee; Submit Complaints and Feedback; Submit Inquiries; Submit Medical Complaints; Submit Suggestions.
  (Tab panes also render Previous/Next carousel arrows.)

## Not designed (third-party overlays)
- Floating chat launcher, sign-language launcher (right edge of the page)
- "Rate the new design" feedback link and "New Design" toggle (site-level, in header area)
- Customer-pulse / feedback widgets

## Item counts
Tabs 8 · Type checkboxes 9 · Gender checkboxes 2 · dropdowns 2 · cards on page 1: 12 · pagination pages 4 · footer link columns 4 · social icons 6
