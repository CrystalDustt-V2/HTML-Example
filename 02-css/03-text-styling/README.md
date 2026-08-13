# Lesson 03 — Text Styling

## What you will learn

- Choosing fonts with `font-family`
- Sizes with `font-size`
- Bold and italic with `font-weight` and `font-style`
- Alignment with `text-align`
- `text-decoration`, `line-height`, and `text-transform`

---

## Font family: `font-family`

`font-family` chooses the font (the typeface):

```css
body {
    font-family: Arial, sans-serif;
}

h1 {
    font-family: Georgia, serif;
}
```

You usually give a **list** of fonts, separated by commas. The browser uses
the first one it has; if it does not have it, it tries the next:

```css
font-family: "Times New Roman", Georgia, serif;
```

- The **last item** is a *generic family* that always exists: `serif`
  (fonts with small lines at the ends of letters), `sans-serif` (clean fonts
  without those lines), `monospace` (typewriter-style, every letter the same
  width).
- Put font names with spaces in quotes: `"Courier New"`.

## Font size: `font-size`

```css
p {
    font-size: 16px;
}

h1 {
    font-size: 32px;
}
```

Sizes are often written in **pixels** (`px`), which are a good place to start.

## Bold and italic

```css
strong-text {
    font-weight: bold;
}

em-text {
    font-style: italic;
}
```

- `font-weight` controls thickness. Values: `normal`, `bold`, or numbers from
  `100` (thin) to `900` (black). `400` is normal and `700` is bold.
- `font-style` controls slant: `normal` or `italic`.

> Note: HTML already has `<strong>` (bold) and `<em>` (italic) elements. CSS
> lets you *override* how they look — for example, you can make `<em>` not
> italic. The HTML element says *what* the text means; CSS says *how* it
> looks.

## Alignment: `text-align`

```css
p {
    text-align: center;
}
```

Values: `left` (default for most languages), `right`, `center`, and
`justify` (stretches lines so both edges are straight).

## More text properties

```css
a {
    text-decoration: none;      /* remove the underline from links */
}

p {
    line-height: 1.5;           /* space between lines (1.5 × font size) */
}

h2 {
    text-transform: uppercase;  /* ALL CAPS */
}
```

- `text-decoration`: `none`, `underline`, `overline`, or `line-through`.
- `line-height`: the space between lines of text. A number like `1.5` is
  usually more readable than the default.
- `text-transform`: `uppercase`, `lowercase`, or `capitalize` (every word
  starts with a capital letter).

## Common mistakes

- **Too many fonts** — using a different font everywhere looks messy. Pick one
  font for headings and one for body text, and stick with them.
- **Forgetting the fallback** — always end `font-family` with a generic family
  (`serif`, `sans-serif`, `monospace`), so something readable is used even if
  your first choice is missing.
- **No space after commas in `font-family`** — the space is optional in
  browsers, but write `Arial, sans-serif` for readability.
- **Tiny or huge text** — 16px body text is a comfortable default; headings
  are larger. Don't shrink everything to fit.
- **Centering everything** — center only short elements (headings). Long
  paragraphs are easier to read left-aligned.

## Recap

- `font-family` picks the typeface (with a fallback list).
- `font-size` sets the size (usually in `px`).
- `font-weight` and `font-style` control bold and italic.
- `text-align` aligns text; `text-decoration` underlines or removes lines.
- `line-height` and `text-transform` polish readability and case.

## What's next?

So far every rule has used element names like `h1` or `p`. [Lesson 04](../04-selectors/README.md)
shows how to target *specific* elements with classes and ids.
