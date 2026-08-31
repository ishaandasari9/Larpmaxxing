# Larpmaxxing product and standards audit

Audit date: 31 August 2026
Scope: product purpose, wealth/status LARPing taxonomy, information quality,
user experience, accessibility, privacy, safety, and technical implementation.

## Executive assessment

The original application did not explain wealth or status LARPing. It was an
editable mock bank-and-crypto dashboard designed to create convincing financial
screenshots. That directly enabled two tactics named in the supplied standard:
fabricated account balances and fake trading proof. Its screenshot-oriented
"Present mode" removed editing controls and made the output look authentic.
There was no disclosure, educational context, verification workflow, or
anti-misuse boundary in the rendered product.

The redesigned Larpmaxxing experience changes the product from a fabrication
tool into a media-literacy tool. It now:

1. defines wealth/status LARPing in claim-level language;
2. explains the major tactic families from the supplied taxonomy;
3. provides fictional practice cases rather than accusing real people;
4. teaches an evidence-first verification method;
5. explicitly distinguishes suspicion from proof; and
6. makes its privacy and prototype limitations clear.

This is a strong conceptual match for the supplied definition, but it is not yet
a production fact-checking service. It does not retrieve posts, preserve source
artifacts, check records, explain score weighting, cite external research, or
support human review. The case score is a teaching device and must not be
presented as an automated truth score.

## What “the standard” means here

The material supplied in the brief is an informal taxonomy, not a published
technical, legal, or accessibility standard. It defines wealth/status LARPing as
constructing a deceptive online identity around unsupported claims of money,
ownership, success, expertise, or elite access.

For this audit, that material is converted into six testable product criteria:

| Criterion | Expected product behavior |
| --- | --- |
| Definition | Explain the difference between ordinary role-play, aesthetic performance, and a deceptive factual claim. |
| Tactics | Cover rented assets, staged sets, fake/cropped financial proof, luxury props, “old money” aesthetics, and guru funnels. |
| Motives | Explain monetization, social validation, and access/networking incentives without treating motive as proof. |
| Detection | Teach users to identify inconsistencies, preserve context, and seek independent corroboration. |
| Language | Define LARPer, to LARP, LARPy, and adjacent concepts while discouraging unsupported labels. |
| Harm control | Prevent the tool from becoming a harassment, doxxing, fraud, or accusation engine. |

WCAG 2.2 AA principles are used separately as the accessibility benchmark,
although this audit is an engineering review rather than a formal conformance
certification.

## Baseline findings

### Original purpose and content

The baseline product was titled “Prop Dashboard” and contained two editable
financial products:

- Halcyon, a mock consumer bank dashboard with editable balances and
  transactions;
- Cinder, a mock crypto portfolio with editable holdings, prices, gains, and
  transaction activity;
- local persistence plus JSON import/export;
- a chart generator; and
- a Present mode that hid all editing chrome for screenshots.

### Alignment with the supplied standard

The baseline accidentally demonstrated what fabricated financial interfaces can
look like, but did not label that behavior as deception or educate the user.
This is not meaningful fulfillment of the taxonomy.

| Area | Baseline result | Reason |
| --- | --- | --- |
| Definition | Fail | No mention of LARPing, unsupported identity claims, or the ownership/access distinction. |
| Tactics | Harmful overlap | Editable balances, gains, and activity could generate the fake screenshots described by the taxonomy. |
| Motives | Fail | No explanation of courses, signals, affiliate funnels, validation, or networking incentives. |
| Detection | Fail | No checklist, provenance, context capture, or corroboration workflow. |
| Language | Fail | No glossary or adjacent-concept distinction. |
| Harm control | Fail | No disclosure watermark, ethical boundary, or friction against deceptive export. |

### Baseline UX and accessibility

Strengths:

- concise visual design;
- mobile rearrangement for account and transaction data;
- keyboard focus styling;
- keyboard support for committing and cancelling inline edits;
- numeric formatting and stable derived calculations; and
- no dependency or build-chain risk.

Material problems:

- editable text was implemented with `contenteditable` spans rather than
  properly labelled form controls;
- tabs had `role="tab"` but omitted full tab relationships and keyboard arrow
  behavior;
- no page description, skip link, landmarks for tool controls, status
  announcements, or error association;
- important table content required horizontal scrolling on mobile;
- destructive actions depended on ambiguous × icons;
- imported JSON received only shallow shape validation;
- errors were swallowed in persistence code;
- the generated chart was ornamental but announced as if it represented real
  market history; and
- Present mode deliberately removed the strongest indication that values were
  editable.

## Redesigned product assessment

### 1. Definition: strong

The page leads with a direct working definition:

> Wealth and status LARPing is the deliberate construction of an online persona
> that implies financial success, ownership, expertise, or elite access that
> the available evidence does not support.

The supporting copy makes an important distinction the initial brief did not
state clearly enough: a luxury image is not itself proof of deception. A
testable claim and evidence mismatch are required.

Improvement over the brief:

- avoids treating all aspirational aesthetics as fraudulent;
- distinguishes access from ownership;
- distinguishes an impression (“this person seems rich”) from a factual claim
  (“this person says they own this car”); and
- avoids presenting a slang label as a verified fact about a person.

### 2. Tactic coverage: good, with gaps

Current coverage:

| Supplied tactic | Product coverage |
| --- | --- |
| Short-term rental shown as an asset | “Access framed as ownership” signal and staged-access demo. |
| Fake private-jet studio | Primary fictional case with matching studio evidence. |
| Fake/cropped financial proof | Trading screenshot case and unverifiable-proof signal. |
| Guru/course funnel | Lifestyle-as-sales-funnel signal and incentive step. |
| Batch-content/location clues | Consistency signal references repeated outfits, recycled locations, and timelines. |
| Photoshop/interface clues | Artifact-inspection workflow references edits and interface inconsistencies. |
| Shopping bags, boxes, and luxury props | Implicitly covered by the access signal, but not shown as a dedicated example. |
| “Quiet luxury” or “old money” aesthetics | Deliberately not treated as evidence by itself; this nuance should be made more explicit in future content. |
| Networking access motive | Not yet covered in enough depth. |

### 3. Motive coverage: partial

The redesign clearly covers:

- course and signal sales;
- affiliate/commercial conversion;
- investment solicitation;
- attention and status as possible incentives; and
- the principle that higher financial stakes require stronger evidence.

It does not yet give social validation and networking access the same depth as
monetization. A future motive module should show that a deceptive status claim
can seek invitations, partnerships, dating access, press attention, or insider
credibility even when no direct sale occurs.

### 4. Detection and verification: strong educational foundation

The four-step playbook is the core product improvement:

1. **Isolate the claim.** Quote the smallest testable claim.
2. **Inspect the artifact.** Preserve the caption, date, disclosures, edits, and
   visible context.
3. **Cross-check the story.** Seek primary and independent sources; reposts do
   not count as corroboration.
4. **Assess the incentive.** Identify what trust or conversion the performance
   is intended to produce.

This is more reliable than a “spot the Photoshop mistake” approach because it
can also handle genuine imagery attached to a misleading claim.

Remaining limitations:

- the URL field does not fetch content;
- no evidence files or citations can be attached;
- no provenance or time-of-capture record exists;
- no reverse-image, EXIF, record, or credential lookup is integrated;
- no contrary-evidence field exists;
- no exportable report exists; and
- demo scores are authored examples rather than calculated outputs.

### 5. Language: strong

The glossary defines:

- LARPer;
- to LARP;
- LARPy; and
- clout chasing.

It also recommends describing the inconsistency before labeling the creator.
The clout-chasing comparison is useful because attention-seeking and deception
overlap but are not synonymous.

An additional production glossary should distinguish:

- parody and disclosed role-play;
- aspirational or editorial imagery;
- puffery;
- material misrepresentation;
- impersonation;
- undisclosed advertising; and
- investment or financial-advice claims.

### 6. Harm controls: good for a prototype

Implemented safeguards:

- all examples are explicitly fictional;
- the score is called “evidence risk,” not truth or fraud probability;
- the interface states that scores prioritize review rather than determine
  guilt;
- pasted URLs are not fetched or scraped;
- saved state remains local to the browser;
- a prominent section says “Suspicion is not proof”;
- the ethics copy prohibits harassment, doxxing, protected-trait inference, and
  taste-based character judgment; and
- the workflow asks for contrary evidence.

Production requirements:

- moderation and abuse-reporting paths;
- retention and deletion controls;
- personally identifiable information handling rules;
- claim-evidence audit trails;
- rate limits and anti-targeting controls;
- minimum evidence thresholds before sharing a report;
- human review for high-impact claims;
- legal review for defamation, privacy, consumer-protection, and financial
  promotion risks; and
- a correction and appeal workflow.

## UX review

### Information architecture

The page now follows a coherent learning journey:

1. understand the term;
2. recognize signal families;
3. practice on fictional cases;
4. learn a repeatable verification method;
5. absorb the ethical boundary; and
6. use precise language.

The sticky navigation provides direct access to each core task. Mobile
navigation becomes a full-screen menu, and all in-page destinations remain
available without JavaScript.

### Interaction design

Implemented:

- selectable demo cases with immediate result updates;
- URL validation with an honest no-fetch message;
- locally saved case state;
- a copyable review checklist;
- tab-like workflow steps with arrow, Home, and End keyboard navigation;
- status announcements through an ARIA live toast; and
- responsive controls with at least 44-pixel targets.

The URL input is intentionally a guided-review entry point, not a fake analyzer.
This avoids claiming that a browser-only prototype can inspect external content.

### Visual design

The new direction uses:

- editorial serif headlines paired with a system sans serif;
- warm paper, dark green, coral, and acid-lime colors;
- a restrained card system;
- visible borders and offsets rather than excessive shadows;
- custom CSS illustration to explain staged luxury visually;
- asymmetrical but readable layouts; and
- a dark, task-focused case-lab section.

The design avoids mimicking a bank or brokerage and gives the product a distinct
media-literacy identity.

### Responsive behavior

Layouts are explicitly adapted at 900px and 620px:

- the hero, analyzer, workflow, and ethics layouts stack;
- signal cards reduce from mixed 5/7-column spans to two columns and then one;
- the menu becomes touch-friendly;
- forms stack;
- case output controls wrap; and
- the glossary moves from a three-part row to a one-column reading flow.

## Accessibility review

### Improvements implemented

- semantic header, nav, main, section, article, footer, and form landmarks;
- unique page title and meta description;
- skip link;
- visible focus indication;
- reduced-motion handling;
- no color-only signal labels;
- text alternatives for meaningful illustration and scores;
- explicit button types and labels;
- native URL validation;
- `aria-live` status feedback;
- tab semantics and expected keyboard navigation for the playbook;
- pressed state for selectable cases;
- mobile controls sized for touch; and
- logical source order that matches the visual reading order.

### Items requiring formal testing

The following cannot be certified by static review alone:

- color contrast under computed browser rendering;
- zoom and text-spacing behavior through 400%;
- VoiceOver, NVDA, JAWS, and TalkBack announcements;
- high-contrast and forced-colors behavior;
- focus behavior when the mobile menu opens and closes;
- exact target-size conformance at every breakpoint; and
- browser/OS combinations.

### Known accessibility improvements still needed

1. Trap focus inside the open mobile menu or present it as a non-modal disclosure
   that does not cover the viewport.
2. Close the menu on Escape and restore focus to the trigger.
3. Add `aria-controls` relationships from every case button to the output.
4. Provide a non-circular text equivalent for the risk dial adjacent to the
   score.
5. Test CSS-generated illustration contrast in Windows forced-colors mode.
6. Add an inline error message associated with the URL field rather than relying
   only on browser validation and a toast.

## Privacy, security, and trust

Current privacy exposure is low:

- no network requests are made by application JavaScript;
- no analytics or trackers are present;
- no account or identity is required;
- only fictional case identifiers are stored; and
- pasted URLs are not persisted.

Current technical risks:

- dynamically rendered demo content uses `innerHTML`. Values are hard-coded, so
  it is not currently exploitable, but future user-controlled content must use
  DOM text nodes or sanitization;
- `localStorage` is origin-readable and should never hold sensitive evidence;
- there is no Content Security Policy;
- there is no integrity or deployment configuration; and
- there are no automated tests.

If URL retrieval is added, the architecture must guard against server-side
request forgery, malicious redirects, tracking pixels, oversized media,
credential leakage, illegal content retention, and platform terms-of-service
violations.

## Technical quality

Strengths:

- no third-party dependencies;
- fast static delivery;
- no build step;
- progressive navigation;
- deterministic demo data;
- CSS and JavaScript contained in one deployable file; and
- no collection or transmission of user data.

Trade-offs:

- one large HTML file is easy to deploy but difficult to test and maintain;
- content and application behavior are tightly coupled;
- no component, design-token package, routing, content model, or localization
  boundary exists;
- no linting, formatting, test, or CI configuration exists; and
- there is no production error telemetry.

For the next implementation phase, split the project into semantic components
and store educational content in structured data. Do not add a framework solely
for visual polish; add one only when routing, evidence workflows, localization,
or team maintenance justify it.

## Prioritized roadmap

### Priority 0 — trust and correctness

1. Publish score methodology or remove numeric scores in favor of “low,”
   “review,” and “high-priority review.”
2. Add citations for definitions, misinformation research, advertising rules,
   and financial-promotion guidance.
3. Build an explicit claim/evidence/contrary-evidence data model.
4. Add correction, appeal, deletion, and abuse-reporting policies before any
   public case publishing.
5. Complete legal and safety review before processing identifiable people.

### Priority 1 — useful product depth

1. Add evidence capture with source URL, timestamp, archived context, notes, and
   confidence.
2. Create more fictional cases for shopping-bag staging, “old money” aesthetics,
   credential claims, charity/status claims, and networking access.
3. Add a side-by-side claim matrix: claimed, observed, corroborated, unresolved.
4. Produce an accessible, citation-rich report export.
5. Add onboarding that teaches why a clue is not proof.

### Priority 2 — UX and accessibility hardening

1. Complete assistive-technology, keyboard, zoom, forced-colors, and contrast
   testing.
2. Add focus management and inline form errors.
3. Add a low-bandwidth mode if external media is introduced.
4. Localize the glossary and examples; slang meaning varies across communities.
5. Add print styles for the playbook and report.

### Priority 3 — engineering maturity

1. Split content, styles, and behavior into maintainable modules.
2. Add unit tests for state and scoring, accessibility checks, and responsive
   browser tests.
3. Add a strict Content Security Policy and deployment headers.
4. Introduce schema validation for persisted or imported records.
5. Add privacy-preserving telemetry only after defining a measurement plan.

## Product success measures

Avoid measuring success by accusations generated or “LARPers caught.” Better
measures are:

- percentage of reviews that quote a specific claim;
- percentage that record independent and contrary evidence;
- reduction in unsupported labels after using the playbook;
- completion and comprehension rates for fictional cases;
- accessibility task completion across assistive technologies;
- correction rate and time to correction; and
- user understanding that a risk score is not a verdict.

## Final verdict

The baseline product failed the supplied wealth/status LARPing standard and
created a concrete misuse risk by facilitating fake financial screenshots.

The redesign strongly fulfills the definition, detection, language, and
harm-control criteria as an educational prototype. It partially fulfills tactic
and motive coverage and intentionally stops short of claiming real automated
analysis. The most important next step is not a more sophisticated detector; it
is a transparent evidence model with citations, contrary evidence, human review,
and correction rights.
