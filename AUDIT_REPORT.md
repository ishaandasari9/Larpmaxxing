# Larpmaxxing product and UX report

Audit date: 31 August 2026

## Executive summary

Larpmaxxing is a creative money-screen simulator for skits, shorts, roleplay,
moodboards, and rehearsals. Its mission is entertainment, not financial
verification or social-media policing.

The original prototype proved the core interaction: editable bank and crypto
screens that worked without accounts or dependencies. Its limitations were
product breadth, creator workflow, mobile ergonomics, and the absence of a
visible in-product statement that the screens were fictional.

The revised product now makes the creator mission explicit and adds:

- six fictional screen worlds: bank, crypto, brokerage, storefront, payment,
  and livestream;
- a visual dashboard picker with instant previews;
- live name, value, and scene-mood controls;
- local setup saving and reset;
- a full-screen focus mode for filming;
- four fire-on-cue fictional alerts;
- optional live number drift;
- production notes and a clear local-only privacy model;
- creator-focused onboarding, feature explanations, and FAQ; and
- a persistent “Fictional prop · not real money” label.

The result is substantially closer to the low-friction creator mission of
[Larped](https://larped.app/app/) while retaining an original editorial visual
identity and stronger disclosure at the moment of use.

## Product-direction decision

The earlier report treated Larpmaxxing partly as a media-literacy or detection
tool. The product clarification supersedes that direction. The primary user is
a creator who needs a fictional screen quickly, not an investigator evaluating
someone else’s post.

This changes the product priorities:

| Previous emphasis | Current emphasis |
| --- | --- |
| Analyze external posts | Create fictional scenes |
| Evidence-risk scoring | Live production cues |
| Verification playbook | Four-step creator workflow |
| Detection glossary | Product and privacy FAQ |
| Case saving | Local scene saving |
| Researcher/moderator audience | Creator/filmmaker audience |

Safety remains part of product quality, but it is framed as a simple creator
boundary instead of the main experience.

## Reference benchmark: larped.app

The supplied reference succeeds because it is easy to understand:

1. choose a dashboard;
2. edit the screen;
3. film the scene.

The public site also communicates that the product is fictional, local, and not
connected to financial institutions.

Larpmaxxing adapts the useful interaction pattern without copying brand names,
layouts, or copy.

| Area | Reference strength | Larpmaxxing improvement |
| --- | --- | --- |
| Entry point | Simple dashboard launcher | Six visual templates plus a live workspace |
| Account friction | Free previews without an account | Entire prototype works without an account |
| Variety | Multiple financial and creator surfaces | Bank, crypto, brokerage, store, pay, and live worlds |
| Filming | Clean recording-oriented screens | Focus mode plus keyboard Escape exit |
| Movement | Live-looking values and alerts | User-controlled number drift and cue deck |
| Privacy | Device-local framing | No requests, integrations, trackers, or financial connections |
| Continuity | Editable scenes | Local setup saving across sessions |
| Disclosure | Public disclaimers | Persistent disclosure inside every generated scene |

## How the app relates to the supplied wealth-LARPing definition

The supplied definition concerns pretending to have wealth, access, or expertise
that a person does not have. A fictional prop simulator can resemble one tactic
in that taxonomy, but resemblance does not determine intent or use. Film props,
games, parody, rehearsals, and consensual pranks are legitimate creative uses.

The website now makes the distinction explicit:

- the product is called a fictional simulator;
- all companies and activity are invented;
- the application never connects to real money;
- a prop label remains visible in all six templates and focus mode;
- production notes state the intended use; and
- copy says the screens are not evidence of funds, payment, returns, identity,
  or expertise.

The standard is therefore fulfilled as an intended-use and disclosure boundary,
not as a requirement to turn the product into a detector.

## Current experience audit

### 1. Hero and navigation

The hero now leads with “Your story. Your numbers.” and immediately explains the
creative use cases. The primary action opens the studio; the secondary action
jumps to the six-screen picker.

Navigation follows creator tasks:

- Dashboards;
- Live cues;
- Features; and
- How it works.

The sticky header, skip link, mobile menu, and in-page anchors reduce navigation
friction. Escape closes the mobile menu and restores focus.

### 2. Dashboard picker

Six compact visual previews communicate variety before the user commits:

| Screen | Intended scene |
| --- | --- |
| Halcyon Bank | Everyday balance or savings story |
| Cinder Wallet | Crypto or market scene |
| Ridgeline Trade | Position or trading scene |
| Vaultly Store | Launch-day or creator-business scene |
| Northstar Pay | Social payment or group-chat scene |
| Luma Live | Livestream and audience scene |

The picker follows the ARIA tabs keyboard pattern:

- Left/Right moves between templates;
- Home/End jumps to the first or last template; and
- only the selected template remains in the tab order.

### 3. Scene customization

The creator can set:

- a fictional display name;
- a bounded hero value from 0 to 9,999,999; and
- one of three scene moods.

Input is escaped before rendering. Numbers are formatted by screen type:
currency for financial screens and viewer count for the livestream.

The workspace provides clear controls rather than relying on hidden
`contenteditable` regions. This improves discoverability, validation, keyboard
use, and mobile input behavior.

### 4. Save and reset

“Save setup” stores only four non-sensitive values in `localStorage`:

- selected template;
- display name;
- hero value; and
- mood.

“Reset” stops live drift, restores defaults, and selects the first template.
Both actions return visible status feedback.

### 5. Focus mode

Focus mode:

- centers the fictional device;
- removes the setup chrome from the shot;
- keeps the prop label inside the device;
- provides a visible Exit control; and
- exits with Escape.

This resolves the original Present-mode trap, where the control to exit was
hidden and the keyboard shortcut was undiscoverable.

### 6. Cue deck and live drift

The cue deck adds performance timing rather than more configuration:

- project payout;
- new store order;
- market goal;
- live viewer milestone.

Each cue updates the rehearsal card, scrolls to the device, appears inside the
marked preview, and clears automatically.

Live drift moves the main value gently every 1.1 seconds. The user can pause it
at any time. It does not update unrelated data or contact a market-data source.

### 7. Creator onboarding and FAQ

The four-step workflow teaches:

1. pick a world;
2. customize the scene;
3. rehearse cues; and
4. enter focus mode and record.

The FAQ answers the highest-trust questions directly: financial connections,
local saving, focus mode, and prohibited use.

## Visual design assessment

### Strengths

- distinctive warm-paper, dark-green, coral, and lime palette;
- editorial serif headlines with legible system sans-serif body text;
- recognizable but invented screen worlds;
- restrained borders and shadows;
- a clear visual boundary between website chrome and the device prop;
- responsive hierarchy rather than a desktop layout merely scaled down; and
- no reliance on stock imagery or third-party assets.

### Improvements over the baseline

- unified Larpmaxxing identity replaces two unrelated dashboard brands;
- preview cards make variety visible;
- primary controls are grouped beside the resulting screen;
- action feedback uses non-blocking live-region toasts;
- focus mode is purpose-built for filming; and
- the permanent in-scene disclosure is visually integrated.

### Remaining visual opportunities

1. Add optional device frames for phone, tablet, and desktop.
2. Add creator-selectable accent themes while keeping contrast compliant.
3. Add a compact horizontal picker on narrow phones to reduce page length.
4. Add subtle entrance motion only when reduced motion is not requested.
5. Add print and presentation styles for production planning.

## Accessibility assessment

Implemented:

- semantic page landmarks;
- skip link;
- visible focus states;
- labelled native controls;
- 44-pixel-or-larger primary targets;
- reduced-motion support;
- ARIA tab state and keyboard navigation;
- ARIA pressed state for live drift;
- status announcements for save, reset, cues, and clipboard actions;
- Escape behavior for the mobile menu and focus mode; and
- layouts for desktop, tablet, and mobile.

Still requiring formal validation:

- NVDA, JAWS, VoiceOver, and TalkBack behavior;
- Windows forced-colors mode;
- 200% and 400% zoom;
- text-spacing overrides;
- computed color contrast in all six screen themes; and
- focus visibility against every preview background.

Recommended accessibility improvements:

1. Add `aria-labelledby` updates between each template tab and the shared panel.
2. Announce live drift value changes at a low frequency or provide an optional
   text status without creating excessive screen-reader output.
3. Move focus to the cue notification only when the user opts into that behavior.
4. Add automated accessibility checks in CI.

## Privacy and security

Current data exposure is low:

- no account;
- no backend;
- no analytics;
- no trackers;
- no bank, broker, wallet, or store integration;
- no URL submission;
- no user-content upload; and
- only a small fictional setup object in local browser storage.

Technical considerations:

- user-provided display names are escaped before insertion;
- values are numerically bounded;
- generated screen HTML still uses `innerHTML`, so future user-generated fields
  must follow the same escaping rule or use DOM text nodes;
- `localStorage` is suitable for fictional setup values, not sensitive content;
- a production deployment should add a strict Content Security Policy; and
- automated regression tests should cover save/restore, cue cleanup, drift
  start/stop, and focus exit.

## Performance and maintainability

The single-file architecture remains fast and simple:

- no dependencies;
- no build step;
- no runtime network requests;
- immediate static hosting; and
- minimal operational risk.

The file is now large enough that the next material feature should trigger
modularization:

```text
index.html
styles/
  tokens.css
  marketing.css
  studio.css
src/
  templates.js
  studio.js
  cues.js
  persistence.js
tests/
  studio.test.js
  accessibility.test.js
```

A framework is not required yet. Modular JavaScript and CSS would provide most
of the maintenance benefit without adding a heavy build chain.

## Prioritized roadmap

### Priority 0: validate the current simulator

1. Browser-test all six templates.
2. Verify cue timing, drift pause, reset, save/restore, and Escape exits.
3. Run keyboard and screen-reader checks.
4. Test the prop label under focus mode and common recording crops.

### Priority 1: creator value

1. Add phone, tablet, and desktop frame options.
2. Add named local presets for recurring characters.
3. Add fictional transaction/comment editors with sensible limits.
4. Add a scene timer and countdown cue.
5. Add a privacy-preserving screenshot export that always includes disclosure.

### Priority 2: production polish

1. Add theme accents and accessibility-safe palettes.
2. Add a cue sequence for multi-beat scenes.
3. Add optional sound cues with explicit mute controls.
4. Add offline installability through a small web-app manifest and service
   worker.

### Priority 3: engineering maturity

1. Split the single file into modules.
2. Add unit, browser, and accessibility tests.
3. Add deployment headers and Content Security Policy.
4. Add schema versioning for locally saved scenes.

## Success measures

Useful product measures are:

- time from landing to first customized scene;
- percentage of users who successfully switch templates;
- cue and focus-mode completion rate;
- save/restore success rate;
- mobile task completion;
- accessibility task completion; and
- percentage of recorded/exported output retaining the prop disclosure.

Avoid measuring success through the realism of deception. Measure how quickly a
creator can tell a clearly fictional story.

## Final verdict

Larpmaxxing now has a coherent creator mission and a stronger experience than
the original two-screen dashboard. It combines the reference product’s
low-friction dashboard selection with broader scene variety, live performance
controls, local continuity, accessible navigation, and visible fictional
context.

The strongest next improvement is not more marketing copy. It is production
validation of the six screens, live cue timing, focus mode, save/restore, and
mobile filming ergonomics.
