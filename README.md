# முஹம்மது ஸஃபான் முபா — Personal Academic Website (Tamil edition)

A free-to-run, Tamil-language personal website for publishing writings,
research and lecture notes, aimed at Tamil students and readers. It's plain
HTML/CSS/JS — no server, database or paid software needed.

- All page content is in Tamil (`lang="ta"` on every page).
- Fonts: **Noto Serif Tamil** (headings) + **Catamaran** (body/labels) —
  both free Google Fonts with full Tamil script support, loaded via a
  `<link>` tag in each page's `<head>`.
- Everything else (folder structure, how to add/edit/delete articles, free
  hosting steps) works exactly the same as described below.

## 1. Put your real details in

Before publishing, search the files for these placeholders and replace them:

- `youremail@example.com` and the social links in `contact.html`
- `YOUR_FORM_ID` in `contact.html` (see step 4)
- The sample writings, research entries and lecture notes on `index.html`,
  `writings.html`, `research.html`, `lectures.html`, `about.html`
- The date/author line in `writings/article-template.html`

## 2. Add a new article

1. Duplicate `writings/article-template.html`, rename it (e.g.
   `writings/reading-papers-critically.html`).
2. Edit the title, label, meta line and body text inside it.
3. Add a matching card to `writings.html` (and optionally `index.html`)
   linking to the new file — copy an existing `<a class="card">` block and
   edit it.

No build tools, no CMS login — just HTML you edit directly.

## 3. Publish it for free

You don't need to buy hosting. Two good free options:

**GitHub Pages (recommended, fully free forever)**
1. Create a free GitHub account at github.com.
2. Create a new repository, e.g. `muba-site`.
3. Upload all the files in this folder to that repository (drag-and-drop
   works on github.com, or use `git push` if you're comfortable with Git).
4. In the repository, go to **Settings → Pages**, set the source to the
   `main` branch, and save.
5. Your site will be live at `https://yourusername.github.io/muba-site/`
   within a few minutes.

**Netlify (also free, slightly more polished dashboard)**
1. Create a free account at netlify.com.
2. Drag this folder onto the Netlify "Deploy" page, or connect it to a
   GitHub repo as above.
3. You'll get a free address like `https://muba-site.netlify.app`.

Both options renew for free indefinitely on their free tier — no credit
card required.

## 4. Make the contact form actually send email

The form in `contact.html` posts to Formspree, a free service built for
exactly this (static sites with no backend):

1. Go to formspree.io and create a free account (50 submissions/month free).
2. Create a new form and copy the form ID it gives you.
3. In `contact.html`, replace `YOUR_FORM_ID` in the `<form action="...">`
   line with that ID.

Alternatively, delete the form and just keep the `mailto:` email link if you
prefer people to email you directly.

## 5. Writing new articles in Tamil

Just type Tamil directly into the `.html` file in any text editor that
supports Unicode (VS Code, Notepad, TextEdit all work fine) — no special
setup needed. Save the file as UTF-8 (the default in virtually every modern
editor) and the Tamil script will display correctly in the browser.

## 6. About a domain name (onlinemuba.com)

A custom domain is optional — the free GitHub Pages / Netlify address works
fine to start, and you can add a domain later without rebuilding anything.
When you're ready:

- Domain registration typically costs roughly **$10–15/year** (not a
  recurring web-hosting fee — hosting itself stays free via GitHub Pages or
  Netlify). Registrars like Namecheap or Porkbun tend to be cheaper than
  average.
- Some registries (e.g. `.com.np`, or student/education-linked offers) run
  occasional free-domain promotions — worth checking, but not guaranteed.
- Once you own a domain, both GitHub Pages and Netlify let you connect it
  for free — you only pay the registrar's yearly renewal.

## File structure

```
index.html              Home page
about.html               About page
writings.html            Article index
writings/
  article-template.html  Duplicate this for each new article
research.html             Research projects
lectures.html             Lecture notes / talks
contact.html               Contact form + direct details
css/style.css              All styling
js/main.js                 Mobile menu + footer year
assets/leaf-veins.svg       Decorative hero graphic
```

## Editing without coding experience

Every page is plain HTML — open any `.html` file in a text editor (even
Notepad or TextEdit), find the sentence you want to change between `<p>`
and `</p>` tags (or similar), and edit the words directly. As long as you
leave the `<...>` tags alone, you can't easily break the layout.
