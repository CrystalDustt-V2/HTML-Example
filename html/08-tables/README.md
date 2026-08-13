# Lesson 08 — Tables

## What you will learn

- The `<table>` element
- Rows `<tr>`, header cells `<th>`, data cells `<td>`
- Table sections `<thead>` and `<tbody>`
- Merging cells with `colspan` and `rowspan` (basic)

---

## A basic table

Tables present data in rows and columns:

```html
<table>
    <tr>
        <th>Subject</th>
        <th>Grade</th>
    </tr>
    <tr>
        <td>Math</td>
        <td>A</td>
    </tr>
    <tr>
        <td>English</td>
        <td>B</td>
    </tr>
</table>
```

The parts:

| Element | Name | What it is |
|---------|------|------------|
| `<table>` | Table | The whole table |
| `<tr>` | Table row | One horizontal row |
| `<th>` | Table header cell | A column heading (bold by default) |
| `<td>` | Table data cell | One data cell |

A `<tr>` contains the cells of one row. The first row here contains the
headings `Subject` and `Grade`; the following rows contain the data.

## `<thead>` and `<tbody>` — grouping rows

For longer tables you can group the rows. `<thead>` holds the header row(s),
`<tbody>` holds the data rows:

```html
<table>
    <thead>
        <tr>
            <th>Subject</th>
            <th>Grade</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Math</td>
            <td>A</td>
        </tr>
        <tr>
            <td>English</td>
            <td>B</td>
        </tr>
    </tbody>
</table>
```

This makes the structure of the table explicit: the heading part and the data
part. (There is also `<tfoot>` for footer rows — you can meet it later.)

## Merging cells: `colspan` and `rowspan`

Sometimes a cell should span several columns or rows.

- `colspan="2"` — the cell stretches across **two columns**:

```html
<tr>
    <td colspan="2">This cell fills two columns</td>
</tr>
```

- `rowspan="2"` — the cell stretches across **two rows**:

```html
<tr>
    <td rowspan="2">This cell fills two rows</td>
    <td>First</td>
</tr>
<tr>
    <td>Second</td>
</tr>
```

> Use `colspan` and `rowspan` sparingly. Simple tables are easier to read and
> easier to maintain. One merged cell in a lesson exercise is plenty.

## Complete example

```html
<h1>Report card — Spring 2026</h1>

<table>
    <thead>
        <tr>
            <th>Subject</th>
            <th>First term</th>
            <th>Second term</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Math</td>
            <td>B</td>
            <td>A</td>
        </tr>
        <tr>
            <td>English</td>
            <td>A</td>
            <td>A</td>
        </tr>
    </tbody>
</table>
```

## Common mistakes

- **Forgetting `<tr>`** — cells must live inside rows.
- **Putting `<td>` directly inside `<table>`** — every cell belongs to a `<tr>`.
- **Mismatched cell counts** — each row should have the same number of cells
  (unless you use `colspan`/`rowspan`).
- **Using tables for layout** — tables are for *data*, not for arranging the
  look of a page (that is what CSS is for).
- **Forgetting `</table>`** — close the table.

## Recap

- `<table>` → `<tr>` (rows) → `<th>` (headers) / `<td>` (data cells).
- `<thead>` groups the header rows; `<tbody>` groups the data rows.
- `colspan="n"` merges a cell across `n` columns; `rowspan="n"` across `n`
  rows.

## What's next?

[Lesson 09](../09-forms/README.md) shows how to build forms so visitors can
type text, pick options, and press buttons.
