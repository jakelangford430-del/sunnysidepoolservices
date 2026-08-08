# Sunnyside Pool Services copy audit

Original audit: 6 August 2026
Last updated: 8 August 2026 (rebuild — core four pages)

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
- Customer reviews: six reproduced verbatim from Google, captured 8 August 2026 — Dhanushka Sigera, Mina Salib, Daphne Whiteside, Conner Maitland, Fale Talaepa, Karl Fisher
- Google rating: 5.0 from 20 reviews, confirmed on the Google Business Profile 8 August 2026
- Google Business Profile: https://share.google/x0TZIAeJNAugILFP8
- Google category: Swimming pool contractor

## Supplied directly by Sunnyside

Provided for the rebuild, not independently confirmed on a public source:

- Founded by Daniel
- Service area: Western Australia
- 60+ regular pool cleans for ongoing clients
- Equipment repair and assessment services
- Fibreglass renovation services
- Testing technology used to read water chemistry, filtration, circulation and equipment condition
- Phone-first enquiries; no online booking or enquiry form on the rebuilt site

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

- **Service area widened to Western Australia** at Daniel's direction, including `areaServed` in the LocalBusiness schema. Previously Perth metro. Copy still leads with Perth where natural, since that is where search volume sits.
- **`60+` reworded** from "regular cleans every month" to "60+ regular pool cleans for ongoing clients". The monthly framing is no longer used.
- **Review count is deliberately not displayed** in visible copy. It is present in `aggregateRating` schema, which requires it, and is public on the Google profile regardless.
- **Rating published.** 5.0 shown in the proof bar on Home, Services and Contact, linked to the Google profile so a visitor can check it. `aggregateRating` (5.0 / 20) added to LocalBusiness schema on all four pages, with the profile as `sameAs`.
- **Reviews are quoted in full only.** Reviews truncated by Google's "…More" link were left out rather than clipped mid-sentence or completed by guesswork.

## Conflict to resolve: service area

The site states Western Australia, including `areaServed` in the schema, at Daniel's direction.

Sunnyside's own Google Business Profile draws a much tighter service area — a polygon covering Joondalup, Ellenbrook, Perth, Fremantle, Rockingham and Mandurah. That is the Perth metropolitan area plus Peel, not the state.

Google uses the Business Profile service area for local ranking, so the two should agree. Either widen the profile to match the site, or narrow the site to metro and note that renovation, equipment and one-off work travels further — which is what the Contact page already says.

## Still outstanding

- **Before/after photography.** None exists. The module is not built until real matched pairs are supplied.
- **Certifications, licences, insurance.** None evidenced. No trust badges are shown.
- **Gallery photography.** No photographs of completed Sunnyside work are available.
- Truncated Google reviews (David, Stefunia G, Ebony H, Kate Baxter, Rebecca Lamont, conno749, K P) can be added once supplied complete.
- **Opening hours.** The Google profile shows "Opens 7am Mon" but the full week was not captured. Supply the trading hours and `openingHoursSpecification` can be added to the schema.

## Image sources

- Hero and equipment photographs were generated for this rebuild and depict representative settings, not completed Sunnyside projects.
- `sunnyside-logo.png` (transparent) and `sunnyside-logo-reversed.png` (white wordmark) were derived from the supplied `sunnyside-logo-web.png`, whose canvas was opaque white and therefore unusable on dark surfaces. The original vector should be obtained if it still exists.
