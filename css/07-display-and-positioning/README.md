# Lesson 07 — Display and Positioning

## What you will learn

- `display: block`, `inline`, `inline-block`, and `none`
- The normal page flow
- `position: static`, `relative`, `absolute`, and `fixed`
- Offsetting elements with `top`, `right`, `bottom`, `left`

---

## Display: how elements sit on the line

Every element has a `display` value that decides how it behaves in the page
flow. Four values cover almost everything a beginner needs.

### Block

```css
p, h1, div, section {
    display: block;   /* this is the default for these elements */
}
```

Block elements:

- Start on a **new line** and take the full width available
- Stack vertically, one after another
- Accept `width`, `height`, `margin`, and `padding` normally

### Inline

```css
span, a, em, strong {
    display: inline;  /* default for these elements */
}
```

Inline elements:

- Sit **next to** other inline content on the same line
- Flow like text inside a paragraph
- **Ignore** `width` and `height`, and only respect horizontal padding/margin

### Inline-block

```css
.button {
    display: inline-block;
}
```

The best of both: sits on a line with neighbors (like inline), but accepts
`width`, `height`, and vertical spacing (like block). This is what you used
for menu links and "chips" in earlier lessons.

### None

```css
.hidden {
    display: none;
}
```

Removes the element from the page **completely** — no space is left behind.
(Different from `visibility: hidden`, which hides the element but keeps its
space.)

## Position: where an element goes

All elements are in the normal flow by default. The `position` property takes
an element out of that flow, or shifts it.

| Value | What it does |
|-------|--------------|
| `static` | The default. Normal flow, ignores `top`/`left`/etc. |
| `relative` | Normal flow, but shifted from its normal spot |
| `absolute` | Taken out of flow; positioned relative to the nearest *positioned* ancestor (or the page) |
| `fixed` | Taken out of flow; stays put relative to the browser window, even when scrolling |

### `relative`

The element stays in the flow, but you can nudge it with `top`, `right`,
`bottom`, or `left`:

```css
.badge {
    position: relative;
    top: -5px;    /* moved 5px up from where it would normally sit */
}
```

### `absolute`

The element is removed from the flow (other elements ignore it) and placed
relative to the nearest ancestor with `position: relative` (or `absolute` /
`fixed`). If no ancestor is positioned, it is placed relative to the page.

```css
.card {
    position: relative;   /* becomes the reference point */
}

.badge {
    position: absolute;
    top: 10px;
    right: 10px;
}
```

The classic pattern: a "badge" or "ribbon" pinned to the corner of a card.

### `fixed`

The element is removed from the flow and pinned to the browser window. It
stays visible while the page scrolls:

```css
.top-bar {
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
}
```

## Common mistakes

- **Applying `width` to an inline element** — it is ignored. Use `inline-block`
  or `block` if you need a width.
- **Forgetting to position the parent** — an `absolute` child without a
  `position: relative` ancestor positions itself relative to the page, which
  is rarely what you wanted. Add `position: relative` to the parent.
- **Overusing `absolute`** — absolute positioning fights the normal flow.
  For most layouts, plain flow, `display`, and (in the next lesson) flexbox
  are simpler and sturdier.
- **`display: none` for hiding** — it removes the element from the page.
  If you only want it invisible but in place, use `visibility: hidden`.
- **Mixing up `position` and `display`** — they are different tools.
  `display` decides how the element behaves on the line; `position` decides
  where it goes.

## Recap

- `display`: `block` (full-width, stacked), `inline` (in the text flow),
  `inline-block` (both), `none` (removed).
- `position`: `static` (default), `relative` (nudged from its spot),
  `absolute` (relative to a positioned ancestor), `fixed` (relative to the
  window, stays while scrolling).
- Offset with `top`, `right`, `bottom`, `left`.

## What's next?

Positioning one box at a time is fiddly. [Lesson 08](../08-flexbox/README.md)
introduces flexbox — the modern way to lay out rows and columns of boxes.
