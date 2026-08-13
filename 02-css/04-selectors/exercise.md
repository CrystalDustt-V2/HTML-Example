# Exercise — Style with Classes and Ids

## 🎯 Goal

Style a given page by targeting specific elements with classes, ids, grouped
selectors, and a descendant selector.

## 📚 What You Learned

- Type, class, and id selectors
- Grouping and descendant selectors
- When to use a class vs. an id

## 📝 Task

1. Create `classy-page.html` in the `04-selectors` folder.
2. Build a small page with:
   - A `<nav>` with three links
   - A `<h1>` title with `id="page-title"`
   - Three paragraphs; two of them share `class="highlight"`
   - A `<h2>` and a couple more paragraphs
3. Style it so that:
   - The `h1` and `h2` share a color (use a **grouping** selector)
   - The element with `id="page-title"` is larger than the other headings
   - Only the two `highlight` paragraphs get a background color
   - Only the links **inside the `nav`** are white on a dark background
     (use a **descendant** selector)
   - A normal `<p>` rule gives all paragraphs the same text color and size

## Requirements

- [ ] At least one class used on two elements
- [ ] Exactly one id used on the title
- [ ] A grouping selector (`h1, h2 { ... }` style)
- [ ] A descendant selector (`nav a { ... }` style)
- [ ] A plain type selector for paragraphs
- [ ] The `highlight` paragraphs differ visually from the normal ones

## 💡 Hint

Write the HTML first, add the `class` and `id` attributes, then write CSS for
each part. If a rule does nothing, check for a missing `.` or `#` in front of
the selector.

## ⭐ Challenge

Add a fourth paragraph with **two** classes, for example
`class="highlight small"`, and write rules that use *only one* of the two
classes to affect it. Verify that the element picks up styles from both class
rules.

## ✅ Solution

Open `solution.html` **after** you have attempted the exercise and compare
your work. The important part is that each selector targets exactly the
elements you intended.
