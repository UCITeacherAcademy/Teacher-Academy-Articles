# Teacher Academy Classroom Library

A body-only redesign of https://teacheracademy.uci.edu/classroom/ for WordPress / Divi. No build step, JavaScript, external fonts, or Cloudflare deployment is needed. GitHub stores the source; WordPress serves the page.

## Install in Divi

1. Create a draft page and enable Divi Builder. Retain your existing site header and footer.
2. Add a regular section with a single-column row and a Code module.
3. Set the row width to 100% and max width to 100%. Set section/row padding to 0 so the module manages its own spacing.
4. Paste the complete contents of `divi-code-module.html` into the Code module. It includes a scoped `<style>` block and the page body. Do not paste `index.html`, which is only a standalone preview.
5. Save the draft and preview desktop and mobile. Publish through your normal WordPress workflow.

Alternative: paste `classroom.html` into the Code module and `classroom.css` into the page's Custom CSS field (without `<style>` tags). Use one installation method, not both.

All styles are scoped beneath `.ta-library`. The snippet adds no site navigation and does not alter the theme header or footer. If WordPress removes the style block, use the separate CSS method with an account permitted to edit page CSS. Installation has not been tested inside your live Divi environment.

## Files and maintenance

- `divi-code-module.html`: complete copy-and-paste deliverable.
- `classroom.html`: body markup only.
- `classroom.css`: scoped responsive CSS.
- `index.html`: local standalone preview; open in a browser.
- `articles.json`: reference inventory of all 31 resources and their source metadata.

The HTML is static: changes to WordPress posts or `articles.json` do not automatically update the cards. To add an article, duplicate a `.ta-card` in the appropriate section, update title/link/author/date/type, and adjust the section and total counts. Keep the separate and combined deliverables in sync.

## Content and editorial decisions

Source reviewed November 13, 2026: https://teacheracademy.uci.edu/classroom/ . All 31 nonempty resource headings are retained with original authors and publication dates, grouped into five editorial topics. The feature description and section introductions are new summaries. Full articles remain on the original WordPress URLs. Article dates are preserved, including March 2023 where no day was supplied.

Destinations use the source heading links rather than generic Read More links: the old page contains some mismatched Read More destinations. Builder query strings (`?fl_builder`) have been removed from public links. Each destination was transcribed from the source page; individual destination availability has not been comprehensively verified. The feature uses a CSS and typography panel with no external image dependency. Historical dates and an archive note distinguish older material from current advice.

## Validation

Browser preview checked at 390px and 1440px: no horizontal overflow. Topic jump links worked; all 31 cards rendered.

Verify 31 article cards, all five topic anchors, keyboard focus, desktop/mobile layout, and theme integration before publishing. No WordPress page has been changed by this repository.
