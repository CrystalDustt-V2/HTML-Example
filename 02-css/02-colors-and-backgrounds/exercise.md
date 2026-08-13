# Exercise — A Colorful Page

## 🎯 Goal

Create a small page about your favorite color and style it with a consistent
palette using `color` and `background-color`.

## 📚 What You Learned

- The `color` property (text color)
- The `background-color` property
- Named colors, hex, and `rgb()`
- Keeping text readable (contrast)

## 📝 Task

1. Create `favorite-color.html` in the `02-colors-and-backgrounds` folder.
2. The page has a heading and at least three short paragraphs about your
   favorite color (why you like it, where you see it, …).
3. Style the page:
   - A light background for the whole page (`body`)
   - A heading with a colored background and a readable text color
   - Paragraphs in a dark, readable text color
   - One element highlighted with a different background color
4. Use **all three color formats** somewhere in your CSS: at least one named
   color, one hex, and one `rgb()`.

## Requirements

- [ ] The page has a `<style>` block in the `<head>`
- [ ] `background-color` on `body`
- [ ] A heading styled with both `color` and `background-color`
- [ ] At least one highlighted element with its own background
- [ ] At least one named color, one hex color, and one `rgb()` color in your
      CSS
- [ ] All text is readable against its background

## 💡 Hint

Pick your palette before you write CSS. For example, for the color blue:

- background: `#eef4fb` (very light blue)
- heading background: `#1f4e79` (dark blue), heading text: `white`
- highlighted text: `#ffe68a` (light yellow) with dark text

Write the values down, then use them in your rules.

## ⭐ Challenge

Change the `<h1>` so its background uses the **same** color in two different
formats — for example give it a `background-color` in hex in one rule and add
a paragraph whose `color` is the same value written as `rgb()`. The two colors
should look identical in the browser.

## ✅ Solution

Open `solution.html` **after** you have attempted the exercise and compare
your work. Your palette does not need to match — but every text/background
pair on the solution is readable, and yours should be too.
