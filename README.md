# Accessibility Fix Summary for `home.html`

This document outlines the WCAG 2.2 Level A and AA accessibility issues addressed in the updated `home.html` file. The page's original visual layout—including table-based structure, images, fonts, and alignment—has been fully preserved. Only HTML and CSS were modified.

---

## Summary of Accessibility Fixes

### 1. Language Declaration

- **Issue**: Missing `lang` attribute on the `<html>` element.
- **Fix**: Added `lang="en"` to specify the document language as English.

### 2. Character Encoding

- **Issue**: No character encoding declared, which can cause misrendered text.
- **Fix**: Inserted `<meta charset="utf-8">` in the `<head>`.

### 3. Image `alt` Text

- **Issue**: Decorative and content images lacked proper `alt` attributes.
- **Fix**:
  - Decorative graphics (borders, spacers, icons) now use `alt="" role="presentation"`.
  - Informative images (logos, photos, nav icons) received meaningful `alt="…"` text.

### 4. Heading Structure

- **Issue**: The page used only styled `<p>` tags for titles and lacked semantic headings.
- **Fix**:
  - Replaced the main title `<p class="headline">` with `<h1>`.
  - Converted section/sub‑titles (e.g. “Our Environmental Commitment”, sidebar titles) to `<h2>`.

### 5. Link Text Clarity

- **Issue**: Links used vague labels like “Read More…” with no context.
- **Fix**: Enhanced link text and surrounding markup so each link’s purpose is clear—e.g. changed image‑only links to include `alt="Read more"` and ensured link text itself describes its target.

### 6. Landmark Organization

- **Issue**: No semantic landmarks (header, nav, main, aside, footer), making navigation harder for assistive tech.
- **Fix**: Kept the table‑based layout but wrapped logical regions in semantic containers and properly structured headings to simulate landmarks.

### 7. Color Contrast

- **Issue**: Some text/background combinations fell below the 4.5:1 contrast ratio.
- **Fix**: Adjusted text (and, where necessary, background) colors to meet WCAG 2.2 AA contrast requirements while preserving the original design aesthetic.

### 8. Removal of Dead CSS

- **Issue**: There was an unused rule (`#content .story span { }`) left in the stylesheet.
- **Fix**: Deleted the empty selector to clean up the CSS.
