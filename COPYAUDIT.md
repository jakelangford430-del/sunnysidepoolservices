# Sunnyside Pool Services copy audit

Original audit: 6 August 2026
Last updated: 18 August 2026 (2)

## Evidence standard

Website copy is limited to:

- facts published on Sunnyside's existing website or Google Business Profile;
- facts supplied directly by Sunnyside for this rebuild; or
- technical guidance supported by an official health or manufacturer source.

Marketing language must not imply a rating, customer consensus, qualification, guarantee or service area that has not been evidenced.

## Verified

Source: https://www.sunnysidepoolservices.com.au/ and Sunnyside's Google Business Profile

- Business name: Sunnyside Pool Services
- Business history: founded in 2018
- Phone: 0437 283 972
- Email: info@sunnysidepoolservices.com.au
- Published services: regular maintenance, green pool recovery and pool renovations
- Regular maintenance scope: cleaning, water balancing and equipment checks
- Green pool recovery scope: algae treatment, filtration setup and water balancing
- Renovation scope: resurfacing, repairs and pool makeovers
- Customer reviews: six reproduced verbatim and in full from Google on Home, captured 8 August 2026 — Dhanushka Sigera, Mina Salib, Daphne Whiteside, Conner Maitland, Fale Talaepa, Karl Fisher. A seventh, David hug, is featured on the Services page from 12 August 2026; see the truncation note below.
- Google rating: 5.0 from 20 reviews, confirmed on the Google Business Profile 8 August 2026
- Google Business Profile: https://share.google/x0TZIAeJNAugILFP8
- Google category: Swimming pool contractor
- Service area, per the Google profile map: Perth, Joondalup, Ellenbrook, Fremantle, Rockingham, Mandurah

## Supplied directly by Sunnyside

Provided for the rebuild, not independently confirmed on a public source:

- Founded by Daniel
- 60+ regular pool cleans for ongoing clients
- Equipment repair and assessment services
- Fibreglass renovation services
- Testing technology used to read water chemistry, filtration, circulation and equipment condition
- Phone-first enquiries. An online enquiry form was added to the Contact page on 13 August 2026 (see "Changes made 13 August 2026" below); phone and email remain the two channels named directly in copy
- One-off jobs and one-off cleans offered alongside regular servicing
- Attendance not required; pool-area access can be arranged by lock box or similar
- Invoiced after the work, payable within 7 days
- Fully insured
- Chemicals supplied by Sunnyside

## Technical sources

- HealthyWA, Swimming pools and spas: https://www.healthywa.health.wa.gov.au/en/Articles/S_T/Swimming-pools-and-spas
- AstralPool Australia, Weekly pool maintenance: https://www.astralpool.com.au/pool-and-spa-guides/weekly-maintenance
- AstralPool Australia, Why is my pool green?: https://www.astralpool.com.au/pool-and-spa-guides/why-is-my-pool-green
- AstralPool robotic cleaner operating instructions: https://www.astralpool.com.au/files/products/manuals/RF%20Manual_0.pdf

## Unsupported copy removed or corrected

- Removed the unverified `5.0` rating and review count from visible copy and LocalBusiness schema.
- Removed statements presented as broad customer sentiment. Real Google reviews now carry that job.
- Changed `Top 10` to a knowledge-hub framing because no search-volume evidence established a ranked top ten.
- Removed the unsupported `24 to 72 hours` green-pool recovery timeframe.
- Corrected water testing from weekly to HealthyWA's at-least-daily guidance.
- Corrected pH and outdoor stabilised-pool chlorine guidance to HealthyWA ranges.
- Removed `proven`, `expert`, `specialist` and `trusted` claims in favour of specific, checkable statements.
- Removed the Alice C. quote — sourced only to the old website, superseded by the dated Google reviews.

## Changes made 18 August 2026 (2)

- **Logo replaced with owner-supplied vector artwork, approved 18 August 2026.** The owner supplied a new master (PNG preview + a genuine vector PDF, unlike the earlier flattened `sunnyside-logo-web.png`) that fixes the uneven letter-heights in the "Sunny" cursive noted earlier the same day. Extracted the vector at high resolution, removed its baked-in white background programmatically (connected-component analysis to key out the background rectangle without disturbing the artwork's own anti-aliased edges), and produced two exports:
  - `assets/sunnyside-logo.png` — the navy-on-transparent version, used only in the `LocalBusiness` schema's `logo` field (not visible on-page).
  - `assets/sunnyside-logo-reversed.png` / `.webp` — a white-on-navy version for the header and footer, built the same way as the previous reversed logo: sun and wave keep their real colours, the wordmark and "POOL SERVICES" are recoloured solid white (again via connected-component masking, so the sun/wave colours were untouched).
  - Updated every page's `width`/`height` attributes on the logo `<img>` (480×156 → 480×244) to match the new artwork's actual aspect ratio, since the new file is proportioned differently from the old one.
  - Old logo files are not kept in the repo as a backup; git history covers rollback if ever needed.

## Changes made 18 August 2026 (1)

- **Nav label "Knowledge hub" shortened to "Advice"**, matching the existing `pool-advice.html` URL and page title so the nav catches up to wording already used elsewhere on the site. No new terminology introduced.
- **Footer redesigned to a single minimal row**, replacing the three-column footer (brand/tagline, an "Explore" link list, an email-only "Get in touch" column, and a bottom row with copyright, ABN and a marketing signature). The new footer is: logo + social icons (phone, Instagram, Facebook) on the left, a single "All pages →" link on the right, and copyright + ABN on a small second line. Chosen at the owner's direction to reduce footer clutter and push the full link list onto a dedicated page instead, for search-console/crawlability reasons.
- **New page: `all-pages.html`.** A single flat page — no design flourish — listing the five main pages, then all 44 service-area pages grouped A–Z. It exists so every URL on the site is reachable within one click from every other page (via the footer), which gives Google Search Console and any crawler a direct, un-nested path to every location page regardless of how deep `locations.html`'s own grouping sits. Added to `sitemap.xml`.
- **`thanks.html` (the Netlify form confirmation page) brought up to date.** It had been missed in the 17 August changes — still had the old three-column footer, the plain-text phone number, the removed mobile call-dock, and no Areas nav link. All four are now consistent with the rest of the site.

## Changes made 17 August 2026 (3)

- **Mobile call dock removed sitewide.** The fixed yellow "Call or SMS Sunnyside" bar that sat at the bottom of the screen on mobile is gone from every page. In its place, the header's call button (previously hidden on mobile to avoid duplicating the dock) is now always visible, restyled as a circular "Call us" button next to the mobile menu control — the header is `position: sticky`, so it stays on screen through the scroll the same way the dock did. No facts changed, layout/UI only.
- **Footer phone number replaced with an icon.** The plain-text "0437 283 972" link in the footer brand column is gone; a phone-emoji icon now sits at the front of the footer's social-icon row (before Instagram and Facebook), linking to the same `tel:` number. Same number, same destination, different presentation.

## Changes made 17 August 2026 (2)

- **"Areas we service" reframed as "Our regular service areas".** The owner's intent for the hub and location pages is primarily SEO — appearing in searches like "pool cleaning Applecross" — rather than implying the 44 listed suburbs are the only places Sunnyside will go. Hero, headings, footer links, the contact-page reference, and the `BreadcrumbList` schema name across all 44 location pages now read "Our regular service areas", and the hub's intro copy states the run covers those suburbs weekly while Sunnyside remains happy to service anywhere in the Perth metro area.
- **"Nearby areas" links now geographic, not alphabetical.** Each location page's "Areas near {suburb} we also service" list previously showed the next few suburbs alphabetically. It's now computed from approximate suburb-centre coordinates (public geographic knowledge, not survey-grade) via straight-line distance, aiming for suburbs within roughly 10–15km and falling back to the nearest few if a suburb has fewer neighbours in range. This is a navigational aid, not a claim requiring the evidence standard applied to marketing copy.
- **Suburb-page closing CTA changed.** "Need a hand with your pool in {suburb}?" is now "Want us to let you know when we're in {suburb}?", pointing at the existing "take your details and add you to our database" mechanism already used on the Contact page rather than a new feature. The supporting line was rewritten to "Or leave your details · Servicing Perth pools since 2018, fully insured." — same verified facts (since 2018, fully insured), fresher wording. This change applies only to the 44 location pages; the Home/Services/Contact final-CTA sections, which don't reference a suburb, were left as they were.

## Changes made 17 August 2026 (1)

- **Service area expanded from 6 named cities to 44 suburbs, supplied directly by the owner.** The owner provided a list of 38 additional suburbs and confirmed Sunnyside currently services all of them, superseding the 8 August decision to narrow visible copy and `areaServed` to only the six areas shown on the Google Business Profile map. The Google profile itself has not been updated to show this wider polygon — this expansion rests on the owner's direct statement, not on independent verification against the profile or another public source.
- **Location pages added.** A `locations.html` hub page and 44 individual suburb pages (`locations/<suburb>.html`) were built, one per serviced suburb (the original 6 plus the 38 supplied). Per the owner's direction, these are deliberately templated rather than carrying suburb-specific detail — each page repeats the same service list, trust points and Google rating, with only the suburb name and internal links varying. No suburb-specific claims (bore water, local landmarks, streets worked on) have been invented; none should be added without the owner supplying the specific fact.
- **`areaServed` schema widened sitewide** on `index.html`, `services.html`, `contact.html`, `pool-advice.html`, `locations.html` and every location page to list all 44 suburbs, replacing the 6-city list.
- **Contact page's static 6-suburb pill list replaced** with a link to the new `locations.html` hub, so the visible area list doesn't need separate maintenance as suburbs are added or removed.
- **Nav and footer updated** across all pages to add an "Areas" link to `locations.html`.
- Sitemap updated with the hub page and all 44 location page URLs.

## Changes made 13 August 2026

- **Contact-page enquiry form added, superseding the earlier "no enquiry form" decision.** The 6/12 August entries recorded phone-first enquiries with no form, supplied directly by Sunnyside. The site owner has now asked for one, so a Netlify Forms-powered message form (name, email, phone, suburb, topic, message) was added to the Contact page, submitting to a new `thanks.html` confirmation page. No new factual claims were introduced — the form copy states only that Daniel receives and replies to messages himself, consistent with the owner-operated framing already used elsewhere on the site. No response-time promise is made, since none has been confirmed.
- **Contact-page phone repetition reduced.** Before this change, the Contact page carried three separate large "Call Daniel" buttons in the content flow (hero, phone card, closing section) in addition to the header pill and mobile call dock. The closing section's button now points to the new message form instead of duplicating the hero button, with the phone number kept as a plain-text link in the same section. The hero button gained a small secondary link to the form. Phone remains the first-listed, fastest-described channel in the "How to reach us" section.

## Changes made 8 August 2026

- **Service area set to match the Google Business Profile.** Copy and `areaServed` now name the six places the profile's map covers, rather than claiming the state. Site and profile agree, which is what Google ranks local results on.
- **Out-of-area enquiries welcomed explicitly.** The Contact page says Daniel is happy to talk it through, take details and add them to the database — so the narrower area reads as honest rather than as a closed door.
- **`60+` reworded** from "regular cleans every month" to "60+ regular pool cleans for ongoing clients". The monthly framing is no longer used.
- **Review count is deliberately not displayed** in visible copy. It is present in `aggregateRating` schema, which requires it, and is public on the Google profile regardless.
- **Rating published.** 5.0 shown in the proof bar on Home, Services and Contact, linked to the Google profile so a visitor can check it. `aggregateRating` (5.0 / 20) added to LocalBusiness schema on all four pages, with the profile as `sameAs`.
- **Reviews on Home are quoted in full only.** Reviews truncated by Google's "…More" link were left out rather than clipped mid-sentence or completed by guesswork.
- **Exception, 12 August 2026 — David hug on the Services page.** This review was recorded on 8 August as one of the seven truncated by Google's "…More" link. The owner supplied its text on 12 August and directed it be featured; the text supplied matches the truncated portion recorded earlier and ends on the problem, before any outcome. It could not be checked against Google, which is unreachable from the build environment. The Services provenance line therefore reads "From our Google Business Profile, captured 12 August 2026" and deliberately does **not** carry the "quoted in full" claim used on Home. If the remainder is retrieved, it should be appended and the wording aligned.

## Resolved: service area

The site previously claimed Western Australia while the Google Business Profile drew a Perth metro plus Peel polygon. Resolved 8 August 2026 by narrowing the site to match the profile.

Visible copy and `areaServed` now name Perth, Joondalup, Ellenbrook, Fremantle, Rockingham and Mandurah. The Contact page lists them and invites out-of-area callers to have their details taken for the database.

One deliberate exception: `contactPoint.areaServed` on the Contact page stays `AU-WA`. The service run is metro; who Daniel will *talk to* is not.

## Still outstanding

- **Before/after photography.** None exists. The module is not built until real matched pairs are supplied.
- **Certifications, licences, insurance.** None evidenced. No trust badges are shown.
- **Gallery photography.** No photographs of completed Sunnyside work are available.
- Truncated Google reviews (Stefunia G, Ebony H, Kate Baxter, Rebecca Lamont, conno749, K P) can be added once supplied complete. **David hug** is now featured on the Services page from the truncated text the owner supplied on 12 August 2026 — the remainder is still outstanding and should be appended if retrieved.
- **Chemicals: included or billed?** The site says Sunnyside supplies them, which is what Daniel confirmed. It does not say whether the cost sits inside the service price or on top, because that was not stated. Competitors publish "+ chemicals", so customers will ask.
- **Damage during a service.** No answer yet on what happens if something breaks while Sunnyside is working on a pool. Insurance is confirmed, the process is not.
- **Pricing.** Still unpublished. The single most-asked question on a phone-only site.
- **Opening hours.** The Google profile shows "Opens 7am Mon" but the full week was not captured. Supply the trading hours and `openingHoursSpecification` can be added to the schema.

## Image sources

- Hero and equipment photographs were generated for this rebuild and depict representative settings, not completed Sunnyside projects.
- The two residential pool photographs on the services page (`assets/pools/everyday-perth-pool-*`, `assets/pools/routine-pool-maintenance-*`) are the same category: generated for this rebuild, not photographs of Sunnyside jobs.
- **12 August 2026 — on-page note removed at the owner's direction.** These photographs previously carried the line "Photographs shown are representative Perth pool settings, not photographs of completed Sunnyside work." The owner directed its removal with the images staying in place. Before the change was made, the position was put to the owner that presenting generated imagery without a qualifier on a services page risks being a misleading representation under the Australian Consumer Law, and the alternatives (confirming the photos show real work, or removing the photos with the note) were offered and declined. The images remain generated. They still must not be captioned as completed Sunnyside work, or used as before/after evidence, unless Daniel confirms they are photographs of real jobs and supplies the customer consents.
- **12 August 2026 — both removed from the site.** The services page section carrying these two photographs was replaced with a featured Google review, and the `assets/pools/` files (592 KB) were deleted. **No generated pool photography now appears anywhere on the site**, which closes the exposure described above. Git history retains the files if real photography is ever wanted in that slot.
- `sunnyside-logo.png` (transparent) and `sunnyside-logo-reversed.png` (white wordmark) were derived from the supplied `sunnyside-logo-web.png`, whose canvas was opaque white and therefore unusable on dark surfaces. The original vector should be obtained if it still exists.
