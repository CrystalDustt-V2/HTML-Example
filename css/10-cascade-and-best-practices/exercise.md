# Exercise — Your First External Stylesheet

## 🎯 Goal

Move CSS out of the page: create an external `style.css`, link it, and
organize it with comment groups. Also practice predicting which rule wins.

## 📚 What You Learned

- The cascade: specificity first, then order, then inheritance
- id > class > type specificity
- External stylesheets with `<link rel="stylesheet" href="...">`
- Organizing a stylesheet with comment groups

## 📝 Task

1. Create `my-site.html` in the `10-cascade-and-best-practices` folder with
   a small page: a `<h1>`, a couple of paragraphs, one paragraph with
   `class="intro"`, and a `<div class="card">` containing a `<p>`.
2. Create `style.css` **next to** it (same folder) and link it from the HTML
   `<head>`.
3. In `style.css`:
   - A **base** group: body font, line height, text color
   - A **typography** group: heading color; an `.intro` rule that changes
     color or style
   - A **card** group: padding, border, rounded corners, background
   - A `.card p` rule that gives paragraphs inside the card a slightly
     different color
4. Write a CSS comment **predicting** which rule wins for the intro paragraph
   (the `p` rule or the `.intro` rule) and which wins inside the card — then
   check in the browser.

## Requirements

- [ ] The HTML links `style.css` with `<link rel="stylesheet" href="style.css">`
- [ ] No `<style>` block in the HTML — all CSS is in the external file
- [ ] At least three comment groups in `style.css` (Base, Typography, …)
- [ ] An `.intro` class rule that visibly beats a type rule
- [ ] A `.card p` rule different from the plain `p` rule
- [ ] A prediction comment about who wins, verified in the browser

## 💡 Hint

The link goes in the `<head>`, and the `href` is relative to the HTML file:

```html
<head>
    <meta charset="UTF-8">
    <title>My Site</title>
    <link rel="stylesheet" href="style.css">
</head>
```

If nothing is styled, check that `style.css` is in the same folder and the
filename matches exactly.

## ⭐ Challenge

Add an element with an `id` (for example `id="footer-note"` on the last
paragraph) and give it a color that **beats** both the type rule and any
class rule. Add a comment explaining why it wins (id > class > type).

## ✅ Solution

Open `solution.html` and `solution.css` **after** you have attempted the
exercise. Compare the file organization and check whether your predictions
matched the actual result.
