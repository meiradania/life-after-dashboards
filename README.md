# Life After Dashboards

Static site for Life After Dashboards (data literacy and analytics training, consulting and live show).
Plain HTML and CSS, no build step. The look follows the **Life After Dashboards design system** (pop-art print: cream ground, thick key lines, halftone dots, hard colour fields).

## Files
- `index.html` – home page (hero, episodes list, hosts, watch the latest episode / join as a guest)
- `robots.txt`, `sitemap.xml` – for search engines; add each new episode page to the sitemap
- `privacy.html` – event privacy policy (can be used as the privacy URL for LinkedIn events)
- `style.css` – page layout, built on the design-system tokens
- `css/tokens.css` – design tokens (colours, type, spacing, shadows); copied from the design system
- `css/bundle.css` – component styles (`.lad-*`: wordmark, buttons, tags, stickers, cards, event card); copied from the design system
- `css/fonts.css` – self-hosted fonts, so visitors never call Google
- `fonts/` – Bungee, Bangers, Rubik, Space Mono (SIL Open Font License, licences included)
- `img/` – Episode 01 poster/thumbnail (also the social preview image), favicon and touch icon
- `.nojekyll` – tells GitHub Pages to serve the files as they are

## Updating the design
`css/tokens.css` and `css/bundle.css` are generated from the design system: replace them with the new versions rather than editing them by hand. Put site-specific rules in `style.css`.

## Tracking
Every external link (LinkedIn, YouTube) carries `?utm_source=landingpage`. Internal links and `mailto:` links do not (UTM on internal links would restart the visit in analytics).

## Episode pages
There is no page for Episode 01 yet: it goes live after the episode airs, with the transcript (the previous draft is in git history, commit `2b7aad6`). Link the thumbnail in the Episodes list to it then, add it to `sitemap.xml`, and move the `Event` structured data to that page.

## To finish
Search for `TODO` in `index.html` and fill in: the Episode 01 LinkedIn event URL, host bios and host photos (an `<img>` in the disc; see the `TODO`s in the Hosts section). After Episode 01, swap the poster in `img/` and the hero copy for the next episode.

## Publish on GitHub Pages
Settings → Pages → Build and deployment → Source: "Deploy from a branch", Branch: `main`, folder `/ (root)`.
Live at `https://<your-username>.github.io/life-after-dashboards/`.
