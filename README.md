# dropdate

A personal second-hand selling tracker built for managing Vinted listings. Tracks prices, schedules drops, logs relists, and keeps everything in one place.

**Live app:** [hanakysela.github.io/dropdate/dropdate.html](https://hanakysela.github.io/dropdate/dropdate.html)

---

## What it does

- **Listing cards** — name, price, status, days listed, views/likes, platform badges
- **Price drop scheduler** — set drop dates and prices weeks in advance, get overdue alerts
- **Action banner** — shows what needs attention today: drops due, relist recommendations, top listing improvements
- **Relist tracking** — logs relist history with original price and date
- **Stats analysis** — enter views and likes, get AI diagnosis (requires Anthropic API)
- **Platform tracking** — tracks which platforms each item is listed on (Vinted, eBay, etc.)
- **Backup** — export JSON to clipboard, import by paste

## Vinted-specific rules built in

- Bumping is **not free** on Vinted CZ — never suggested
- Relisting (delete + re-create) is **free** and resets algorithm visibility — always preferred
- Topping costs ~100 Kč — only suggested for items priced above 800 Kč

## Data storage

Data lives in your browser's `localStorage`. It persists across restarts, tab closes and browser updates. It will be lost if you clear Chrome site data for the domain.

**Back up regularly:** use the ⋯ menu → Copy to clipboard → paste into Notes or email to yourself.

## AI features

The app calls the Anthropic API for:
- Generating selling strategy when adding a listing (drop dates, platform recommendations, listing tips)
- Analysing stats (views/likes) and recommending action
- Inferring item details from a Vinted URL slug

These features require a valid Anthropic API key served via a backend proxy (due to browser CORS restrictions). Without one, all manual features still work — you can add listings, track drops, log relists, and manage backups without AI.

## Tech

- Single HTML file, no build step, no dependencies
- Vanilla JS, plain CSS
- localStorage for persistence
- Hosted on GitHub Pages

## Status

Personal tool, actively used. Not a polished product — built iteratively for real selling use.
