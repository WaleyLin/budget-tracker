# 💸 Budget Tracker

> A clean, Discord-inspired personal budget tracker — built with vanilla HTML, CSS & JS. No backend, no accounts, no BS.

![Budget Tracker Preview](https://img.shields.io/badge/status-ready%20to%20use-57f287?style=for-the-badge)
![No Dependencies](https://img.shields.io/badge/dependencies-zero-5865f2?style=for-the-badge)
![Saves Locally](https://img.shields.io/badge/storage-localStorage-fee75c?style=for-the-badge)

---

## ✨ Features

### 💰 Income Calculator
- **Hourly or Salary** — switch between pay types with one click
- Enter your **hourly rate + hours per week**, or just your annual salary
- Calculates gross pay across weekly, bi-weekly, semi-monthly, and monthly periods
- Deducts:
  - Federal income tax %
  - State tax % (defaults shown for Arizona ~2.5%)
  - FICA / Social Security (7.65%)
  - Other deductions (401k, health insurance, etc.) per paycheck

### ⛽ Gas Tracker
- Enter **price per gallon**, **gallons per fill-up**, and **fill-ups per month**
- Auto-calculates your monthly gas cost
- **💑 Split with GF button** — one click divides the cost in half and shows the math

### 📋 Expense Tracker
- Add unlimited expenses with custom names
- Each expense supports **5 frequency types**:
  - Weekly
  - Bi-weekly
  - Monthly
  - Every 6 months
  - Yearly
- All expenses are automatically **converted to monthly** for calculations
- **💑 Split toggle on every expense** — splits any bill in half with your girlfriend
- Delete any expense with the `×` button

### 📊 Summary Dashboard
- **4 stat cards** — Monthly income, Monthly expenses, Monthly leftover, Annual leftover
- **Expense ratio progress bar** — visual indicator of how much of your income goes to bills
  - Green → under 50% (healthy)
  - Yellow → 50–75% (watch it)
  - Red → 75%+ (tight)
- **Income Breakdown Table** — gross vs net across every pay period
- **Expense Breakdown Table** — every bill listed with split indicator and monthly equivalent
- **Leftover Breakdown** — weekly / monthly / 6-month / annual money left after all expenses

### 💾 Auto-Save
- Everything saves automatically to your browser's `localStorage` — no account needed
- Comes back exactly where you left off on reload

---

## 🚀 How to Use

1. **Download** `index.html`
2. **Double-click** to open in your browser — that's it, no server needed
3. Fill in your income details in section **01**
4. Add your gas info in section **02** and hit the split button if needed
5. Add your bills in section **03** — set the frequency and split any shared ones
6. Watch the **Summary** section at the bottom update in real time

---

## 📁 File Structure

```
budget-tracker/
└── index.html   ← everything is in here (HTML + CSS + JS)
```

Single file. No build step. No npm install. Just open it.

---

## 🎨 Design

- **Dark theme** inspired by Discord's UI
- Color palette:
  - `#5865f2` — Discord blurple (accent)
  - `#57f287` — green (income / positive)
  - `#ed4245` — red (expenses / negative)
  - `#fee75c` — yellow (warnings / gas)
  - `#eb459e` — pink (split with GF indicator)
- Fonts: **DM Sans** + **JetBrains Mono**
- Fully responsive — works on mobile too

---

## 🛠 Customization

Open `index.html` in VSCode and look for these easy tweaks:

**Change default expenses** — find `DEFAULT_EXPENSES` array near the top of the `<script>` tag:
```js
const DEFAULT_EXPENSES = [
  { name: 'Rent / Mortgage', amount: '', freq: 'monthly', split: false },
  // add your own here
];
```

**Change location for tax hint** — find the label text:
```html
State Tax % <span>(AZ ~2.5%)</span>
```

**Change accent color** — find `:root` in the CSS and change `--accent`:
```css
--accent: #5865f2;  /* change this hex */
```

---

## 📝 Notes

- All data stays **100% on your device** — nothing is sent anywhere
- Works completely **offline**
- To reset everything: open browser DevTools → Application → Local Storage → clear `budgetData`

---

*Built with ❤️ — no frameworks, no build tools, just a single HTML file.*
