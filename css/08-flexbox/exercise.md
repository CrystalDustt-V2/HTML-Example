# Exercise — A Flexbox Layout

## 🎯 Goal

Build a page with a flexbox navigation bar and a row of three cards, plus a
perfectly centered element — using only flex properties.

## 📚 What You Learned

- `display: flex` on a container
- `flex-direction` (row / column)
- `justify-content` and `align-items`
- `gap` between items

## 📝 Task

1. Create `flex-layout.html` in the `08-flexbox` folder.
2. Build:
   - A `<nav>` with a site name on the left and three links on the right
   - A row of **three cards** (heading + paragraph each)
   - A centered box ("sign up" area) in the middle of the page
3. Style it with flexbox:
   - The nav uses `display: flex` + `justify-content: space-between`
   - The cards use `display: flex` + `gap` and each card grows equally
     (`flex: 1`)
   - The centered box uses `justify-content: center` +
     `align-items: center` and a fixed `height`
4. Bonus: make the page wrap gracefully — when the window is narrow, the
   cards should stack instead of squishing (add `flex-wrap: wrap` to the
   cards container).

## Requirements

- [ ] `display: flex` on the nav, the cards container, and the centered box
- [ ] `justify-content: space-between` on the nav
- [ ] `gap` on the cards container
- [ ] `flex: 1` on each card
- [ ] `justify-content: center` and `align-items: center` on the centered box
- [ ] No `position` or `float` used anywhere (that is the point of the
      exercise)

## 💡 Hint

Structure first, flex second. Your containers need to *exist* before they can
be flex containers:

```html
<nav>
    <strong>My Site</strong>
    <div>
        <a href="#">Home</a>
        <a href="#">About</a>
        <a href="#">Contact</a>
    </div>
</nav>
```

Then `display: flex` on `nav` puts the two children (brand and links) on one
line, and `space-between` pushes them apart.

## ⭐ Challenge

Add a footer that uses `flex-direction: column` with `align-items: center`,
containing two short lines of text. Then shrink the browser window — the
three cards should wrap below each other thanks to `flex-wrap: wrap`.

## ✅ Solution

Open `solution.html` **after** you have attempted the exercise and compare
your work. Resize your window and watch both layouts respond.
