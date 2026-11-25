# LiveBeyond website: instructions for Claude

This repository is the LiveBeyond marketing website (livebeyond.ai). It is a plain static site: one `index.html` with inline CSS and a small inline script, plus an `images/` folder. There is no build step. Vercel serves the files as they are.

The people editing this site are not developers. They describe changes in plain words. Make the change, keep the site on-brand, and explain what you did in one or two plain sentences.

## How to work

- Never commit straight to `main`. Make every change on a new branch and open a pull request with a short, plain-English title and description ("Shortened the hero headline", not "refactor hero").
- Vercel posts a preview link on every pull request. Remind the person to open it on desktop and phone before merging.
- Keep the site as one `index.html` unless the person asks for a new page. A new page is a new `.html` file in the root, using the same header, footer and styles.
- Do not add frameworks, build tools or npm packages unless the person explicitly asks.
- Check every change at phone width (390px) as well as desktop (1440px). Nothing may scroll sideways.
- Images: put them in `images/`, use lowercase-hyphenated names, keep each under about 400 KB (resize to 1400px wide max), and give every meaningful image `alt` text. Decorative images get `alt="" aria-hidden="true"`.

## Visual rules (from the approved BeyondClock investor deck, v78)

Follow these exactly. If a request conflicts with them, do it, but say which rule it breaks.

**Backgrounds**: only white `#FFFFFF`, lilac `#F4ECFC` and deep plum `#3A0F63` (dark bands, footer). No cream, beige or off-white.

**Colours**

| Use | Colour |
|---|---|
| Primary violet (buttons, links, numerals, labels) | `#6938A0` |
| Deep plum (headings, dark sections) | `#3A0F63` |
| Body text | `#565469` |
| Small/muted text on white | `#6E6C84` |
| Highlight card fill | `#ECDCFC` |
| Borders and hairlines | `#E6E0EE`, stronger `#D9C9F0` |
| Pink emphasis word in a headline (white or lilac ground) | `#B8429F` |
| Pink accent rule on plum | `#D86CCC` |
| Light text on plum | `#FFFFFF`, `#ECDCFC`, `#D9C9F0` |

Pink is only for one or two emphasis words in large headlines and short accent rules. Never for body text or small labels.

**Type**: Playfair Display Italic (weight 400) for headlines, names and big numerals; Poppins for everything else (300 body, 400 card titles, 500 labels and buttons). Both load from Google Fonts in the `<head>`.

**Deck devices to reuse**

- Section labels: tiny uppercase Poppins 500, wide letter-spacing, violet, in the form `03 // The science`.
- Section openers: a split block with text on white (label, big italic numeral like `02`, italic headline) and a full-height image on the other half.
- Cards: 6px corners, either white with a `#E6E0EE` border, lilac `#F4ECFC`, or highlight `#ECDCFC`. Numbered cards start with an italic `01`, a short pink rule, a small label, then the title.
- Bullets use a violet `+`, not dots.
- "+ Message" bar: lilac strip with a tiny "+ MESSAGE" label and one italic Playfair sentence.
- Round violet arrow buttons (40–48px circle with a white arrow) next to a text label; pill buttons in violet `#6938A0`.
- Dark plum band with white italic headline for partnerships, contact and footer.
- Imagery: the approved deck and Midjourney set only (lavender hills, glass crystals, molecular rings, iridescent spheres, people in white and lilac). No stock photos, no emoji, no gradient washes.

**Accessibility**: text contrast at least 4.5:1 (3:1 only for headlines 24px+). Real `<button>` and `<a href>` elements. Visible focus outlines. Touch targets at least 44px.

## Content rules

- Do not invent statistics, client names, testimonials, prices or clinical claims. If something is missing, write a clear placeholder like `[CONFIRM PRICE]` and tell the person.
- BeyondClock is described as general-wellbeing information, not medical advice, diagnosis or treatment, and it does not predict lifespan. Keep those disclaimers wherever results or reports are shown.
- Keep the caveats next to the LinAge2 paper and the Raffles listing.
- The sources and open decisions are listed in the "Sources, design decisions & pre-launch notes" panel in the footer. Update it when content changes.

## Before public launch (do only when asked)

1. Remove the "Independent website concept // For discussion" bar at the top and the concept line and notes panel in the footer.
2. Remove `<meta name="robots" content="noindex, nofollow">` from the `<head>`.
3. Replace the email-draft form with the approved form service (the destination and privacy terms must be agreed first).
4. Add privacy and legal pages, a favicon and a social-sharing image.
5. Connect the livebeyond.ai domain in Vercel.
