# Final Project — Styled Personal Website

Congratulations — you have finished all ten CSS lessons! Now it is time to
combine everything: give the **personal website** you built in the HTML
course a complete look with one external stylesheet.

## 🎯 Goal

Take the personal website from the HTML course (already prepared for you in
`starter.html`) and style it with a single external `style.css`. The goal is
to demonstrate your CSS knowledge: colors, typography, the box model, links,
lists, flexbox, and styled forms and tables.

## 📚 What you will use

- An **external stylesheet** (`style.css`) linked in the `<head>`
- Colors: `color` and `background-color` (named, hex, and `rgb()`)
- Typography: `font-family` (with fallbacks), `font-size`, `line-height`
- The box model: `padding`, `border`, `border-radius`, `margin`
- Link states: `:hover` (plus `:visited` and `:focus` if you like)
- Lists: `list-style-type`, the menu reset (`margin: 0; padding: 0;`)
- **Flexbox**: a nav with `space-between`, a row of project cards with `gap`
- Forms and tables: styled fields, button with `:hover`, `border-collapse`,
  colored `thead`, zebra stripes
- Cascade and organization: comment groups, sensible rule order

## 📝 Task

The HTML is already written — your job is the CSS. There is **no** JavaScript
and **no** `<style>` block allowed; everything goes in `style.css`.

1. Open `starter.html` and read it. Note the three hooks already in the HTML:
   - `main class="container"` — style this to limit the page width and center
     it (`width` + `margin: 0 auto`).
   - `nav ul class="menu"` — style this to remove bullets and indent.
   - `article class="project"` — style these as cards.
2. Create `style.css` **in this same folder** and link it from the `<head>` of
   your page:
   ```html
   <link rel="stylesheet" href="style.css">
   ```
3. Style the page. Suggested structure for your stylesheet:

   ```css
   /* ---------- Base ---------- */
   /* body: font, line-height, background, text color */

   /* ---------- Header & nav ---------- */
   /* dark header, white text; .menu as a flexbox row; links as buttons */

   /* ---------- Layout ---------- */
   /* .container: width + margin: 0 auto */

   /* ---------- Sections ---------- */
   /* about (avatar!), .project cards (padding, border, radius, gap) */

   /* ---------- Lists, table, form ---------- */
   /* skills list, zebra table, styled fields and button */

   /* ---------- Aside & footer ---------- */
   /* quote box, dark footer, links */
   ```

## Requirements

- [ ] CSS lives in an external `style.css` linked from the `<head>`; no
      `<style>` block and no inline styles in the HTML
- [ ] The `body` has a `font-family` ending in a generic family and a
      comfortable `line-height` and text color
- [ ] At least one `background-color` and one `color` in hex, one named
      color, and one `rgb()` somewhere in the stylesheet
- [ ] `main.container` is centered and limited in width
- [ ] `nav ul.menu` has no bullets and no indent, and the nav links have
      padding, a background, and a `:hover` change
- [ ] The project `article`s are laid out with **flexbox** (`display: flex`,
      `gap`) and have padding, border, and `border-radius`
- [ ] The table uses `border-collapse: collapse`, a colored `thead`, and
      zebra stripes
- [ ] The form fields share a consistent style, and the button has
      `cursor: pointer` and a `:hover` style
- [ ] Every link has a visible `:hover` (and `:focus`) state
- [ ] The stylesheet is organized with at least four comment groups

## 💡 Hints

- The `#about` section is a great place to try flexbox: put the avatar image
  and the paragraphs side by side (`display: flex` + `align-items: center`).
- Round the avatar with `border-radius: 50%`.
- The skills list has **nested** lists — remember that the menu reset
  (`list-style-type: none; margin: 0; padding: 0;`) only needs to apply to
  the menu, not to every list.
- Change one property at a time and refresh. If a rule does nothing, check
  the selector: is the class in the HTML spelled the same as in the CSS?

## ⭐ Challenge

1. Give the header `position: sticky; top: 0;` so the menu stays visible
   while you scroll (sticky is a sibling of the `fixed` you learned in
   Lesson 07 — it sticks within its container instead of the window).
2. Add a `:visited` style so visited footer links look different.
3. Style the `aside` as a "quote box" with a light background, a left border
   (for example `border-left: 4px solid #1f4e79`), and padding.

## ✅ Solution

Open `solution.html` and `style.css` **after** you have finished your own
attempt. Yours does not need to look like the solution — compare how both
use the same ten lessons.
