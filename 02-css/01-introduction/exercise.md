# Exercise — Your First CSS Rules

## 🎯 Goal

Write your first CSS: add a `<style>` block to a page and create several rules
that change how it looks.

## 📚 What You Learned

- What CSS is and what it does
- The parts of a rule: selector, property, value
- Where CSS goes (embedded `<style>` for now)
- CSS comments

## 📝 Task

1. Create a new file called `my-style.html` in the `01-introduction` folder.
2. Start from `example.html` (copy it, or write your own).
3. Write at least **three CSS rules**:
   - One that styles the `<h1>` (change its color and font-size)
   - One that styles paragraphs (change their color)
   - One that styles another element of your choice (for example `em` or `strong`)
4. Add at least **one CSS comment** explaining what a rule does.
5. Save and open the page in your browser.

## Requirements

- [ ] The page has a `<style>` element inside the `<head>`
- [ ] At least three rules, each with a selector, a property, and a value
- [ ] Every declaration ends with a semicolon (`;`)
- [ ] Every rule ends with a closing brace (`}`)
- [ ] At least one CSS comment (`/* ... */`)
- [ ] The page still shows all of its text (CSS should change *looks*, not
      remove content)

## 💡 Hint

A rule looks like this — fill in your own colors and sizes:

```css
h1 {
    color: teal;
    font-size: 40px;
}
```

If nothing changes when you refresh, check your selector name and your
spelling (`color`, not `colour`).

## ⭐ Challenge

Add a rule that styles the whole page at once using the `body` selector — for
example, change the background color of the entire page:

```css
body {
    background-color: #f0f0f0;
}
```

We will study colors properly in
[Lesson 02](../02-colors-and-backgrounds/README.md), but feel free to peek
ahead and experiment.

## ✅ Solution

Open `solution.html` **after** you have attempted the exercise and compare
your work. Your colors and sizes do not need to match — the point is that your
rules work.
