# Lesson 02 — Colors and Backgrounds

## What you will learn

- The `color` property for text
- The `background-color` property
- Named colors, hex colors, and `rgb()`
- Making sure text is readable (contrast)

---

## Text color: `color`

The `color` property changes the color of text:

```css
h1 {
    color: darkblue;
}

p {
    color: gray;
}
```

> `color` styles the *text*. The *background* is a different property — see
> below. Beginners often mix these up, which is why text sometimes becomes
> invisible.

## Background color: `background-color`

The `background-color` property paints the background of an element:

```css
body {
    background-color: #fafafa;
}

h1 {
    background-color: yellow;
}
```

You can use it on any element: the whole page (`body`), headings, paragraphs,
or a container like `div` or `section`.

## Ways to write colors

CSS accepts several color formats. All of these mean roughly the same "blue":

```css
/* Named color */
color: blue;

/* Hex (hexadecimal) — the most common format */
color: #0000ff;

/* RGB — red, green, blue, each from 0 to 255 */
color: rgb(0, 0, 255);
```

### Named colors

The easiest to read: `red`, `blue`, `green`, `white`, `black`, `gray`,
`orange`, `teal`, `crimson`, `darkblue`, … There are about 140 named colors,
all with fixed meanings.

### Hex colors

Written as `#` followed by six hex digits (0–9 and a–f): two for red, two for
green, two for blue.

```
#ff0000  →  red (maximum red, no green, no blue)
#00ff00  →  green
#0000ff  →  blue
#ffffff  →  white (all maximum)
#000000  →  black (all zero)
```

Hex gives you far more control than named colors. If both pairs are the same,
you can shorten them: `#ff0000` → `#f00`, `#ffffff` → `#fff`.

### rgb()

The same idea as hex, written as numbers:

```css
color: rgb(255, 0, 0);   /* red */
color: rgb(102, 51, 153); /* a purple */
```

## Common mistakes

- **No contrast** — light-gray text on a white background is nearly
  unreadable. Dark text on a light background (or the reverse) is the safe
  choice.
- **Coloring the page instead of the text** — `color` styles text,
  `background-color` styles the background. To make the whole page light gray
  you need `background-color` on `body`.
- **Wrong number of hex digits** — `#fff` (3) or `#ffffff` (6) are valid;
  `#fffff` (5) is not.
- **Missing `#` in hex colors** — write `#ffcc00`, not `ffcc00`.
- **Spelling `gray` differently** — both `gray` and `grey` work, but pick one
  and be consistent.

## Recap

- `color` changes **text** color; `background-color` changes the **background**.
- Three common formats: named colors (`teal`), hex (`#008080`), and
  `rgb(0, 128, 128)`.
- Check contrast: text must be readable against its background.

## What's next?

Colors are fun, but most of a page is text. [Lesson 03](../03-text-styling/README.md)
shows how to control fonts, sizes, and alignment.
