# Larpmaxxing

A dependency-free, single-page responsible prop studio and media-literacy
experience for wealth and status content.

## What it includes

- Four customizable, clearly marked fictional screens: bank, crypto, brokerage,
  and storefront.
- A permanent on-screen prop disclosure and production-safety checklist.
- A clear working definition focused on unsupported claims of ownership,
  expertise, financial success, and elite access.
- Four evidence-signal families: access, money, urgency, and consistency.
- An interactive case lab with three fictional cases and a URL-guided review.
- A keyboard-accessible verification playbook.
- Language and ethics guidance that keeps analysis focused on claims, not people.
- Responsive layouts, reduced-motion support, visible focus states, and local-only
  case-note persistence.

## Run locally

No build step or dependencies are required:

```bash
python3 -m http.server 4173
```

Then open `http://localhost:4173`.

## Privacy and scope

The prop studio never connects to a bank, broker, exchange, or storefront, and
must not be used as evidence of payment, funds, returns, or expertise. The case
lab does not fetch pasted URLs, scrape social platforms, identify people, or
issue factual verdicts. Saved demo cases remain in browser `localStorage`.

See [`AUDIT_REPORT.md`](./AUDIT_REPORT.md) for the product, content, UX,
accessibility, trust, and implementation assessment.
