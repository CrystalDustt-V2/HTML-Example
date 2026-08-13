# Lesson 01 — Introduction to CSS

## What you will learn

- What CSS is and what it does
- The parts of a CSS rule: selector, property, value
- The three ways to add CSS to a page
- CSS comments
- Basic syntax and common mistakes

---

## What is CSS?

**CSS** stands for **Cascading Style Sheets**. It is the language that decides
how a web page *looks*.

HTML builds the **structure** — "this is a heading, this is a paragraph, this
is a list." CSS builds the **style** — "headings are dark blue and large,
paragraphs are gray, this list has no bullets."

```
HTML = what the page contains
CSS  = how the page looks
```

The same HTML can look completely different with different CSS. Try opening
`example.html` in your browser, then change a color in the `<style>` block and
refresh — the page changes without touching any HTML.

> CSS is **not** a programming language. It is a *style sheet* language: it
> describes how content should be displayed.

## CSS rules

A **rule** is the basic building block of CSS. It has three parts:

```css
selector {
    property: value;
}
```

- **Selector** — *which* elements the rule applies to (for example `h1` means
  "every `<h1>` element").
- **Property** — *what* you want to change (for example `color`).
- **Value** — *how* you want to change it (for example `darkblue`).

Here is a real rule:

```css
h1 {
    color: darkblue;
    font-size: 32px;
}
```

This rule says: "for every `<h1>`, make the text color dark blue and the font
size 32 pixels."

Rules to remember:

- A rule starts with a selector and ends with a closing brace `}`.
- Each declaration is `property: value;` — a colon `:` after the property and
  a semicolon `;` after the value.
- One rule can contain as many declarations as you need.

## Three ways to add CSS

### 1. External stylesheet (best for real projects)

CSS lives in its own file, usually called `style.css`, and the HTML links to
it with one line in the `<head>`:

```html
<link rel="stylesheet" href="style.css">
```

One stylesheet can style **many pages** — that is why real websites use this
method. We use it in [Lesson 10](../10-cascade-and-best-practices/README.md)
and in the final project.

### 2. Embedded stylesheet (what this course uses in examples)

CSS lives inside a `<style>` element in the `<head>` of the page:

```html
<head>
    <style>
        h1 {
            color: darkblue;
        }
    </style>
</head>
```

This is convenient for small pages and for learning, because the HTML and CSS
are in one file.

### 3. Inline style (avoid unless you have to)

CSS is written directly on an element with the `style` attribute:

```html
<h1 style="color: darkblue;">Hello</h1>
```

This only affects that one element, mixes style into your HTML, and is hard to
maintain. You will meet it, but prefer the other two ways.

## CSS comments

Comments are notes for humans that the browser ignores:

```css
/* This is a CSS comment. */
/* They can also span
   multiple lines. */
```

Use them to explain what a rule does:

```css
/* Make the main heading stand out */
h1 {
    color: darkblue;
    font-size: 32px;
}
```

## Common mistakes

- **Missing semicolons** — `color: darkblue` without the `;` confuses the
  browser. Always end a declaration with `;`.
- **Missing closing brace** — every rule needs `}` at the end.
- **Colon vs. equals** — it is `color: darkblue;`, never `color = darkblue`.
- **Typos in property names** — `colour:` (British spelling) is not a CSS
  property; it is `color:`. The browser silently ignores unknown properties,
  so the rule simply does nothing.
- **Applying a rule to the wrong element** — `p { color: red; }` colors
  paragraphs, not the whole page. If the page does not change, check your
  selector first.

## Recap

- CSS controls **how** a page looks; HTML controls **what** is on it.
- A rule is `selector { property: value; }`.
- The three ways to add CSS: external file, embedded `<style>`, inline
  `style` attribute.
- Comments are written `/* ... */`.
- End every declaration with a semicolon and every rule with a brace.

## What's next?

Now that you know the shape of CSS, [Lesson 02](../02-colors-and-backgrounds/README.md)
shows you how to add colors to text and backgrounds.
