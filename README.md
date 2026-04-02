# Flavortown Games

A browser-based mini-game hub themed around the iconic cooking world of Flavortown. Play games, earn cookies — all in a single self-contained HTML file.

---

## 🚀 Getting Started

No installation, no server, no dependencies. Just open the file in any modern browser:

```
flavortown-games.html
```

On your first visit, you'll be greeted by the welcome screen. Enter your name and start playing. Your progress is automatically saved in your browser's `localStorage` so your cookie count persists across sessions.

---

## 🎮 Games

| Game | Description | 🍪 Win | 🍪 Lose / Skip |
|---|---|---|---|
| **Tic-Tac-Toe** | Play against a minimax AI. Auto-restarts on loss or draw, stops on win. | +15 | -5 |
| **Rock Paper Scissors** | Classic one-round showdown vs CPU. | +10 | -3 |
| **Number Guess** | Guess a number 1–100 in 10 tries. Hot/cold hints. | +5 to +20 | -3 (give up), -5 (out of tries) |
| **Memory Match** | Flip food emoji cards to find all 8 pairs. | +25 | — |
| **Word Scramble** | Unscramble food-themed words. Streak bonus tracking. | +12 | -2 (wrong), -3 (skip) |
| **Cookie Clicker** | Click the cookie. Every 10 clicks earns 1 🍪. | +1/10 clicks | — |

---

## ✨ Features

- **Persistent user profile** — name and cookie count saved in `localStorage`
- **Returning user detection** — one-click login for returning players
- **Cookie economy** — earn and lose cookies across all games
- **Collapsible sidebar** — expands on hover with game navigation, collapses to icons
- **Auto-restart in Tic-Tac-Toe** — 3-second countdown after loss/draw, stops when you win
- **Fully self-contained** — single `.html` file, no internet connection required after load (Google Fonts optional)

---

## 🗂️ Project Structure

This is a single-file project — everything lives in `flavortown-games.html`:

```
flavortown-games.html
├── <style>         — All CSS (variables, layout, game styles)
├── <body>
│   ├── #welcome-screen     — Login / returning user card
│   ├── .sidebar            — Collapsible navigation with game links
│   ├── .user-card          — Fixed bottom-left user info + cookie count
│   └── .main               — Page container with one div per game
└── <script>        — All game logic + localStorage save/load
```

---

## 🍪 Cookie System

Cookies are the in-game currency. They are:

- **Earned** by winning games or clicking the Cookie Clicker
- **Subtracted** on losses, give-ups, and skips (never goes below 0)
- **Saved automatically** after every change via `localStorage`
- **Restored** when you return with the same name

---

## 🛠️ Tech Stack

| Layer | Choice |
|---|---|
| Language | Vanilla HTML / CSS / JavaScript |
| Fonts | [Fredoka One](https://fonts.google.com/specimen/Fredoka+One) + [Nunito](https://fonts.google.com/specimen/Nunito) via Google Fonts |
| Storage | `localStorage` (browser-native) |
| AI (Tic-Tac-Toe) | Minimax algorithm |
| Assets | Chef logo embedded as base64 PNG |
| Background | Inline SVG pattern (stars, chef hats, rolling pins, forks) |

---

## 🎨 Design

Inspired by the visual style of [Flavortown](https://flavortown.hackclub.com) — a blue tartan sidebar, cream patterned background, dark red user card, and golden cookie accent color.

The chef character in the logo and sidebar is `chepheus.png`, embedded directly into the HTML as a base64 data URI so no external file is needed.

---

## 📁 Files

| File | Description |
|---|---|
| `flavortown-games.html` | The entire project — open this in a browser |
| `README.md` | This file |

---

## 🔧 Customization

Want to tweak things? Everything is in one file:

- **Add a game** — add a nav item in `.sidebar`, a page div in `.main`, and a JS section in `<script>`
- **Change cookie rewards** — find `addCookies(n)` or `subtractCookies(n)` calls in each game's logic
- **Change the color scheme** — edit the CSS variables in `:root`
- **Change the background pattern** — replace the inline SVG in `body { background-image: ... }`

---

*Built with 🍪 .*
