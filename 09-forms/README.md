# Lesson 09 — Forms

## What you will learn

- The `<form>` element
- `<label>` and the `for` attribute
- `<input>` and common input types
- `<textarea>`, `<select>`, and `<option>`
- `<button>`
- Important attributes: `id`, `name`, `value`, `placeholder`, `required`

---

Forms let visitors type text, choose options, and press buttons — think login
pages, search boxes, and registration forms. In this lesson you will build the
**structure** of a form. (What happens to the data after the button is pressed
needs a server — that is outside this course.)

## The `<form>` element

Everything in a form lives inside `<form>`:

```html
<form>
    ...form fields go here...
</form>
```

## Text input with a label

Every field needs a `<label>` so visitors (and screen readers) know what to
type:

```html
<label for="name">Your name</label>
<input type="text" id="name" name="name">
```

Three attributes work together:

- `for="name"` on the label points to the input with `id="name"`.
- `id` gives the field a unique name on the page — used by the label.
- `name` is the field's name for when the form data is sent.

> Clicking a label focuses its input field. That small detail makes forms much
> easier to use.

## Common input types

```html
<input type="text" ...>      <!-- single line of text -->
<input type="email" ...>     <!-- an email address -->
<input type="password" ...>  <!-- hidden characters -->
<input type="number" ...>    <!-- a number -->
<input type="date" ...>      <!-- a date picker -->
```

`type` changes how the browser renders the field and what it accepts. For
example, `type="email"` makes the browser warn about `hello` without an `@`.

### Checkbox and radio

- **Checkbox** — one or more independent options:

```html
<label for="news">Send me news</label>
<input type="checkbox" id="news" name="newsletter">
```

- **Radio** — exactly one choice from a group. All radios in the group share
  the same `name`:

```html
<input type="radio" id="fulltime" name="schedule" value="full-time">
<label for="fulltime">Full time</label>

<input type="radio" id="parttime" name="schedule" value="part-time">
<label for="parttime">Part time</label>
```

Each radio needs a `value` — that is what gets sent when it is chosen.

## Useful attributes

| Attribute | What it does |
|-----------|--------------|
| `id` | A unique name for the field on the page (used by labels) |
| `name` | The field's name when data is submitted |
| `value` | The field's initial value (or the value of a radio/option) |
| `placeholder` | Grey hint text inside the field (not a value!) |
| `required` | The field must be filled in before submitting |

```html
<input type="text" name="city" placeholder="e.g. Springfield" required>
```

## `<textarea>` — longer text

For multi-line text (messages, comments):

```html
<label for="message">Your message</label>
<textarea id="message" name="message" rows="5" cols="40">
Default text goes between the tags.
</textarea>
```

`rows` and `cols` set the visible size. Unlike `<input>`, `<textarea>` has a
closing tag.

## `<select>` and `<option>` — a dropdown

```html
<label for="country">Country</label>
<select id="country" name="country">
    <option value="">Please choose…</option>
    <option value="us">United States</option>
    <option value="uk">United Kingdom</option>
</select>
```

- `<select>` is the dropdown; each `<option>` is one choice.
- The `value` of an option is what gets sent; the text between the tags is what
  the visitor sees.

## `<button>`

```html
<button type="submit">Register</button>
```

- `type="submit"` — submits the form (the default).
- `type="reset"` — clears the form.
- `type="button"` — a plain button that does nothing by itself.

## A complete registration form

```html
<h1>Student registration</h1>

<form>
    <label for="fullname">Full name</label>
    <input type="text" id="fullname" name="fullname" placeholder="e.g. Alex Smith" required>

    <label for="email">Email</label>
    <input type="email" id="email" name="email" required>

    <label for="password">Password</label>
    <input type="password" id="password" name="password">

    <label for="birthdate">Date of birth</label>
    <input type="date" id="birthdate" name="birthdate">

    <p>Schedule</p>
    <input type="radio" id="fulltime" name="schedule" value="full-time">
    <label for="fulltime">Full time</label>
    <input type="radio" id="parttime" name="schedule" value="part-time">
    <label for="parttime">Part time</label>

    <label for="course">Course</label>
    <select id="course" name="course">
        <option value="">Please choose…</option>
        <option value="html">HTML</option>
        <option value="python">Python</option>
    </select>

    <label for="message">Anything else?</label>
    <textarea id="message" name="message" rows="4" cols="40"></textarea>

    <input type="checkbox" id="terms" name="terms">
    <label for="terms">I agree to the terms</label>

    <button type="submit">Register</button>
</form>
```

## Common mistakes

- **Missing `for`/`id` pairs** — a label without `for` is not connected to its
  field.
- **Missing `name`** — a field without `name` sends no data.
- **Two inputs with the same `id`** — `id` must be unique on the page.
- **`placeholder` instead of `value`** — placeholder is grey hint text that
  disappears; it is not a submitted value.
- **Radio buttons with different `name`s** — radios must share a `name` to work
  as a group.
- **Forgetting the closing `</form>`** — close the form.

## Recap

- `<form>` wraps all fields; `<label for="...">` + `id` connects labels to
  fields.
- `<input type="text|email|password|number|date|checkbox|radio">` covers most
  fields.
- `<textarea>` is for multi-line text; `<select>` + `<option>` makes a dropdown.
- `<button type="submit">` submits the form.
- `id` (unique), `name` (submitted), `value` (sent value), `placeholder`
  (hint), `required` (mandatory).

## What's next?

[Lesson 10](../10-semantic-html/README.md) — the last lesson — shows how to give
your page's sections real meaning with semantic HTML.
