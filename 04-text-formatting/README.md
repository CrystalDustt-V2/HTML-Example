# Lesson 04 — Text Formatting

## What you will learn

- Emphasizing text: `<strong>` and `<em>`
- Presentational styles: `<b>`, `<i>`, `<u>`
- Highlighting and notes: `<mark>`, `<small>`
- Showing changes: `<del>` and `<ins>`
- Subscript and superscript: `<sub>` and `<sup>`
- The difference between *semantic* and *presentational* elements

---

## Making text bold and italic

```html
<p><strong>Important!</strong> Please read the notice below.</p>
<p>This is <em>really</em> interesting.</p>
```

- `<strong>` — marks text as **important**. Browsers usually show it bold.
- `<em>` — marks text with **emphasis** (stress). Browsers usually show it
  italic.

```html
<p><b>Bold</b> and <i>italic</i> are the visual versions.</p>
```

- `<b>` — bold text, with no extra meaning.
- `<i>` — italic text, with no extra meaning.

### Semantic vs. presentational — what's the difference?

This is the key idea of this lesson.

- **Semantic** elements describe what the text *means*:
  `<strong>` = *important*, `<em>` = *stressed*.
- **Presentational** elements describe how the text *looks*:
  `<b>` = *bold*, `<i>` = *italic*.

```html
<!-- Semantic: the text means "important" -->
<p><strong>Deadline is Friday.</strong></p>

<!-- Presentational: the text just looks bold -->
<p>The word <b>bold</b> is written in bold letters.</p>
```

Why care? Screen readers, search engines, and other programs use the *meaning*,
not the look. If a word is truly important, use `<strong>`. If you only want it
bold for appearance, `<b>` is fine.

> A general rule: use `<strong>` and `<em>` most of the time. Use `<b>` and
> `<i>` only when you want the look without the meaning.

## Underline, highlight, small print

```html
<p>Please <u>read the instructions</u> before starting.</p>
<p>Do not forget to <mark>save your work</mark>!</p>
<p><small>This footnote is printed in small letters.</small></p>
```

- `<u>` — underlined text (use sparingly; underlined text looks like a link).
- `<mark>` — highlighted text, like a marker pen. Browsers show it with a
  yellow background.
- `<small>` — "small print": disclaimers, footnotes, legal notes.

## Showing changes: deleted and inserted

```html
<p>The meeting is on <del>Monday</del> <ins>Tuesday</ins>.</p>
```

- `<del>` — text that has been **deleted** (usually shown with a line through it).
- `<ins>` — text that has been **inserted** (usually shown underlined).

## Subscript and superscript

```html
<p>Water is H<sub>2</sub>O.</p>
<p>The theory of relativity: E = mc<sup>2</sup>.</p>
```

- `<sub>` — **subscript**: smaller text below the line (H₂O, chemical formulas).
- `<sup>` — **superscript**: smaller text above the line (powers, exponents).

## Complete example

```html
<h1>About my project</h1>

<p>
    This project is <strong>very important</strong> to me. I started it
    <em>three years ago</em> and it is almost finished.
</p>

<p>
    <mark>Deadline: March 31.</mark>
</p>

<p>
    <del>Version 1.0 was released in January.</del>
    <ins>Version 1.1 is now available.</ins>
</p>

<p>
    The formula for water is H<sub>2</sub>O and the speed of light squared is
    c<sup>2</sup>.
</p>

<p><small>© 2026 My Project. All rights reserved.</small></p>
```

## Common mistakes

- **Using `<b>` when you mean `<strong>`** — if the text is important, use the
  semantic element.
- **Wrapping whole paragraphs in `<small>`** — `<small>` is for short notes,
  not for shrinking a full paragraph.
- **Forgetting the closing tag** — `<em>oops` has no `</em>`.
- **Nesting wrong** — formatting tags must open and close in the correct order:
  `<strong><em>correct</em></strong>`, not `<strong><em>wrong</strong></em>`.

## Recap

- `<strong>` = important (semantic, usually bold); `<em>` = emphasis (semantic,
  usually italic).
- `<b>` and `<i>` = bold and italic for looks only (presentational).
- `<u>` = underline, `<mark>` = highlight, `<small>` = small print.
- `<del>` = deleted text, `<ins>` = inserted text.
- `<sub>` = subscript (H₂O), `<sup>` = superscript (c²).

## What's next?

[Lesson 05](../05-links/README.md) shows how to create links so visitors can
move between pages and to other websites.
