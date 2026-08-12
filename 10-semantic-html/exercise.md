# Exercise — From Divs to Semantics

## 🎯 Goal

Restructure a page that uses only generic `<div>` containers into a page that
uses semantic elements.

## 📚 What You Learned

- `<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<aside>`,
  `<footer>`
- Why semantic HTML is useful

## 📝 Task

1. Create a new file called `semantic-page.html`.
2. Copy the messy page below **exactly as it is** (it works — it is just not
   semantic).
3. Rewrite it so that every generic `<div>` is replaced by the semantic element
   that best matches its content. The page has: a header with a nav, two
   articles inside a main section, an aside, and a footer.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Recipe blog</title>
</head>
<body>
    <div>
        <h1>Recipe blog</h1>
        <div>
            <a href="#pancakes">Pancakes</a> |
            <a href="#soup">Soup</a>
        </div>
    </div>

    <div>
        <div>
            <h2 id="pancakes">Pancakes</h2>
            <p>Fluffy pancakes with maple syrup — a weekend favorite.</p>
        </div>
        <div>
            <h2 id="soup">Tomato soup</h2>
            <p>Simple tomato soup made with fresh basil and cream.</p>
        </div>
    </div>

    <div>
        <h2>About the cook</h2>
        <p>I have been cooking for ten years and love simple recipes.</p>
    </div>

    <div>
        <p>© 2026 Recipe blog</p>
    </div>
</body>
</html>
```

## Requirements

- [ ] The page still contains the same text and links as the original
- [ ] `<header>` wraps the page title and the navigation
- [ ] `<nav>` wraps the two links
- [ ] `<main>` wraps the two recipes
- [ ] Each recipe is wrapped in its own `<article>`
- [ ] `<aside>` wraps the "About the cook" block
- [ ] `<footer>` wraps the copyright line
- [ ] The page contains no `<div>` elements at all

## 💡 Hint

Work top to bottom. Start with the outer structure (header, main, aside,
footer), then go inside `<main>` and wrap each recipe in an `<article>`.

## ⭐ Challenge

Inside each `<article>`, add a short `<header>` containing a small paragraph
like "Posted on March 12, 2026" — the article header is separate from the page
header. Also wrap the two recipes in a `<section>` inside `<main>`.

## ✅ Solution

Open `solution.html` **after** you have attempted the exercise and compare your
work. As long as every region uses the matching semantic element, your answer
is correct.
