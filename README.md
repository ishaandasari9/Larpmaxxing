# Larpmaxxing

A dependency-free, single-page media-literacy experience for understanding and
investigating wealth and status LARPing on social media.

## What it includes

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

The case lab is an educational prototype. It does not fetch pasted URLs, scrape
social platforms, identify people, or issue factual verdicts. Saved demo cases
remain in browser `localStorage`.

See [`AUDIT_REPORT.md`](./AUDIT_REPORT.md) for the product, content, UX,
accessibility, trust, and implementation assessment.
