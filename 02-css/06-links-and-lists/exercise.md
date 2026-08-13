# Exercise — A Fancy Menu and a Reading List

## 🎯 Goal

Style a navigation menu and a reading list: link states, no-bullet menus, and
styled list markers.

## 📚 What You Learned

- Link states: `:link`, `:visited`, `:hover`, `:active` (in that order)
- `:focus` and why not to remove it
- `list-style-type` and the three-part menu reset
- Links as "button" menu items with padding and background

## 📝 Task

1. Create `my-menu.html` in the `06-links-and-lists` folder.
2. Build:
   - A `<nav>` with a `<ul>` of four links (Home, About, Projects, Contact)
   - A "reading list" section with a `<h2>` and a `<ul>` of at least three
     books or articles
3. Style the nav:
   - No bullets and no indent (the three-part reset)
   - Links with padding and a background color, so they look like buttons
   - A different background on `:hover`, and an underline or color change on
     `:focus`
4. Style the reading list with `list-style-type` set to something other than
   the default (square, circle, or lower-alpha).

## Requirements

- [ ] All four link states are styled, in the order link, visited, hover,
      active
- [ ] `nav ul` has `list-style-type: none; margin: 0; padding: 0;`
- [ ] Nav links have padding and a background color
- [ ] `:hover` changes the nav link background
- [ ] A visible `:focus` style (never just remove the outline)
- [ ] The reading list uses a non-default `list-style-type`

## 💡 Hint

The three-part reset has to go on the `ul`, not on the links:

```css
nav ul {
    list-style-type: none;
    margin: 0;
    padding: 0;
}
```

If your bullets are still there, check that the reset is on the `ul` (or on
`ul` *and* `ol` if you use both).

## ⭐ Challenge

Give the four menu links different styles: make the "Home" link stand out
(for example a lighter background), using a class such as
`class="active"` on that one link. Then add `border-radius` to the nav links
so the menu looks rounded.

## ✅ Solution

Open `solution.html` **after** you have attempted the exercise and compare
your work. Hover over both menus and tab through the links — every link
should give clear feedback.
