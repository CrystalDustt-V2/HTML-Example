# Lesson 10 — Cascade and Best Practices

## What you will learn

- The cascade: which rule wins when several match
- Specificity: id > class > type
- Inheritance
- External stylesheets and how to organize a real `style.css`

---

## Why "Cascading"?

CSS stands for *Cascading* Style Sheets. "Cascading" means that when several
rules could apply to the same element, the browser has a fixed system for
deciding which one wins. You do not need to memorize every detail — you need
the three rules that decide almost every conflict.

## Rule 1 — Specificity

When two rules target the same element, the **more specific** selector wins.
The rough order (most specific first):

```
id (#header)          → most specific
class (.card)         →
type (p, h1, div)     → least specific
```

```css
p { color: gray; }            /* type — lowest specificity */
.intro { color: teal; }       /* class — wins over the type rule */
#special { color: crimson; }  /* id — wins over both */
```

A paragraph with `class="intro"` **and** `id="special"` would be crimson.

Two practical consequences:

- A class rule always beats a plain element rule, no matter what order they
  appear in the file.
- An id rule beats a class rule. This is why ids are for unique elements —
  using them for styling creates conflicts that are hard to override later.

## Rule 2 — Later rules win (at equal specificity)

If two rules have the **same** specificity, the one that appears **later** in
the stylesheet wins:

```css
h1 { color: teal; }
h1 { color: crimson; }   /* this one wins */
```

## Rule 3 — Inheritance

Some properties are **inherited**: children take the value from their parent
unless they set their own. Text properties are the big ones:

```css
body { font-family: Arial, sans-serif; }
```

Every paragraph, heading, and link inside `<body>` inherits Arial — you style
the whole page with one rule.

Not everything inherits. Backgrounds and borders do **not** inherit — each
element has its own (usually transparent) background.

## External stylesheets

From [Lesson 01](../01-introduction/README.md) you know the three ways to add
CSS. Real projects use **external stylesheets**: one `style.css` file linked
from the HTML `<head>`:

```html
<link rel="stylesheet" href="style.css">
```

Why external wins:

- **One file, many pages** — change the site's colors in one place.
- **Clean HTML** — structure and style stay separate.
- **Faster to read** — a long stylesheet is easier to manage than styles
  scattered across pages.

This lesson's `example.html` uses an external `style.css` — look at both files
and how the link connects them.

## Organizing a stylesheet

Good organization makes a stylesheet readable and easy to grow:

1. **Group rules by purpose**, in a sensible order:
   - Base styles first (`body`, general typography)
   - Then sections of the page (header, nav, main, footer)
   - Then specific components (cards, buttons, badges)
2. **Add a comment before each group**:

```css
/* ---------- Base ---------- */
body {
    font-family: Arial, sans-serif;
    line-height: 1.6;
}

/* ---------- Navigation ---------- */
nav {
    background-color: #1f4e79;
}
```

3. **Name classes by purpose**, not appearance — `.warning` not `.red`,
   `.card` not `.box-1`.
4. **Keep specificity low** — prefer classes over ids for styling. A
   stylesheet full of `#header`, `#nav`, `#footer` ids is hard to override.

## Common mistakes

- **Overriding with `!important` everywhere** — `!important` forces a rule to
  win regardless of specificity:

  ```css
  p { color: red !important; }
  ```

  Use it rarely (or never as a beginner). If you need it often, your
  specificity is probably out of control.
- **Styling with ids when classes would do** — ids are for unique elements
  and in-page links; classes are for styling.
- **Putting `style.css` in the wrong place** — the `href` must match the file
  location relative to the HTML file. `href="style.css"` works when both are
  in the same folder.
- **Repeating rules** — if the same `color` appears in ten rules, consider
  one inherited rule on `body` instead.

## Recap

- The cascade decides conflicts: **specificity first** (id > class > type),
  then **order** (later wins), then **inheritance** for text properties.
- Use external stylesheets for real projects: one `style.css`, linked in the
  `<head>`.
- Organize with comment groups and purpose-named classes, and keep
  specificity low.

## What's next?

You have all the tools. The [final project](../final-project/README.md) puts
everything together: style the personal website you built in the HTML course
with one external `style.css`.
