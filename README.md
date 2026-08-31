# Larpmaxxing

A dependency-free, single-page fictional money simulator for skits, shorts,
roleplay, moodboards, and rehearsals.

## What it includes

- Six customizable fictional screens: bank, crypto, brokerage, storefront,
  payment, and livestream.
- A permanent on-screen prop disclosure and production-safety checklist.
- Live display name, value, and scene-mood controls.
- User-triggered payout, store, market, and livestream cues.
- Optional live number drift for active-looking scenes.
- Focus mode with a visible exit and permanent fictional disclosure.
- Local setup saving and reset.
- Keyboard-accessible template and creator-workflow tabs.
- Responsive layouts, reduced-motion support, and visible focus states.

## Run locally

No build step or dependencies are required:

```bash
python3 -m http.server 4173
```

Then open `http://localhost:4173`.

## Privacy and scope

The simulator never connects to a bank, broker, exchange, storefront, payment
service, or social platform. It must not be used as evidence of payment, funds,
returns, identity, or expertise. Saved fictional setups remain in browser
`localStorage`.

See [`AUDIT_REPORT.md`](./AUDIT_REPORT.md) for the product, content, UX,
accessibility, trust, and implementation assessment.
