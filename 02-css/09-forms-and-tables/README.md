# Lesson 09 — Forms and Tables

## What you will learn

- Styling form fields: padding, borders, `border-radius`
- `:focus` styles for fields
- Styling buttons
- Table borders with `border-collapse`
- Padding in table cells and readable tables

---

## Styling form fields

By default, browser form fields look plain. A little padding, a border, and
rounded corners go a long way:

```css
input, textarea, select {
    padding: 8px 10px;
    border: 1px solid #cccccc;
    border-radius: 4px;
    font-size: 16px;
}
```

The `font-size: 16px` matters: on phones, browsers zoom into fields smaller
than 16px when you type in them. 16px keeps everything calm.

### Focus styles

When a user clicks (or tabs) into a field, it gets `:focus`. Style it so the
active field is obvious:

```css
input:focus, textarea:focus, select:focus {
    border-color: #1f4e79;
    outline: 2px solid #1f4e79;
    outline-offset: 1px;
}
```

> Just like with links, do **not** remove the focus outline. Make it visible
> and nice instead.

### Buttons

```css
button {
    padding: 10px 20px;
    background-color: #1f4e79;
    color: white;
    border: none;
    border-radius: 4px;
    font-size: 16px;
    cursor: pointer;
}
```

- `border: none` removes the default border so the background color shows
  cleanly.
- `cursor: pointer` shows the hand cursor over the button.
- Add a `:hover` state so the button responds:

```css
button:hover {
    background-color: #b22222;
}
```

## Styling tables

### Borders

`table` borders do not touch by default — each cell has its own border with a
gap. `border-collapse: collapse` joins them into one clean grid:

```css
table {
    border-collapse: collapse;
    width: 100%;
}

th, td {
    border: 1px solid #cccccc;
    padding: 10px 14px;
    text-align: left;
}
```

### A header that stands out

```css
thead th {
    background-color: #1f4e79;
    color: white;
}
```

### Zebra striping

Alternating row colors make long tables easier to scan:

```css
tbody tr:nth-child(odd) {
    background-color: #eef4fb;
}
```

`tr:nth-child(odd)` selects every other row (the odd-numbered ones). You will
meet `nth-child` in detail later — this one pattern is enough for now.

## Common mistakes

- **Fields of different widths in one form** — give your inputs a consistent
  width (for example `width: 100%` with a container that limits the form's
  width).
- **Borderless buttons** — remember `border: none`, or the default border
  fights your background color.
- **No `:focus` styles** — the browser default outline works, but a styled
  focus state looks better and still helps keyboard users. Never set
  `outline: none` and stop there.
- **Double table borders** — if you see doubled lines between cells, you
  forgot `border-collapse: collapse`.
- **Tiny font in fields** — keep `font-size: 16px` (or larger) in inputs.

## Recap

- Give fields consistent padding, border, and `border-radius`.
- Style `:focus` — and never remove it without replacing it.
- Buttons: padding, background, `border: none`, `cursor: pointer`, `:hover`.
- Tables: `border-collapse: collapse`, cell padding, a distinct `thead`,
  optional zebra stripes.

## What's next?

You now know all the styling tools. [Lesson 10](../10-cascade-and-best-practices/README.md)
ties it together: how CSS rules win conflicts, and how to organize real
stylesheets.
