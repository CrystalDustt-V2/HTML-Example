# Exercise — Style a Mini Article

## 🎯 Goal

Style a short article about your favorite book (or movie, game, or hobby) with
different fonts, sizes, alignment, and emphasis.

## 📚 What You Learned

- `font-family` with a fallback list
- `font-size` in pixels
- `font-weight` and `font-style`
- `text-align`, `line-height`, and `text-transform`

## 📝 Task

1. Create `my-article.html` in the `03-text-styling` folder.
2. Write a short article: a `<h1>` title, two or three `<h2>` section
   headings, and a few paragraphs. Add a one-line quote in a `<p class="quote">`.
3. Style it:
   - A different font for headings than for body text
   - A large title, medium section headings, and readable body text (16px or so)
   - The quote centered and italic
   - `line-height` of at least 1.5 on paragraphs
   - One word made bold and colored, using a class

## Requirements

- [ ] `font-family` on `body` ends with a generic family (`serif`,
      `sans-serif`, or `monospace`)
- [ ] Headings use a different `font-family` than body text
- [ ] At least three different `font-size` values (title > section heading >
      body)
- [ ] `.quote` is centered and italic
- [ ] `line-height` is set to at least 1.5
- [ ] A class makes one word bold and a different color

## 💡 Hint

A classic pairing: Georgia (serif) for headings, Arial (sans-serif) for body
text. For the bold word:

```css
.big-word {
    font-weight: bold;
    color: #b22222;
}
```

and in the HTML:

```html
<p>I read this book in one weekend — it was <span class="big-word">amazing</span>.</p>
```

## ⭐ Challenge

Make your section headings all-caps with `text-transform: uppercase`, then
experiment with `text-decoration: underline` on just the first paragraph.
Decide for yourself whether the underline helps or hurts readability.

## ✅ Solution

Open `solution.html` **after** you have attempted the exercise and compare
your work. Your article content is up to you — compare the *styling*.
