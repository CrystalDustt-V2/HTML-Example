# Lesson 05 — The Box Model

## What you will learn

- That every element is a box
- `padding` — space inside the border
- `border` — the edge of the box
- `margin` — space outside the border
- How `width` and `height` fit in

---

## Every element is a box

In CSS, every element on the page is a **box**. A paragraph, a heading, an
image — each one is a rectangle. The box model describes the four layers of
that rectangle:

```
┌─────────────────────────────────────────────┐
│                 margin                      │
│  ┌───────────────────────────────────────┐  │
│  │              border                   │  │
│  │  ┌─────────────────────────────────┐  │  │
│  │  │            padding              │  │  │
│  │  │  ┌───────────────────────────┐  │  │  │
│  │  │  │         content           │  │  │  │
│  │  │  │  (text, images, etc.)     │  │  │  │
│  │  │  └───────────────────────────┘  │  │  │
│  │  └─────────────────────────────────┘  │  │
│  └───────────────────────────────────────┘  │
└─────────────────────────────────────────────┘
```

From the **inside out**:

1. **Content** — the actual text or image.
2. **Padding** — space between the content and the border. It is *inside* the
   element, so it shows the element's background color.
3. **Border** — a visible (or invisible) line around the padding.
4. **Margin** — space *outside* the border, between this element and the next.

## Padding

Space inside the element, around the content:

```css
.card {
    padding: 20px;          /* 20px on all four sides */
}
```

You can set each side separately:

```css
.card {
    padding-top: 10px;
    padding-right: 20px;
    padding-bottom: 10px;
    padding-left: 20px;
}
```

Shorthand order (top, right, bottom, left — clockwise):

```css
.card {
    padding: 10px 20px 10px 20px;
}
```

If you give only two values, the first is top/bottom and the second is
left/right:

```css
.card {
    padding: 10px 20px;    /* 10px top & bottom, 20px left & right */
}
```

Padding shows the background color of the element, which is why a "button"
looks padded when you add `background-color` + `padding`.

## Border

A line around the padding:

```css
.card {
    border: 2px solid #333333;
}
```

The shorthand is: **width**, **style**, **color**.

```css
border: 2px solid #333333;   /* solid line */
border: 1px dashed gray;     /* dashed line */
border: 3px dotted teal;     /* dotted line */
```

`border-radius` rounds the corners:

```css
.card {
    border: 1px solid #cccccc;
    border-radius: 8px;
}
```

## Margin

Space *outside* the border, pushing other elements away:

```css
.card {
    margin: 20px;
}
```

`margin: 0 auto;` is a handy trick for centering a box horizontally:

```css
.card {
    width: 400px;
    margin: 0 auto;    /* top/bottom 0, left/right automatic → centered */
}
```

## Width and height

```css
.card {
    width: 400px;
    height: 200px;
}
```

> **Watch out:** by default, `width` sets the width of the *content* only.
> Padding and border are added on top. A `width: 400px` element with
> `padding: 20px` and a `border: 2px` is actually **444px** wide in total.
> (The `box-sizing: border-box;` rule changes this so `width` includes padding
> and border — you will often see it in real projects. We mention it here so
> it does not surprise you later, but you can finish this course without it.)

## Common mistakes

- **Confusing padding and margin** — padding is *inside* the border (spaces
  out the content, shows the background), margin is *outside* the border
  (spaces out the boxes).
- **Expecting background to cover the margin** — it does not. The background
  covers content + padding only.
- **Elements sticking together** — if boxes touch with no space, you usually
  need `margin` between them, `padding` inside them, or both.
- **The total-width surprise** — `width` + `padding` + `border` can be wider
  than you expected (see the note above).

## Recap

- Every element is a box: **content → padding → border → margin**.
- `padding` — space inside the border (shows the background).
- `border` — the visible edge (`width style color`).
- `margin` — space outside the border, between elements.
- `width`/`height` set the size of the content box by default.

## What's next?

Now that you can control boxes, [Lesson 06](../06-links-and-lists/README.md)
applies all of this to links and lists — two things every page has.
