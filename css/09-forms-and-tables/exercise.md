# Exercise — A Nice Form and Table

## 🎯 Goal

Style a registration form and a grades table so they look clean: consistent
fields, clear focus states, a real button, and a readable table.

## 📚 What You Learned

- Styling `input`, `textarea`, and `select`
- `:focus` styles for fields
- Button styling (`border: none`, `cursor: pointer`, `:hover`)
- `border-collapse: collapse` and table cell padding
- A distinct `thead` and zebra stripes

## 📝 Task

1. Create `registration.html` in the `09-forms-and-tables` folder.
2. Build a small form with at least three fields (for example name, email,
   and a message or a dropdown) and a submit button.
3. Build a small table (for example your class grades or a weekly schedule)
   with `thead` and `tbody`.
4. Style everything:
   - Fields share padding, a light border, and `border-radius`
   - Fields are `width: 100%`
   - A visible `:focus` style on fields
   - A button with padding, background, `border: none`, `cursor: pointer`,
     and a `:hover` color change
   - Table with `border-collapse: collapse`, cell padding, a colored `thead`,
     and zebra stripes

## Requirements

- [ ] At least three styled fields, all with the same border and padding
- [ ] A `:focus` rule that makes the active field obvious
- [ ] The button uses `border: none` and `cursor: pointer`
- [ ] A `:hover` rule for the button
- [ ] `border-collapse: collapse` on the table
- [ ] Zebra stripes using `nth-child(odd)` (or your own alternative)

## 💡 Hint

Group the field styling in one rule so all fields look the same:

```css
input, textarea, select {
    padding: 8px 10px;
    border: 1px solid #cccccc;
    border-radius: 4px;
    font-size: 16px;
    width: 100%;
}
```

Then add focus and button rules separately.

## ⭐ Challenge

Use `width: 100%` on the fields but limit the *form's* width so the form does
not stretch across the whole page (for example
`form { width: 400px; }`). Then add `border-radius` to the table's header
corners — or leave the table square and explain to yourself why it looks fine
either way.

## ✅ Solution

Open `solution.html` **after** you have attempted the exercise and compare
your work. Click into each field and tab through the form — every field
should clearly show where the focus is.
