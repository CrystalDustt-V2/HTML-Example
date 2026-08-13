# Exercise — A Simple Navigation

## 🎯 Goal

Build a page with a working navigation bar that uses absolute links, relative
links, and a link that opens in a new tab.

## 📚 What You Learned

- `<a href="...">` and link text
- Absolute URLs for external websites
- Relative URLs for your own pages
- `target="_blank"` for new tabs

## 📝 Task

1. Create a new file called `navigation.html` in the `05-links` folder.
2. Add a heading and a small navigation with **four** links:
   - "Home" → `navigation.html` (a relative link)
   - "About" → `about.html` (a relative link to the page in this folder)
   - "Contact" → `contact.html` (a relative link to the page in this folder)
   - "Wikipedia" → `https://www.wikipedia.org` with `target="_blank"`
3. Below the navigation, add a paragraph that contains one more link of your
   choice — for example a link to your favorite website.
4. Open `navigation.html` in your browser and click **every** link to check
   that it goes where you expect.

## Requirements

- [ ] The page is a complete, valid HTML document
- [ ] It contains at least four `<a>` elements
- [ ] At least one link uses a relative URL (`about.html` or `contact.html`)
- [ ] At least one link uses an absolute URL (`https://...`)
- [ ] Exactly the external link has `target="_blank"`
- [ ] Every link has descriptive text (not "click here")

## 💡 Hint

`navigation.html` lives in the same folder as `about.html` and `contact.html`,
so a plain relative link like `href="about.html"` is all you need. If a link
does not work, double-check the file name spelling and the quotes.

## ⭐ Challenge

Create a third page of your own — for example `hobbies.html` — and add it to
the navigation. Then link from your new page back to `navigation.html`. You now
have a tiny multi-page website!

## ✅ Solution

Open `solution.html` **after** you have attempted the exercise and compare your
work. Any navigation with four working links is a correct answer.
