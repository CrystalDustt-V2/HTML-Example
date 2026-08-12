# Lesson 10 — Semantic HTML

## What you will learn

- What semantic HTML is
- `<header>`, `<nav>`, `<main>`
- `<section>`, `<article>`, `<aside>`, `<footer>`
- Why semantic HTML is useful

---

## What is semantic HTML?

**Semantic** means *related to meaning*. A semantic element tells you what its
content **is**, not just how it looks.

Compare these two lines:

```html
<div>My Blog</div>          <!-- A generic container -->
<header>My Blog</header>    <!-- A page header -->
```

Both look identical in the browser. But the second one tells browsers, search
engines, and screen readers: *"this is the top of the page."*

In this lesson you will replace generic `<div>` containers with elements that
have meaning.

## The semantic elements

```html
<header>
    Top of the page: logo, page title, sometimes the navigation
</header>

<nav>
    The main navigation links
</nav>

<main>
    The main content of the page — unique to this page
</main>

<section>
    A themed group of content (like a chapter)
</section>

<article>
    A self-contained piece of content (a blog post, a news item)
</article>

<aside>
    Side content: related links, ads, author info
</aside>

<footer>
    Bottom of the page: copyright, contact links
</footer>
```

A typical page layout:

```html
<header>
    <h1>My Blog</h1>
    <nav>
        <a href="index.html">Home</a>
        <a href="about.html">About</a>
    </nav>
</header>

<main>
    <article>
        <h2>My first post</h2>
        <p>Today I learned semantic HTML.</p>
    </article>

    <article>
        <h2>My second post</h2>
        <p>Semantic elements make pages easier to understand.</p>
    </article>
</main>

<aside>
    <h2>About me</h2>
    <p>I am learning HTML.</p>
</aside>

<footer>
    <p>© 2026 My Blog</p>
</footer>
```

### When to use which?

- `<header>` — the top of the page (or the top of a section/article).
- `<nav>` — the main set of navigation links.
- `<main>` — the main content; there is only **one** per page.
- `<section>` — a group of related content inside a page.
- `<article>` — content that makes sense on its own, even outside the page.
- `<aside>` — content loosely related to the main content.
- `<footer>` — the bottom of the page (or of a section/article).

> An `<article>` can contain `<header>`s and `<section>`s; a `<section>` can
> contain `<article>`s. Think about the *meaning*, not the shape.

## Why does semantic HTML matter?

1. **Accessibility** — screen readers use the structure to help visually
   impaired visitors navigate (for example "jump to the main content").
2. **Search engines** — they use semantics to understand what a page is about.
3. **Readable code** — you (and other developers) can see at a glance what each
   part of the page is.
4. **Styling later** — when you learn CSS, you can target `header`, `footer`,
   etc. by name.

The browser shows the same result either way — the meaning is the difference.

## Common mistakes

- **Using `<div>` for everything** — reach for a semantic element first.
  Generic `<div>`s are fine when no semantic element fits.
- **More than one `<main>`** — exactly one per page.
- **Putting `<nav>` inside `<footer>` for every small link set** — `<nav>`
  is for the *main* navigation; small link collections in a footer can stay
  plain links.
- **Replacing every `<div>` blindly** — a `<div>` inside `<main>` that holds
  three buttons is still just a container. Use semantics where they fit.

## Recap

- Semantic elements describe *what* content is, not just how it looks.
- `<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<aside>`,
  `<footer>` cover the main page regions.
- One `<main>` per page; use `<article>` for self-contained content.
- Semantic HTML helps accessibility, search engines, and code readability.

## What's next?

You have finished all ten lessons! It is time to build the
[Final Project](../final-project/README.md): a personal website that uses
everything you have learned.
