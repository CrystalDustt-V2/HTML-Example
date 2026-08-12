# Lesson 05 — Links

## What you will learn

- The anchor element `<a>`
- The `href` attribute
- Links to other websites (absolute URLs)
- Opening links in a new tab with `target="_blank"`
- Links between your own pages (relative URLs)

---

## The anchor element

Links are created with the `<a>` element (short for *anchor*):

```html
<a href="https://www.wikipedia.org">Visit Wikipedia</a>
```

- `<a>` … `</a>` — the clickable text between the tags is what visitors see.
- `href="..."` — the **destination**: where the link goes when clicked.

The text inside the link should tell the visitor where they are going.
"Click here" tells them nothing; "Read the Wikipedia article on HTML" does.

## Links to other websites (absolute URLs)

An absolute URL contains the full address, including `https://`:

```html
<a href="https://developer.mozilla.org">MDN Web Docs</a>
```

## Opening a link in a new tab

By default, a link opens in the same tab. To open it in a **new tab**, add
`target="_blank"`:

```html
<a href="https://www.wikipedia.org" target="_blank">Wikipedia (new tab)</a>
```

> Use `target="_blank"` for external websites. For your own pages, keep the
> visitor in the same tab.

## Links between your own pages (relative URLs)

A **relative URL** points to another file next to your current file. It does
not need `https://` — just the file name (or folder path):

```html
<a href="about.html">About me</a>
<a href="pages/contact.html">Contact</a>
<a href="../index.html">Back to the home page</a>
```

| Path | Meaning |
|------|---------|
| `about.html` | `about.html` in the same folder |
| `pages/contact.html` | `contact.html` inside the `pages` folder |
| `../index.html` | `index.html` in the parent folder (`..` = one level up) |

## A small navigation example

```html
<p>
    <a href="index.html">Home</a> |
    <a href="about.html">About</a> |
    <a href="contact.html">Contact</a>
</p>
```

This is how simple navigations are built. (In
[Lesson 10](../10-semantic-html/README.md) you will learn the `<nav>` element
that gives such link lists a clear meaning.)

## Complete example

```html
<h1>My small website</h1>

<p>Welcome! Here are a few useful links:</p>

<p>
    <a href="about.html">About me</a> |
    <a href="contact.html">Contact</a> |
    <a href="https://www.wikipedia.org" target="_blank">Wikipedia</a>
</p>
```

## Common mistakes

- **Missing `href`** — `<a>About</a>` without `href` is not clickable.
- **Forgetting the quotes** — write `href="about.html"`, not `href=about.html`.
- **Wrong relative paths** — check the folder structure. If `contact.html` is
  inside `pages/`, the link is `pages/contact.html`.
- **`target="_blank"` on internal links** — keep your own pages in the same tab.
- **Vague link text** — prefer "Read the HTML guide" over "Click here".

## Recap

- `<a href="...">text</a>` creates a link; `href` is the destination.
- Absolute URLs (`https://...`) point to other websites.
- Relative URLs (`about.html`, `pages/contact.html`) point to your own files.
- `target="_blank"` opens the link in a new tab.
- Write link text that describes the destination.

## What's next?

[Lesson 06](../06-images/README.md) shows how to add images to your pages with
the `<img>` element.
