# Lesson 03 — Headings and Paragraphs

## What you will learn

- Headings `<h1>` through `<h6>`
- Paragraphs `<p>`
- Line breaks `<br>`
- Horizontal rules `<hr>`

---

## Headings — the titles of your page

Headings structure your content, just like titles and subtitles in a book.
HTML gives you **six levels**:

```html
<h1>Level 1 — the main title</h1>
<h2>Level 2 — section title</h2>
<h3>Level 3 — subsection title</h3>
<h4>Level 4</h4>
<h5>Level 5</h5>
<h6>Level 6 — the smallest</h6>
```

Rules of thumb:

- Use **one `<h1>`** per page — it is the main title.
- Use `<h2>` for the major sections under it, `<h3>` for subsections, and so on.
- Jumping from `<h1>` straight to `<h4>` is bad practice — go level by level.

```html
<h1>My School</h1>

<h2>History</h2>
<p>...text about the school's history...</p>

<h2>Facilities</h2>
<p>...text about the facilities...</p>
```

## Paragraphs — blocks of text

A paragraph is a block of text wrapped in `<p>`:

```html
<p>This is the first paragraph.</p>
<p>This is the second paragraph.</p>
```

The browser automatically adds space between paragraphs, so you do **not** use
empty lines or multiple spaces to create gaps — a new `<p>` does that for you.

> Pressing **Enter** inside your source code does **not** create a new line on
> the page. The browser collapses whitespace: several spaces and newlines in
> your code become a single space on the page.

## Line break — `<br>`

`<br>` forces a new line *inside* a paragraph. It is an **empty element**: it
has no content and no closing tag.

```html
<p>
    First street<br>
    Second street<br>
    Third street
</p>
```

## Horizontal rule — `<hr>`

`<hr>` draws a horizontal line across the page. Use it to separate topics.
Like `<br>`, it is an empty element with no closing tag.

```html
<p>End of the first section.</p>
<hr>
<p>Start of the second section.</p>
```

## A complete example

```html
<h1>My School</h1>

<p>Welcome to the page about my school.</p>

<h2>History</h2>
<p>Our school was founded in 1995.</p>
<p>It started with only forty students.</p>

<h2>Contact</h2>
<p>
    School office<br>
    12 Main Street<br>
    Springfield
</p>

<hr>

<p>This page was written in Lesson 03.</p>
```

## Common mistakes

- **Using `<br>` to create paragraphs** — use `<p>` for paragraphs and `<br>`
  only for a single line break inside a paragraph.
- **Using headings to make text big or bold** — headings describe structure,
  not size. If you want a small sub-note, don't use `<h6>`; use a `<p>`.
  (Making text look different is a job for Lesson 04 and, later, CSS.)
- **Skipping heading levels** — go `<h1>` → `<h2>` → `<h3>` in order.
- **Forgetting to close `<p>`** — every paragraph needs `</p>`.

## Recap

- `<h1>` to `<h6>` create headings; use one `<h1>` per page and go level by level.
- `<p>` creates a paragraph; browsers space paragraphs automatically.
- `<br>` forces a line break inside a paragraph (no closing tag).
- `<hr>` draws a horizontal separator line (no closing tag).

## What's next?

[Lesson 04](../04-text-formatting/README.md) shows how to format text *inside*
your headings and paragraphs — bold, italic, highlighted, and more.
