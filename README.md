# Prop Dashboard

A single self-contained `index.html` for making mock financial UI screenshots.
No build step, no dependencies — open the file in a browser.

## Two dashboards (tab-switched)

- **Halcyon** — light retail bank: editable greeting, account cards with masked
  numbers, auto-summed total balance, and a transaction list (credits green `+`,
  debits `−`).
- **Cinder** — dark crypto portfolio: portfolio value with 24h change, a seeded
  SVG area chart, a holdings table with computed values and allocation bars, cash
  balance, and recent activity.

## Behavior

- Every number and label is inline-editable (`contenteditable` spans bound to a
  state object by `data-path`). Commit on blur/Enter, cancel on Escape.
- Derived figures (portfolio value, 24h change, per-holding value, allocation %)
  recalculate automatically and can't be edited directly.
- Add / delete rows for transactions and holdings.
- Chart is a seeded pseudo-random walk — stable across reloads, and the end of
  the line trends with the 24h change.

## Persistence

- Saves to `localStorage` on every commit, loads on boot.
- **Reset** restores defaults (behind a confirm).
- **Export** / **Import** move a setup between machines as a JSON file.

## Present mode

Top-bar toggle, also **Cmd/Ctrl+E**. Hides all editing chrome and the top bar,
and sets `contenteditable` to false — a clean full-bleed screenshot.

## Note

All brand names are invented. No real company names, logos, or trademarks.
