# Child Health and Vaccinations (service detail) - content outline

Source: https://www.ehs.gov.ae/en/services/services-directory/child-health-and-vaccinations
Screenshot: `references/child-health-and-vaccinations/full.png` (1536 wide, full page). Arabic not captured.
Template: Service detail (no sub-page banner). Same template as `references/service-detail.md`.
Captured 2026-11-20. FAQ answers read by expanding every item (only item 1 is open by default).

## Global (not page body)
- Header (library instance), alert strip (same global alert as the template; copy text from the existing frame), Footer (library instance). Phone 171 (tel:171), Toll free 800 8877 (tel:8008877).
- Not designed: chat launcher, sign-language launcher, customer pulse / survey widget (the on-page "Give us your feedback" button IS designed, only the widget it opens is not).

## Sections (live order)
1. Breadcrumb: Home > Services > Services Directory > Child Health and Vaccinations (current). Links: en/home, en/services, en/services/services-directory.
2. Title row: H1 "Child Health and Vaccinations" + 3 icon buttons: Share (addtoany), Print (javascript), Download (PDF handler id=29312).
3. Primary action: [Start Service] button, top of page (https://patient.ehs.gov.ae/FE/Login.aspx?OriginalURL=...ServiceCardId=3). NEW vs the radiation page, which had none.
4. Intro: "This service enables children to obtain periodic health assessments including physical examination, growth and developmental assessments, age-specific screening and the mandated vaccinations by the National Immunization Program"
5. Service Process (4 numbered steps, vertical):
   1. Log in using UAEPASS
   2. Book a new appointment
   3. Arrive at the center 20 minutes before the appointment.
   4. Evaluate and diagnose the case by the treating physician and Perform the necessary laboratory tests and examinations as needed.
6. Conditions & Requirements (4 bullets):
   - A Health Card is not required for vaccination.
   - Vaccination is not associated with the patient's location of residence or the issuing location of residence.
   - In case the child's Valid Emirates ID or Valid Passport is not available, then a copy of the official birth notification or birth certificate and ID/passport of the guardian are required
   - Previous immunization card if applicable
7. FAQ's (accordion, 5 items, item 1 open by default):
   1. Q: Where can I issue a vaccination card for children below 5 years of age?
      A: The digital vaccination cared is available on EHS App.
   2. Q: Do I need to obtain the service according to the residential health center?
      A: No, you can obtain the service and make an appointment at the nearest health center.
   3. Q: What are the fees for obtaining the service?
      A: Vaccination service and medical consultation for the purpose of vaccination are provided free of charge for children under the age of five according to the National Immunization Program.
   4. Q: Is health insurance required to obtain the service?
      A: No, it is not required as vaccination service and medical consultation for the purpose of vaccination are provided free of charge for children under the age of five according to the National Immunization Program.
   5. Q: Does the service require a valid health card?
      A: The service does not require issuing a health card.
8. Info rows (label left, value right), in live order:
   - Service completion duration: 30 mins
   - Service Fees: Free of charge for children below the age of five
   - Service channels: Service Delivery Centers; Call Center; EHS Website; EHS Application
   - Target audience: Children up to 5 years ( all nationalities )
   - Service Limitations: Children up to 5 years ( all nationalities )
   - Service Provision Timings: "According to the working hours of the primary healthcare centers, which are available at: Health Care Facilities" (link: https://www.ehs.gov.ae/en/services/health-care-facilities)
   - Service Type: Social
   - Sub Service Type: Variation
9. Sidebar: Required Documents (2 bullets): Valid Emirates ID; Valid Passport.
10. Sidebar: Service locations, grouped by emirate (54 centers, plain text, no links; counted from the capture: 3+17+5+4+14+11):
    - Dubai (3): Al Aweer Health Center; Al Muhaisnah Health Center; Al Ittidad Health Center
    - Sharjah (17): Al Riqqa; Al Batayieh; Al Dhaid; Dibba Alhosn; Family Health Promotion Center; Al Hamryeh; Kalba; Al Khalidiyah; Khorfakkan; Almadam; Al Melieha; Nazwa; Al Rifaa; Al Thameed; Wadi Al Helow; Nahwa; Shees (each followed by "Health Center" except Family Health Promotion Center)
    - Ajman (5): Al Hamidyia; Al Madina; Al Manama; Mushairef; Muzairea (each "Health Center")
    - Umm Al Quwain (4): Al Salama; Al Rafa; Falaj Almualla; Al Khazan (each "Health Center")
    - Ras Al Khaimah (14): Al Hemrania; Al Jeer; Julphar; Al Jazeerah; Khat; Wadi Esfini; Shawka; Saif Bin Ali; Al Rams; Ras Alkhaimah; Al Mairid; Al Manaie; Abdullah Al Sharhan (Aldhait); Kedra (each "Health Center")
    - Fujairah (11): Al Bidiya; Dhadnah; Al Faseel; Al Halah; Al Khalibia; Murbah; Qidfaa; Al Qurrayah; Al Siji; Al Twayeen; Wadi Seder (each "Health Center")
    (Names above drop the repeated "Health Center" suffix only to save space here. Build each as the full live text, e.g. "Al Aweer Health Center", "Family Health Promotion Center".)
11. Sidebar: "For assistance, get in touch through": "Click here to email us" (mailto:cen.pmd@ehs.gov.ae). No phone line on this page (the radiation page had Call 800 8877).
12. Related Services (1 card): "Preventive Vaccinations" - "This service provides comprehensive vaccination for individualos and the community against infectious diseases, in accordance with the latest national and international recommendations and standards (World Health Organization). The service includes:" then 4 bullets: Routine Vaccinations for Adults and Senior Citizens; Traveler Vaccinations; Pre-employment Vaccinations; Vaccinations for Residence Permits and Immigration Visas. Link: [Start Service] (en/services/services-directory/preventive-vaccinations is the card link; the card's own Start Service goes to the patient portal URL above, confirm when building).
13. Feedback band: "Do you think this content is helpful?" [Yes] [No] | "Have you used our services at our service center or digitally recently?" [Give us your feedback]

## Differences from the radiation page (already built in the frame)
- Process: 4 steps (was 7). Conditions: 4 bullets (was 2). FAQ: 5 items (was 1).
- Fees is a single line (was a group with 6 bullets). Channels: 4 (was 2).
- Required documents: 2 (was 5). Locations: 54 centers in 6 emirates (was 1 section + email).
- Top-of-page Start Service button is new. Assistance block is email only (no Call).
- Related card has a 4-bullet list and a Start Service link.

## Typos to approve before fixing (kept as live text until approved)
- "vaccination cared" -> "vaccination card" (FAQ 1 answer)
- "individualos" -> "individuals" (Related Services)
- "Perform the necessary laboratory tests" (step 4): mid-sentence capital "Perform" -> "perform"
- "Children up to 5 years ( all nationalities )": spaces inside parentheses -> "(all nationalities)"
- "Al Hemrania" / "Ras Alkhaimah" spellings: leave as live.
