# Lesson 08 — Flexbox

## What you will learn

- What flexbox is for
- `display: flex` on a container
- `flex-direction` — row or column
- `justify-content` — spacing along the main axis
- `align-items` — alignment across the other axis
- `gap` — space between items

---

## What is flexbox?

Flexbox is a CSS layout mode for arranging **items inside a container** in a
row or a column. It exists because the old ways of laying out boxes were
fiddly — flexbox makes the common cases easy:

- a navigation bar where links sit side by side
- a row of cards of equal height
- centering something both horizontally and vertically

The idea has two parts:

- the **container** (the parent) gets `display: flex`
- its direct **items** (the children) are then arranged by flexbox

```html
<div class="row">
    <div class="item">1</div>
    <div class="item">2</div>
    <div class="item">3</div>
</div>
```

```css
.row {
    display: flex;
}
```

That single rule makes the three items sit side by side.

## flex-direction

Decides whether items line up as a **row** (horizontal, the default) or a
**column** (vertical):

```css
.row {
    display: flex;
    flex-direction: row;       /* default: left to right */
}

.column {
    display: flex;
    flex-direction: column;    /* top to bottom */
}
```

The direction you choose is the **main axis**; the other direction is the
**cross axis**. `justify-content` works along the main axis, `align-items`
along the cross axis.

## justify-content — spacing along the main axis

Controls how items are spaced *along the main axis*:

```css
.row {
    display: flex;
    justify-content: center;    /* grouped in the middle */
}
```

Common values:

| Value | Effect |
|-------|--------|
| `flex-start` | packed at the start (default) |
| `flex-end` | packed at the end |
| `center` | packed in the middle |
| `space-between` | first and last at the edges, equal space between |
| `space-around` | equal space around each item |
| `space-evenly` | fully equal spacing everywhere |

## align-items — alignment across the other axis

Controls how items are aligned *across the cross axis*:

```css
.row {
    display: flex;
    align-items: center;    /* vertical centering in a row */
}
```

Common values: `stretch` (default — items stretch to fill), `flex-start`,
`center`, `flex-end`.

Together these two properties are the classic recipe for centering:

```css
.centered {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 200px;
}
```

Anything inside is centered both ways.

## gap — space between items

Adds a gap between items without touching the outer edges:

```css
.row {
    display: flex;
    gap: 20px;
}
```

Much simpler than adding margins to every item except the last one.

## A complete example: a nav and a row of cards

```css
nav {
    display: flex;
    justify-content: space-between;   /* brand left, links right */
}

.cards {
    display: flex;
    gap: 20px;
}

.card {
    flex: 1;   /* each card grows equally to fill the row */
}
```

> `flex: 1` is a shortcut meaning "let this item grow to share the available
> space equally". You will meet more flex properties later — these five
> (`display: flex`, `flex-direction`, `justify-content`, `align-items`,
> `gap`) cover most beginner layouts.

## Common mistakes

- **Applying flex properties to the items, not the container** —
  `justify-content` and `align-items` go on the **parent**. The items only
  need `flex` properties (like `flex: 1`) when you want them to grow.
- **Expecting flex to affect nested content** — flexbox arranges the direct
  children of the container only. Deeper nesting needs its own flex container.
- **Confusing the two axes** — in a row, `justify-content` is horizontal and
  `align-items` is vertical; in a column, they swap. When something is not
  where you expect, check which direction your container uses.
- **Using old margins for spacing** — `gap` is simpler and does not collapse
  or double up.

## Recap

- Put `display: flex` on the **container**; its direct children become items.
- `flex-direction` chooses row (default) or column.
- `justify-content` spaces items along the main axis.
- `align-items` aligns them along the cross axis.
- `gap` adds space between items.

## What's next?

Flexbox arranges boxes. [Lesson 09](../09-forms-and-tables/README.md) shows
how to make forms and tables look good — the last new styling topics before
you bring everything together.
