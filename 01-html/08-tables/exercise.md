# Exercise — A Student Grade Table

## 🎯 Goal

Practice `table`, `tr`, `th`, `td`, `thead`, and `tbody` by building a grade
table for a class.

## 📚 What You Learned

- `<table>`, `<tr>`, `<th>`, `<td>`
- `<thead>` and `<tbody>`
- `colspan` and `rowspan` (basic)

## 📝 Task

1. Create a new file called `grades.html` with a complete HTML document.
2. Build a table with the header **Student** and at least three subjects of
   your choice (for example Math, English, Science).
3. Add at least **four** student rows. For each student, show:
   - the student's name in the first column (use `<th>` so the names stand out)
   - a grade for each subject in the following columns (use `<td>`)
4. Wrap the header row in `<thead>` and the student rows in `<tbody>`.
5. Below the main table, add a **second small table** that uses either
   `colspan` or `rowspan` at least once.

## Requirements

- [ ] The page is a complete, valid HTML document
- [ ] The main table has a header row with at least four `<th>` cells
- [ ] The main table has at least four `<tr>` data rows
- [ ] Each data row has the same number of `<td>` cells as the header has columns
- [ ] `<thead>` wraps the header row and `<tbody>` wraps the data rows
- [ ] The second table uses `colspan` or `rowspan` at least once
- [ ] Every `<table>` is properly closed

## 💡 Hint

Count the cells! If your header has four columns, every data row must have four
cells too. When you use `colspan="2"`, that one cell counts as two columns.

## ⭐ Challenge

Add a final row to the main table with a cell that uses `colspan` to span all
columns and shows the class average.

## ✅ Solution

Open `solution.html` **after** you have attempted the exercise and compare your
work. Your subjects and grades can be anything — the table structure is what
matters.
