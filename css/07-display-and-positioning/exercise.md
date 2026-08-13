# Exercise — A Badge on a Card

## 🎯 Goal

Build a small product card with an absolutely positioned "badge" in the
corner, plus a fixed bar that stays on screen while scrolling — using
`display` and `position`.

## 📚 What You Learned

- `display: block`, `inline`, `inline-block`, `none`
- `position: relative`, `absolute`, `fixed`
- Offsets: `top`, `right`, `bottom`, `left`
- The "position the parent" pattern for badges

## 📝 Task

1. Create `product-card.html` in the `07-display-and-positioning` folder.
2. Build a card:
   - A heading (product name) and a paragraph (description)
   - A badge in the top-right corner, hanging over the card's edge
   - Long enough content (or a few cards) that the page can scroll
3. Style it:
   - The card has `position: relative`
   - The badge has `position: absolute`, offset with `top` and `right`, a
     background color, and rounded corners
   - A fixed bar at the top of the page (for example "Free shipping!") that
     stays visible when you scroll
4. In the card text, include at least one inline element (`<span>` or
   `<strong>`) and one `inline-block` element, and style them so the
   difference is visible.

## Requirements

- [ ] The card uses `position: relative`
- [ ] The badge uses `position: absolute` with `top` and `right` offsets
- [ ] The fixed bar uses `position: fixed` and stays visible while scrolling
- [ ] An inline element styled (flows with text)
- [ ] An `inline-block` element styled (has its own width or padding)
- [ ] The badge is visibly different from the card (color, position)

## 💡 Hint

To make the badge hang over the card's corner, give it a **negative** offset:

```css
.badge {
    position: absolute;
    top: -12px;
    right: -12px;
}
```

And remember: the badge positions itself relative to the **nearest positioned
ancestor** — that is why the card needs `position: relative`.

## ⭐ Challenge

Add a second card with a badge that hangs over the **bottom-left** corner
(`bottom` and `left` with negative values). Then add a third card with no
badge at all. All three cards should use the same `card` class — only the
badge markup differs.

## ✅ Solution

Open `solution.html` **after** you have attempted the exercise and compare
your work. Scroll your page: the fixed bar should stay put, and each badge
should sit neatly on its card's corner.
