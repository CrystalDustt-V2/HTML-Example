# Lesson 07 — Lists

## What you will learn

- Unordered lists `<ul>` with `<li>` items
- Ordered lists `<ol>` with `<li>` items
- Nested lists (lists inside lists)

---

## Unordered lists — bullets

Use `<ul>` (unordered list) when the order does not matter. Each item is an
`<li>` (list item):

```html
<ul>
    <li>Apples</li>
    <li>Bananas</li>
    <li>Oranges</li>
</ul>
```

The browser shows a bullet (•) before each item.

## Ordered lists — numbers

Use `<ol>` (ordered list) when the order matters — steps, rankings, recipes:

```html
<ol>
    <li>Wash the fruit.</li>
    <li>Cut it into pieces.</li>
    <li>Put it in a bowl.</li>
</ol>
```

The browser numbers the items automatically: 1, 2, 3.

### Which one should you use?

- The items have an order that matters → `<ol>` (steps, rankings, top 10 lists).
- The order does not matter → `<ul>` (ingredients, hobbies, features).

## The parts

```html
<ul>   <!-- opening tag of the list -->
    <li>First item</li>   <!-- one list item -->
    <li>Second item</li>  <!-- another list item -->
</ul>  <!-- closing tag of the list -->
```

- A list contains **only `<li>` elements** directly inside it.
- An `<li>` may contain other things too (text, links, images…), not just text.

## Nested lists — lists inside lists

A list item can contain another list. This creates sub-levels, like a table of
contents:

```html
<ul>
    <li>Fruits
        <ul>
            <li>Apples</li>
            <li>Bananas</li>
        </ul>
    </li>
    <li>Vegetables
        <ul>
            <li>Carrots</li>
            <li>Onions</li>
        </ul>
    </li>
</ul>
```

Notice the pattern: the inner `<ul>` sits **inside** an `<li>` of the outer
list. The browser indents the nested list automatically.

You can mix list types while nesting — for example a numbered list inside a
bulleted list.

## Complete example

```html
<h1>Pancake recipe</h1>

<h2>Ingredients</h2>
<ul>
    <li>200 g flour</li>
    <li>2 eggs</li>
    <li>300 ml milk</li>
</ul>

<h2>Steps</h2>
<ol>
    <li>Mix the flour and eggs.</li>
    <li>Add the milk slowly while stirring.</li>
    <li>Bake each pancake for two minutes.</li>
</ol>
```

## Common mistakes

- **Putting text directly inside the list** — `<ul>` may only contain `<li>`
  elements. Text like `<ul>Apples</ul>` is invalid.
- **Forgetting the `</li>` or `</ul>`** — close every item and every list.
- **Using lists for indentation** — nested lists are for *related* content,
  not for creating indented text.
- **Nesting a list outside an `<li>`** — a list inside a list must live inside
  an `<li>`.

## Recap

- `<ul>` — unordered list, shown with bullets.
- `<ol>` — ordered list, shown with numbers.
- `<li>` — one list item, used inside `<ul>` or `<ol>`.
- Lists can be nested: put an inner list inside an `<li>` of the outer list.

## What's next?

[Lesson 08](../08-tables/README.md) shows how to present data in rows and
columns with tables.
