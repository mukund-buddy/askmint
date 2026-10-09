# 💬 AskMint

![vanilla JS](https://img.shields.io/badge/vanilla-JS-f7df1e?logo=javascript&logoColor=black)
![zero backend](https://img.shields.io/badge/zero-backend-3dff9e)
![license](https://img.shields.io/badge/license-MIT-4dd0e1)

**An embeddable "ask me anything" question box for static websites — form se leke browser local save tak, zero backend.**

> Part of [The Antigle](https://github.com/mukund-buddy) 🔥 — AI-assisted build, hand-tested.
> Inspired by Adventigle's "Have a question? I'll reply by email" flow — genericized so any creator can use it.

**Live demo:** _coming soon_ · [Repository](https://github.com/mukund-buddy/askmint)

---

## 🎯 Why This Exists

Static site creators (Gamers, Minecraft YouTubers, digital sellers) get constant
questions, but:

- Forms need backends
- Discord links kick people out of the site
- Email links are ugly and get forgotten

Adventigle solves this with an in-page question box that opens the visitor's
email client with the question pre-filled — works forever, no server.
**AskMint is that flow as a ready-made embeddable widget.**

## ✨ Features

- **In-page question box** — no redirects, no popups
- **Local drafts** — typing survives accidental refresh (localStorage)
- **Optional categories** — "Video idea", "Pack help", "Business", "Other"
- **Email-based or link-based delivery** — configure in one small config file; no data leaves the browser until the visitor submits
- **Character counter + gentle validation** — no empty questions
- **Theme-able** — 2 CSS variables to match your brand
- **Works anywhere static** — GitHub Pages, Cloudflare Pages, itch.io pages, anywhere HTML runs

## 🚀 How It Works

```
index.html   →  embed-ready widget demo
widget.js    →  …this one file. Drop it into any page + one <div>
config.js    →  your settings: recipient email, categories, greeting text
style.css    →  the look (brand colors top of file)
```

### Setup for your own site

```js
window.ASKMINT_CONFIG = {
  recipient: "you@yourmail.com",
  greeting: "Ask me anything about Minecraft packs!",
  categories: ["Pack help", "Video idea", "Business"],
  mode: "email"
};
```

Load `config.js` before `widget.js`, add one line of HTML, done.
(Prefer JSON? `<div id="askmint" data-config="config.json">` still works —
the widget fetches it when that attribute is present.)

## 🗺️ Roadmap

- [x] Email-mode question box (v1)
- [x] Draft saving + validation
- [ ] Discord webhook mode (optional)
- [ ] Char count themes + full customization
- [ ] Per-question reply status (self-hosted Firebase option)

## 🧑‍💻 Honest Note

AI-assisted, human-tested. This runs on a real product (Adventigle) before
shipping as a standalone repo — field-tested, not just generated.

## 🏷️ Suggested GitHub Topics

`embeddable` `contact-form` `static-site` `widget` `vanilla-js` `client-side` `github-pages` `the-antigle`

## 📄 License

MIT
