# Lesson 01 — Introduction to HTML

## What you will learn

- What HTML is and what it does
- Elements and tags
- Opening and closing tags
- Attributes
- HTML comments
- Basic syntax

---

## What is HTML?

**HTML** stands for **HyperText Markup Language**. It is the language used to
structure content on the web.

When you open a web page, your browser reads HTML and turns it into the page you
see. HTML tells the browser:

- "This is a heading."
- "This is a paragraph."
- "This is a link."
- "This is an image."

Think of HTML as the **skeleton** of a web page. It decides what the parts are
and how they are ordered. (CSS and JavaScript add the looks and the behavior —
but this course uses HTML only.)

> HTML is **not** a programming language. It is a *markup* language: it
> describes the structure of content with tags.

## Elements and tags

An **element** is one piece of content on a page. Most elements are written
with a pair of **tags**:

```html
<p>Hello world!</p>
```

Let's look at that line piece by piece:

| Part | Name | What it does |
|------|------|--------------|
| `<p>` | Opening tag | Marks the start of the element |
| `Hello world!` | Content | The actual text of the element |
| `</p>` | Closing tag | Marks the end of the element |

Rules to remember:

- The closing tag is the same word as the opening tag, but with a `/` before it.
- Tags are written with **angle brackets** `<` and `>`.
- HTML tag names are usually written in lowercase: `<p>`, not `<P>`.

### Opening and closing tags

Most elements need **both** an opening tag and a closing tag:

```html
<p>This paragraph has a proper closing tag.</p>
```

A few elements are *empty* — they have no content and no closing tag. You will
meet them in later lessons (for example `<br>`, `<hr>`, and `<img>`).

## Attributes

Attributes are extra information you can add to the **opening** tag. They are
written as `name="value"`:

```html
<a href="https://example.com">Visit Example</a>
```

Here `href="https://example.com"` is an attribute. It tells the link where to
go. We will study links in detail in [Lesson 05](../05-links/README.md) — for
now, just notice the shape: `name="value"` inside the opening tag.

## HTML comments

Comments are notes for humans that the browser ignores:

```html
<!-- This is a comment. The browser will not show it. -->
```

Comments are useful for:

- Explaining what a piece of code does
- Leaving reminders for yourself
- Temporarily hiding code

They start with `<!--` and end with `-->`.

## Basic syntax — a full (mini) page

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>My First Page</title>
</head>
<body>
    <!-- My first HTML comment -->
    <h1>Hello, world!</h1>
    <p>This is my very first web page.</p>
</body>
</html>
```

You do not need to understand every line yet. The parts around `<body>` — the
`<!DOCTYPE html>` line, `<html>`, `<head>`, and `<title>` — are the document
structure, and [Lesson 02](../02-document-structure/README.md) explains them in
detail. For now, focus on the tags, elements, attributes, and comments.

## Common mistakes

- **Forgetting the closing tag** — `<p>Hello` without `</p>` confuses the
  browser about where the element ends.
- **Mismatched closing tags** — `<p>Hello</h1>` is wrong: the closing tag must
  match the opening tag.
- **Typos in tag names** — `<pragraph>` is not a tag. Browsers usually ignore
  unknown tags, so your text may simply not be formatted.
- **Missing quotes around attribute values** — always write
  `href="https://example.com"`, not `href=https://example.com`.
- **Using capital letters in tag names** — write `<p>` and `</p>`, not `<P>`.

## Recap

- HTML is the markup language that structures web content.
- An **element** is content wrapped in tags.
- Most elements need an **opening tag** and a **closing tag**.
- **Attributes** add extra information to the opening tag: `name="value"`.
- **Comments** (`<!-- ... -->`) are notes that the browser ignores.

## What's next?

Now that you know what HTML looks like, [Lesson 02](../02-document-structure/README.md)
explains the parts that every proper HTML document needs.
