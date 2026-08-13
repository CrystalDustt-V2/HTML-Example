# Exercise — Build a Card

## 🎯 Goal

Build a "profile card" and control its box model: content, padding, border,
and margin — plus a centered page element.

## 📚 What You Learned

- The four layers of the box: content, padding, border, margin
- `padding` (all sides, two values, four values)
- `border` and `border-radius`
- `margin`, including `margin: 0 auto` for centering

## 📝 Task

1. Create `profile-card.html` in the `05-box-model` folder.
2. Build a card that looks like a small profile:
   - A heading with a name
   - A paragraph about the person
   - A list of two or three hobbies
3. Style it:
   - The card has `padding` on all sides (15–25px)
   - A visible `border` with `border-radius`
   - A background color, so you can *see* the padding
   - `margin` between the card and the rest of the page
   - The card is centered horizontally (use a fixed `width` +
     `margin: 0 auto`)
4. Add a second, smaller box (for example a "contact me" button) with its
   own padding, background, and rounded corners.

## Requirements

- [ ] One rule sets padding with two values (`padding: 10px 20px;` style)
- [ ] A border with a width, a style, and a color
- [ ] `border-radius` on the card and on the button
- [ ] A background color on the card (to make padding visible)
- [ ] The card is centered with `margin: 0 auto`
- [ ] The button has different padding than the card

## 💡 Hint

```css
.card {
    width: 360px;
    margin: 0 auto;
    padding: 20px 25px;
    border: 2px solid #1f4e79;
    border-radius: 10px;
    background-color: #eef4fb;
}
```

Change one value at a time and refresh to see what each layer does.

## ⭐ Challenge

Add `padding` and `background-color` to the hobby list items so each hobby
looks like a small tag or chip:

```css
li {
    display: inline-block;
    padding: 4px 10px;
    background-color: #dbe9f7;
    border-radius: 12px;
    margin-right: 6px;
}
```

(You will learn what `display: inline-block` does in
[Lesson 07](../07-display-and-positioning/README.md) — using it here is a
teaser.)

## ✅ Solution

Open `solution.html` **after** you have attempted the exercise and compare
your work. Measure the spaces in both versions — the card's layers should be
easy to point at in your browser.
