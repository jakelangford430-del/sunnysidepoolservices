# Sunnyside Pool Services copy audit

Original audit: 6 August 2026
Last updated: 12 August 2026

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
- Phone-first enquiries; no online booking or enquiry form on the rebuilt site
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
