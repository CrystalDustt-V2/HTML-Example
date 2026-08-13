# Lesson 06 — Links and Lists

## What you will learn

- The four link states: `:link`, `:visited`, `:hover`, `:active`
- `:focus` for keyboard users
- Removing and styling link underlines
- Styling list markers with `list-style-type`
- Removing list bullets entirely (for navigation menus)

---

## Styling links

A link is an `<a>` element. By default the browser gives it a blue color and
an underline. You can change both:

```css
a {
    color: #1f4e79;
    text-decoration: none;    /* remove the underline */
}
```

But links also have **states** — they look different depending on what the
user is doing. Four pseudo-classes control this:

| Pseudo-class | When it applies |
|--------------|-----------------|
| `:link` | the link has not been visited yet |
| `:visited` | the user has already visited the page it points to |
| `:hover` | the mouse is over the link |
| `:active` | the user is clicking the link right now |

```css
/* Normal (unvisited) links */
a:link {
    color: #1f4e79;
}

/* Visited links */
a:visited {
    color: #6b4e9e;
}

/* On hover: underline appears, color changes */
a:hover {
    color: #b22222;
    text-decoration: underline;
}

/* While clicking */
a:active {
    color: #7a1c1c;
}
```

> **Order matters.** When you write all four, keep the classic order:
> `:link`, `:visited`, `:hover`, `:active` (remember it as "LoVe HAte" —
> Link, Visited, Hover, Active). If the order is wrong, later rules can hide
> earlier ones.

### `:focus`

`:focus` styles an element while it is selected with the keyboard (the Tab
key). Never remove focus styles entirely — keyboard users need them to see
where they are:

```css
a:focus {
    outline: 2px solid #1f4e79;
    outline-offset: 2px;
}
```

### The hover state is a bonus, not the main style

The normal link color should still look like a link *without* hovering. A
common beginner pattern is styling only `a:hover` and forgetting `a` itself —
then links look like plain text until the mouse happens to touch them.

## Styling lists

### Bullets and numbers: `list-style-type`

```css
ul {
    list-style-type: square;      /* bullets: disc, circle, square, none */
}

ol {
    list-style-type: decimal;     /* numbers: decimal, lower-alpha, … */
}
```

Common values:

- For `ul`: `disc` (default), `circle`, `square`, `none`
- For `ol`: `decimal` (default), `lower-alpha` (a, b, c), `upper-roman`
  (I, II, III)

### Removing bullets for menus

Navigation menus usually have no bullets and no indent. The default list has
both — remove them like this:

```css
nav ul {
    list-style-type: none;    /* no bullets */
    margin: 0;                /* no outer spacing */
    padding: 0;               /* no left indent */
}
```

Then the links themselves become the menu items:

```css
nav a {
    display: inline-block;
    padding: 10px 15px;
    text-decoration: none;
    color: white;
    background-color: #1f4e79;
}
```

(You will learn exactly what `display` does in
[Lesson 07](../07-display-and-positioning/README.md) — for now, think of
`inline-block` as "the link can have padding, but sits on one line with its
neighbors".)

## Common mistakes

- **Wrong pseudo-class order** — if `:hover` is written before `:link`, the
  `:link` rule wins and hover seems broken. Use `link → visited → hover →
  active`.
- **Styling only `:hover`** — give `a` a base style too, so links are
  recognizable before anyone hovers.
- **Removing the focus outline** — never set `outline: none` on links without
  replacing it with a visible focus style.
- **Bullets still showing in a menu** — remember all three resets:
  `list-style-type: none; margin: 0; padding: 0;` (the left padding is what
  indents the bullets).
- **Underline disappearing everywhere** — removing underlines from all links
  is fine for menus, but in body text an underline (or another clear cue)
  helps readers spot links.

## Recap

- Links have states: `:link`, `:visited`, `:hover`, `:active` — in that order.
- `:focus` keeps links usable with the keyboard; do not remove it.
- `list-style-type` changes bullets/numbers; `none` removes them.
- Menus need `list-style-type: none; margin: 0; padding: 0;`.

## What's next?

Links and lists live inside the page flow by default. [Lesson 07](../07-display-and-positioning/README.md)
explains that flow and how to take elements out of it with `display` and
`position`.
