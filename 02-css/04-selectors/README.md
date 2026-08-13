# Lesson 04 — Selectors

## What you will learn

- Type selectors (`h1`, `p`, …)
- Class selectors (`.intro`)
- Id selectors (`#header`)
- Grouping selectors (`h1, h2`)
- Descendant selectors (`nav a`)
- When to use a class vs. an id

---

So far you have styled elements by their **type**: `h1`, `p`, `body`. That
styles *every* element of that type. Selectors let you be more precise.

## Type selector

Targets every element of a type:

```css
p {
    color: gray;
}
```

Every `<p>` on the page turns gray.

## Class selector

A **class** is a label you add to HTML elements yourself. In HTML:

```html
<p class="intro">Welcome to my page.</p>
<p>Normal paragraph.</p>
```

In CSS, a class selector starts with a dot `.`:

```css
.intro {
    font-size: 20px;
    color: darkblue;
}
```

Now only the paragraph with `class="intro"` is affected. Key facts:

- One class can be used on **many** elements.
- One element can have **several** classes, separated by spaces:
  `<p class="intro important">`.
- Class names are your choice — keep them meaningful: `intro`, `warning`,
  `price`, not `red-text` or `big-1`.

## Id selector

An **id** is a unique label for a single element:

```html
<h1 id="site-title">My Website</h1>
```

In CSS, an id selector starts with `#`:

```css
#site-title {
    color: teal;
}
```

Key facts:

- An id must be **unique** on the page — only one element may have
  `id="site-title"`.
- Class names use a dot (`.`), ids use a hash (`#`).

### Class vs. id — which do I use?

| | Class | Id |
|---|-------|-----|
| Written | `.name` | `#name` |
| Used | on many elements | on exactly one element |
| Typical use | styling groups (buttons, cards, highlights) | identifying one special element (header, main content) |

Start with **classes**. Use ids when you need a unique, one-of-a-kind element
(and remember: ids are also used for in-page links, like `href="#about"` from
the HTML course).

## Grouping selector

Apply the same rule to several selectors by separating them with commas:

```css
h1, h2, h3 {
    font-family: Georgia, serif;
}
```

This is the same as writing three separate rules, but shorter.

## Descendant selector

Targets elements *inside* other elements. Write the ancestor, a space, then
the descendant:

```css
nav a {
    color: white;
}
```

This styles only the links **inside** a `nav` — other links on the page are
untouched.

```css
article p {
    line-height: 1.6;
}
```

Paragraphs inside `article` get the line height; paragraphs elsewhere do not.

## Common mistakes

- **Forgetting the dot or hash** — `intro { }` styles nothing; it must be
  `.intro`. And `header { }` styles the HTML `<header>` element, while
  `#header` styles the element with `id="header"`.
- **Reusing an id** — an id must appear once per page. Use a class if you
  need the style on several elements.
- **Making everything an id** — ids are for unique elements. Styling ten
  elements with ten different ids is worse than giving them one class.
- **Meaningless names** — `.red` breaks when you later change the color.
  Name classes by *purpose*: `.warning`, `.highlight`, `.price`.

## Recap

- **Type** selectors (`p`) target every element of that type.
- **Class** selectors (`.intro`) target every element with that class.
- **Id** selectors (`#site-title`) target the single element with that id.
- Separate selectors with commas to **group**; separate with a space for
  **descendants** (`nav a`).
- Use classes for groups, ids for unique elements.

## What's next?

Elements have size and spacing around them — the subject of
[Lesson 05](../05-box-model/README.md), the box model.
