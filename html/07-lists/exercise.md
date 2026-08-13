# Exercise — Favorite Foods and Ingredients

## 🎯 Goal

Practice `ul`, `ol`, `li`, and nested lists by building a page about food.

## 📚 What You Learned

- Unordered lists `<ul>`
- Ordered lists `<ol>`
- List items `<li>`
- Nested lists

## 📝 Task

1. Create a new file called `food.html` with a complete HTML document.
2. Add a section **My favorite foods** that uses an unordered list (`<ul>`)
   with at least four foods.
3. Add a section **How I make fruit salad** that uses an ordered list (`<ol>`)
   with at least four steps.
4. Add a section **Ingredients by category** that uses a **nested list**: a
   `<ul>` with at least two categories (for example *Fruits* and *Vegetables*),
   each containing its own inner `<ul>` with at least three items.

## Requirements

- [ ] The page is a complete, valid HTML document
- [ ] It uses an `<ul>` with at least four `<li>` items
- [ ] It uses an `<ol>` with at least four `<li>` items
- [ ] It uses a nested list (a list inside a list item)
- [ ] Every `<ul>` and `<ol>` has exactly `<li>` elements inside it
- [ ] All tags are properly closed

## 💡 Hint

For the nested list, follow the example's pattern exactly:

```html
<ul>
    <li>Fruits
        <ul>
            <li>Apples</li>
        </ul>
    </li>
</ul>
```

The inner `<ul>` must be inside an `<li>` of the outer list.

## ⭐ Challenge

Change the numbering of your ordered list to start at 5 (hint: there is an
attribute called `start` on `<ol>`), and add a link inside one of your list
items that points to a recipe website.

## ✅ Solution

Open `solution.html` **after** you have attempted the exercise and compare your
work. Your food choices can be completely different — the structure is what
matters.
