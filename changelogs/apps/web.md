# web

## 1.5.0

- Add a Studio docs page on saving `.rungs` files, exporting `.L5X` for Logix Designer, and sharing links

## 1.4.1

No changes in this release.

## 1.4.0

- Add Boiler Interlocks and Burner Control exercises

## 1.3.0

- Browse the exercises as ordered courses at rungs.dev/courses, each with its own page, progress and starting point
- The free tier is now the Boolean Logic course
- Add 10 new exercises to the catalog

## 1.2.1

- Progress made before signing in now follows you into your account more reliably, with a safer hand-over behind the scenes

## 1.2.0

- Show Studio links on phones and add a closing call-to-action to the landing page

## 1.1.0

- Exercises, pricing, and sign-in now live on rungs.dev; learn.rungs.dev redirects there
- Your account and exercise progress carry over unchanged
- The documentation intro moves from /docs/intro to /docs

## 1.0.0

- New rungs.dev website, migrated from the Docusaurus site in `apps/docs` — landing page, documentation, and blog now run on Next.js with Fumadocs, at the same URLs
- Add site-wide search across documentation, blog posts, and the exercise catalog in one dialog
- Publish `/llms.txt`, `/llms-full.txt`, and per-page Markdown behind a Copy Markdown control on every documentation page and blog post

## Previously released as `docs`

rungs.dev ran on Docusaurus until this app replaced it at the same URLs.
Those releases are kept here so the history survives that app's removal.

### 1.10.3

- Allow sharing individual Plus exercise AOIs while prohibiting catalog-scale redistribution.
- Update the Privacy Policy to cover email code sign-in and the bot check that protects it

### 1.10.1

- Stop the docs site and Studio from loading blank right after a new version ships

### 1.10.0

- New post "What Data Taught Me About Testing Time-Based PLC Logic"
- Show preset and accumulator values inside the timer and counter blocks on the ladder instruction pages
- Teach the timer transition-window idiom in test guidance so generated tests accept every correct implementation
- Add per-case `scanTime` and hold-only steps to tests — timing checks can now run finer than the 100 ms default

### 1.9.0

- Add a blog post GPT-5.6 Luna is my new favorite model for Ladder Logic

### 1.8.0

- Add OSR and OSF one-shot instructions to the Ladder Diagram
- Add OSRI and OSFI one-shot instructions and the FBD_ONESHOT data type to Structured Text
- Make timers keep accurate time when scans run late, modeled on measured ControlLogix® behavior

### 1.7.0

- New Ladder Diagram one-input math instructions: ABS, SQRT, and NEG (Math tab), with emulator-verified edge cases
- Add Ladder Logic AND, OR, XOR, NOT bitwise blocks and a Move/Logical toolbar tab
- Add Ladder Logic MVM, CLR, and BTD blocks to the Move/Logical tab
- Major faults now stop the scan: array subscript errors and negative timer presets abort at the faulting instruction
- Add NOP, AFI, and MOD ladder instructions
- Run a Logix-style prescan pass before the first scan; setting EnableIn to 0 now skips Logic and clears EnableOut
- Radix numeric literals in ST and Ladder: 16#, 2#, and 8# DINT bit patterns with underscore grouping
- ST AND/OR/XOR/NOT are bitwise on numeric operands, matching Logix®; & synonym pinned; bitwise legal in subscripts
- Structured Text timers and counters ignore runtime .ACC writes, matching Logix

### 1.6.0

- Add blog post on which AI models write the best Ladder Logic and Structured Text, and why Relay runs on Gemini

### 1.5.0

- Add 'Why Relay reads your PLC logic better than ChatGPT' blog post

### 1.4.1

- Add `hold` to AOI unit tests — assert outputs keep their value on every scan of a step

### 1.4.0

- Add Scan Cycle docs and teach Relay to explain the one-scan delay from rung and statement order
- Measure usage anonymously without cookies when you decline analytics
- Point the Exercises link to the new Learn site and Community to GitHub Discussions
- Add Practice links from Ladder instruction docs to matching exercises in Learn
- Clarify in the Privacy Policy and Terms that we may read exercise snapshots only to fix Service issues

### 1.3.0

- Show a cookie banner so you can accept or reject product analytics

### 1.2.0

- Add 'AI-assisted PLC learning' blog post.
- Add a Relay AI assistant guide to the docs covering what context Relay reads, common prompts, and an FAQ.
- Feature Relay AI assistant on the rungs.dev homepage
- Update privacy and terms to cover the Relay AI assistant: what's sent, where it goes, and how prompts are retained.

### 1.1.0

- Model numeric semantics on Studio 5000 Logix Designer (banker rounding, destination-driven division, 32-bit REAL).
- Document array index expression rules: which forms are allowed (integer literals, DINT tags/members, arithmetic) and which are rejected (REAL, BOOL, whole-array, bit access, non-integer math).
- Publish 0.7.0 release notes blog post

### 1.0.0

- Add Tags and Ladder Logic documentation.

### 0.4.1

- Add links to exercises.rungs.dev

### 0.4.0

- Add documentation for AOI unit tests

### 0.3.0

- Add Privacy Policy and Terms and Conditions
- Introduce feature showcase

### 0.2.0

- Introduce Ladder Logic editor post

### 0.1.1

- Add Algolia search

### 0.1.0

- Initial release

## Previously released as `learn`

The exercise catalog, pricing, and sign-in shipped as a separate app at
learn.rungs.dev until they moved onto rungs.dev. Its releases are kept here
so that history is not lost when the app is removed.

### 0.7.4

- Sign in with a one-time code emailed to you, alongside Google and GitHub

### 0.7.0

- Add 20 playable exercises — math, bit logic, masked moves, filters, and sequencers — bringing the catalog to 60
- Reorder the catalog easiest-first and update which 20 exercises are free
- Tighten tests, reference solutions, and behavior notes across existing exercises, with worked binary examples

### 0.6.0

- Add a Groups option on Pricing to request custom plans for classes, teams, and hiring

### 0.5.1

- Edit hero section

### 0.5.0

- Add Paddle-powered Plus checkout for the exercise paywall
- Add ten exercises and reorder the catalog so concepts build on each other — 40 exercises now playable
- Add nine exercises spanning XOR logic, edge detection, timer patterns, run-time tracking, and configurable scaling

### 0.4.0

- Add the One-Scan Delay exercise: one lamp follows a button instantly, another follows it one scan later
- Measure usage anonymously without cookies when you decline analytics
- Fix the Hysteresis exercise example to match its behavior: output turns on at the high limit and off at the low limit
- Move Press-Toggle Lamp after Rising Edge, raise it to medium difficulty, and clarify what it teaches

### 0.3.0

- Groundwork for the upcoming Rungs Learn launch: sign-in with saved progress, plus Ladder and Structured Text solving
- Add new edge-detection, timer, and flasher exercises with reference solutions to the catalog

### 0.2.0

- Launch the new Learn site at learn.rungs.dev with 100 PLC programming exercises spanning bit logic to batch reactors.

## Previously released as `exercises`

The original exercise site at exercises.rungs.dev, whose routes now redirect to
rungs.dev/exercises. Kept here so the history survives that app's removal.

### 0.2.11

### 0.2.4

- Add a cookie-consent banner to the exercises site

### 0.2.3

- Show a notice on the old exercise pages pointing learners to the new catalog at learn.rungs.dev

### 0.2.0

- Add FAQ

### 0.1.1

- Add sitemap

### 0.1.0

- Initial release
