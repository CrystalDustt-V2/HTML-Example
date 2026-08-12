# Lesson 02 — HTML Document Structure

## What you will learn

- The parts every HTML document needs
- `<!DOCTYPE html>`
- `<html>`
- `<head>` and `<title>`
- `<meta charset>`
- `<body>`

---

## Every web page has the same skeleton

Every HTML page you write — from a tiny note to a huge website — follows the
same basic structure:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Page title goes here</title>
</head>
<body>
    Everything visible on the page goes here.
</body>
</html>
```

Let's look at each part.

## `<!DOCTYPE html>`

```html
<!DOCTYPE html>
```

This line tells the browser: *"This document is written in modern HTML."* It is
not a tag — it is a *declaration*. It must be the **very first line** of your
file, before anything else.

> You do not need to understand the history behind it. Just remember: every
> HTML document starts with `<!DOCTYPE html>`.

## `<html>` — the root element

```html
<html lang="en">
    ...
</html>
```

Everything in the document lives inside `<html>`. The `lang="en"` attribute
tells the browser (and search engines) that the page is written in English.

## `<head>` — the invisible information

```html
<head>
    <meta charset="UTF-8">
    <title>Page title goes here</title>
</head>
```

The `<head>` contains **information about the page**, not the page's visible
content. Common items in the head:

- `<meta charset="UTF-8">` — tells the browser which character set to use, so
  letters like `é`, `ñ`, or `中` display correctly.
- `<title>...</title>` — the title shown in the browser tab and in search
  results. It is not shown on the page itself.

## `<body>` — the visible content

```html
<body>
    Everything the visitor sees goes here.
</body>
```

Headings, paragraphs, links, images — all of it lives inside `<body>`.

## A mini tour of a real page

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>My Recipe Blog</title>
</head>
<body>
    <h1>My Recipe Blog</h1>
    <p>Today I baked a chocolate cake.</p>
</body>
</html>
```

Open that in a browser and you will see the heading and paragraph. Look at the
browser tab: it shows **My Recipe Blog** — that's the `<title>` doing its job.

## Common mistakes

- **Forgetting `<!DOCTYPE html>`** — the page may render in "quirks mode" and
  behave unexpectedly.
- **Putting content inside `<head>`** — `<p>` and other visible elements belong
  in `<body>`.
- **Putting the `<title>` inside `<body>`** — it must live in `<head>`.
- **Closing tags in the wrong order** — tags must close in the reverse order
  they opened (like `</title>` before `</head>`).
- **More than one `<html>` or `<body>`** — there is exactly one of each.

## Recap

- `<!DOCTYPE html>` — declares an HTML document; always the first line.
- `<html>` — the root element that contains everything.
- `<head>` — invisible information about the page.
- `<title>` — the page title (shown in the browser tab).
- `<meta charset="UTF-8">` — makes special characters display correctly.
- `<body>` — everything the visitor sees.

## What's next?

Now that your documents have a proper skeleton, [Lesson 03](../03-headings-and-paragraphs/README.md)
shows you how to fill the `<body>` with headings and paragraphs.
