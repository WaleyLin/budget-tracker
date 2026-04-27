# Budget Tracker

A clean, Discord-inspired personal budget tracker — built with vanilla HTML, CSS & JS. No backend, no accounts, no BS.

![HTML](https://img.shields.io/badge/HTML-5-E34F26?style=flat&logo=html5&logoColor=white)
![CSS](https://img.shields.io/badge/CSS-3-1572B6?style=flat&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-ES6-F7DF1E?style=flat&logo=javascript&logoColor=black)

---

## How It Works

1. Enter your **hourly rate + hours/week** or annual salary in the Income section
2. The app calculates your gross and net pay across all pay periods, deducting federal tax, state tax, FICA, and any custom deductions
3. Add your gas info — price per gallon, gallons per fill-up, and fill-ups per month — and it auto-calculates your monthly fuel cost
4. Add any expense with a name, amount, and frequency (weekly through yearly) — everything is auto-converted to monthly
5. Hit the **Split with GF** button on gas or any individual expense to divide the cost in half
6. Watch the **Summary** section update in real time — income, expenses, leftover, and an expense ratio bar

---

## Features

- **Hourly or salary mode** — switch pay types with one click
- **Gas tracker** — calculates monthly fuel cost with a one-click split
- **Unlimited expenses** — 5 frequency types (weekly, bi-weekly, monthly, every 6 months, yearly), all normalized to monthly
- **Per-expense split toggle** — share any bill in half with your girlfriend, with the math shown
- **Summary dashboard** — 4 stat cards, expense ratio progress bar (green/yellow/red), income breakdown table, expense breakdown table, and leftover breakdown
- **Auto-save** — everything persists to `localStorage`; comes back exactly where you left off on reload
- **Zero dependencies** — single HTML file, no npm, no build step, no server

---

## What Changed vs Basic Budgeting Spreadsheets

| Problem | Before | After |
|---|---|---|
| Pay period math | Manual calculation per period | Auto-calculates weekly, bi-weekly, semi-monthly, monthly |
| Tax deductions | Single flat rate | Federal %, state %, FICA (7.65%), and custom deductions |
| Expense frequency | Everything had to be monthly | 5 frequency types — all auto-converted to monthly |
| Shared expenses | Manual halving | Per-item split toggle with inline math shown |
| Fuel cost | Separate tracking | Built-in gas calculator with split support |
| Persistence | Re-enter every session | Auto-saves to localStorage |

---

## Setup

1. Download `index.html`
2. Double-click to open in any browser — that's it, no server needed
3. Fill in your income in section **01**
4. Add your gas info in section **02**
5. Add your bills in section **03**
6. View totals in the **Summary** section at the bottom

> **Note:** All data stays 100% on your device — nothing is sent anywhere. Works completely offline.

---

## Project Structure

```
budget-tracker/
└── index.html   ← everything is here (HTML + CSS + JS, single file)
```

---

## Tech Stack

| Technology | Usage |
|---|---|
| HTML / CSS | Layout and Discord-inspired dark theme |
| Vanilla JS | All calculations, state management, and DOM updates |
| localStorage | Automatic persistence across sessions |

---

## Customization

Open `index.html` in any editor and look for these easy tweaks:

**Default expenses** — find `DEFAULT_EXPENSES` near the top of the `<script>` tag:
```js
const DEFAULT_EXPENSES = [
  { name: 'Rent / Mortgage', amount: '', freq: 'monthly', split: false },
  // add your own here
];
```

**State tax label** — find this line in the HTML and update the hint:
```html
State Tax % <span>(AZ ~2.5%)</span>
```

**Accent color** — find `:root` in the CSS:
```css
--accent: #5865f2;  /* change this hex */
```

---

## Known Limitations

- **No multi-device sync** — localStorage is browser and device-specific
- **No income history** — tracks current setup only, not changes over time
- **Split is always 50/50** — no custom split ratios

---

## To Reset

Open browser DevTools → Application → Local Storage → clear the `budgetData` key.
