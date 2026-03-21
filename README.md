# Finance Dashboard

A personal finance tracking dashboard — one single HTML file, no backend, no server, no installation. Everything runs in your browser and saves to `localStorage`.

---

## What it does

### Transaction Ledger
- Log **income, expenses, transfers, loans (lend out)** and **repayments**
- Choose your wallet (MoMo, Stanbic, Ecobank, Cash, Other)
- Choose a category from a full list
- Description field with autocomplete from your past entries
- Every entry shows with a colour-coded day stripe so you can tell days apart at a glance
- Sort by date, description, wallet or amount
- Search across all fields
- Expand any row to see full entry details

### Top Metric Cards
Five cards across the top:
- **Pure Income** — total money in for the month
- **Pure Expense** — total money out for the month
- **Surplus / Deficit** — difference between the two
- **Efficiency** — percentage of income you kept
- **Free Benefits** — estimated value of things received for free this month

Tap the first three to reveal or hide (privacy blur).

### Asset Map
- Donut chart showing money split across wallets
- Balance per wallet (negative shown in red)
- Monthly spend per wallet with mini bar chart
- Two net worth figures — **Cash Only** and **Cash + Loans Due**
- Tap the eye icon to reveal or hide

### Spend Velocity Chart
- Last 7 days of daily spending
- Fully dynamic — tallest bar fills the card, rest scale proportionally
- Each day a different colour; zero-spend days in teal
- Hover a bar to see the amount; click to filter ledger to that day

### Top Expenses
- Monthly category breakdown with progress bars
- Biggest single transaction highlighted
- Spend pace projection for month-end

### 6-Month Trend
- Income vs Expense for the last 6 months, clickable to navigate
- Income sources breakdown for the viewed month
- Days since last income

### Gifts Given
- This month vs last month with percentage change
- Top recipients this month

### Monthly Comparison Banner
- Appears when browsing a past month
- Shows spend vs your 3-month rolling average

### 14-Day Cash Flow
- Pure cash movement shown above the ledger
- Second line appears when loans are in the period

### Outstanding Loans
- Tracks money lent per person with repayment progress bar
- Full or partial repayment buttons

### Free Benefits Tracker
- Log things received for free — food, transport, accommodation, other
- Estimate their value; track who gave it
- Top Givers leaderboard, weekly breakdown, searchable and filterable
- Totals for this week, this month, all time

### Recurring Reminders
- Mark transactions as recurring
- Panel shows what has and has not been logged this month

---

## How to use it

### Open locally
1. Download `index.html`
2. Open it in any modern browser (Chrome, Firefox, Safari, Edge)
3. That is it — nothing to install

### Host on GitHub Pages (free)
1. Fork or clone this repository
2. Go to **Settings → Pages**
3. Source: `main` branch, folder `/ (root)`
4. Save — live at `https://yourusername.github.io/repo-name` within a minute

---

## First time setup

The ledger starts empty. Enter your opening wallet balances first:

1. Type → **Inflow (Earnings)**
2. Wallet → whichever wallet
3. Category → **Other**
4. Description → `Opening Balance`
5. Amount → current balance in that wallet
6. **Commit to Audit**

Repeat for each wallet, then log normally from there.

---

## Logging a transaction

| Field | What to do |
|---|---|
| Type | Outflow · Inflow · Transfer · Lend Out · Recv Repay |
| Wallet | Where the money comes from |
| Category | Required — pick from the list |
| Details | Optional (autocomplete from past entries) |
| Amount | The amount |
| Fee | Optional — MoMo charges etc. |
| Date | Defaults to today |
| Destination | Transfer only — pick the receiving wallet |

Click **Commit to Audit** to save.

---

## Backing up your data

1. Click **JSON** top right → downloads a backup file
2. Keep it safe (Google Drive, email to yourself)

To restore:
1. Click **Restore**
2. Paste the JSON content
3. Click **Restore Data**

> ⚠️ Data lives in your browser only. Clear browser data = data gone unless you have a backup. Back up regularly.

---

## Customising

Everything is in one HTML file. To change things:

- **Wallets** — edit the `WALLETS` array in the script
- **Categories** — edit the `CATEGORIES` object
- **Currency** — find `\u20B5` (₵ Ghana Cedi) and replace with your symbol
- **Title** — change `Finance Dashboard` in `<title>` and `<h1>`
- **Wallet colours** — find `WALLET_COLORS` and update hex values

---

## Tech

| | |
|---|---|
| Language | Plain HTML, CSS, JavaScript |
| Styling | Tailwind CSS via CDN |
| Font | Plus Jakarta Sans via Google Fonts |
| Charts | Pure JavaScript |
| Storage | Browser localStorage |
| Backend | None |

**Fully offline after first load. Nothing sent anywhere.**

---

## File structure

```
/
├── index.html    ← the entire app
└── README.md     ← this file
```

---

## License

MIT — use it however you like.
