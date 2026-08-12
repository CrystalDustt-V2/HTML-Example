# Exercise — A Student Registration Form

## 🎯 Goal

Build a complete registration form using `form`, `label`, `input`,
`textarea`, `select`, `option`, and `button`.

## 📚 What You Learned

- The `<form>` element
- Input types: `text`, `email`, `password`, `number`, `date`, `checkbox`,
  `radio`
- `label` + `for` + `id`
- Attributes: `name`, `value`, `placeholder`, `required`
- `textarea`, `select` + `option`, `button`

## 📝 Task

1. Create a new file called `registration.html` with a complete HTML document.
2. Build a **Student Registration Form** that contains all of the following:
   - **Full name** — `text` input, required, with a placeholder
   - **Email** — `email` input, required
   - **Password** — `password` input
   - **Age** — `number` input
   - **Start date** — `date` input
   - **Study program** — a group of **radio** buttons with at least two
     choices, where exactly one can be selected
   - **Favorite subject** — a `select` dropdown with at least three `option`s
   - **Additional notes** — a `textarea`
   - **Agree to terms** — a `checkbox`
   - **Submit button** — a `button` with `type="submit"`
3. Give every field a `<label>` whose `for` attribute matches the input's `id`.

## Requirements

- [ ] The page is a complete, valid HTML document
- [ ] Every input has a connected `<label>` (`for` matches `id`)
- [ ] Every input has a `name` attribute
- [ ] `text`, `email`, `password`, `number`, `date`, `checkbox`, and `radio`
      types are all present
- [ ] The radio buttons share the same `name` and each has a `value`
- [ ] There is a `select` with at least three `option`s
- [ ] There is a `textarea`
- [ ] There is a `button` with `type="submit"`
- [ ] At least two fields use `required` (hint: full name and email)

## 💡 Hint

The `example.html` in this lesson already contains every piece you need. Read
it, then close it and write your own version. When the page is open in your
browser, try submitting the empty form — the `required` fields should stop you.

## ⭐ Challenge

Add a second checkbox "Send me the course newsletter" and a reset button
(`type="reset"`) next to the submit button. Try clicking the reset button after
filling the form — it clears everything.

## ✅ Solution

Open `solution.html` **after** you have attempted the exercise and compare your
work. Your form does not need to match — it just needs to contain every field
type listed above.
