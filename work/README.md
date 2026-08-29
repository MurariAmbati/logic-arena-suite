# Logic Arena Suite

Strategy-first mobile training app with logic-and-game-theory scenario puzzles designed to improve decision discipline, adversarial reasoning, and strategic planning.

It now runs:

- 116 core families with dedicated and adaptive generators
- 34 advanced families synthesized from core families
- 150 total families, plus deterministic difficulty mutations and per-family anti-repeat adaptation

## Core gameplay

- ~**3944 target games** (116 families with 34 base variants each, plus runtime adaptive jitter and advanced-family synthesis), dynamically scaled by mode, profile, and streak context.
- Difficulty tags:
  - Easy: ~4,400 hidden worlds each
  - Medium: ~9,800 hidden worlds each
  - Hard: ~24,000 hidden worlds each
- Scenario budget is also jittered per game to increase randomness.
- Training modes:
  - Standard: regular hidden-world count and strictness
- Expert: 28% more worlds and tighter streak-safe thresholds
- Adversarial: highest variance, hardest strictness, and longer targets
- Adversarial Twist: curated anti-repeat and scenario pressure variant for deep-strategy recalibration
- Apex: maximum uncertainty compression and strict streak gates
- Colossus: extreme stress-test mode for high-intensity practice
- Titan: maximal uncertainty + anti-repeat pressure for long-range strategic planning under adversarial ambiguity
- Zenith: highest-depth strategic load with strictest phase recovery cadence and strongest anti-repeat constraints
- Scenarios are built with explicit game-theory families and calibrated uncertainty.
- Family-adaptive learning now adjusts scenario pressure and generation quotas by performance history.
- Family archetype selection is weighted by strength and per-corpus randomization is mixed each shuffle.
- New catalog filter: `Adaptive streak-safe` for progressive strictness.
- New suite filter for cognitive pathways: `Cognitive Reasoning`, `Game Theory`, `Markets & Ops`, `Security & Resilience`, `Deception & Counterfactuals`, and `Synthesis Labs`.
- Progress saved in `localStorage` under `logicArenaProgressV6` (compatible with save formats `v5`, `v6`, `v7`, `v8`, `v9`, `v10`, `v11`, and `v12`).
- Advanced families are synthesized each generation pass using deterministic family-specific feature randomization for harder mastery ladders.
- Scenario mutation blueprints layer hidden noise, late revisions, policy decay and framing uncertainty so repeated puzzle patterns stay harder over time.
- Streak engine with **quality streaks** (confidence-thresholded perfect runs), dynamic targets, and actionable coaching.
- XP and level system: correct answers earn strategic XP by difficulty, with higher rewards for streak-safe and advanced modes to make progress tangible.
- Perfect streak workflow now includes a 3-phase protocol and adaptive queue guidance.
- Perfect drill guidance is now explicitly phone-optimized with strict run targets, recovery rules, anti-repeat family pacing, and a streak curriculum mode.
- Extra phone-first polish and accessibility-focused controls.
- Install-ready PWA behavior: manifest + service worker + install button and platform-specific install hint.

## Run on desktop or phone

From `work/`:

- Open `index.html` directly, or run a local server:
  - `python -m http.server 4173`
  - Then open `http://localhost:4173/`.
- On the phone, open the URL and choose **Add to Home Screen** (Android / iOS).
- The app uses a manifest + service worker so it behaves like an installable app.
- Use **Install app** button where supported (Chrome/Edge/Android), or browser menu **Add to Home Screen** on iOS Safari.

## Deploying (fastest paths)

### Deploy on Vercel

From the project root:

1. Install CLI once:
   - `npm i -g vercel`
2. Authenticate:
   - `vercel login`
3. Deploy directly from the repo root (route to `work` via `vercel.json`):
   - `vercel --prod`

### Deploy on GitHub Pages

1. Push this project to your GitHub repository (`main` branch).
2. The included workflow file at `.github/workflows/gh-pages.yml` will publish `work/` to GitHub Pages.
3. In repository Settings → Pages:
   - Source: **GitHub Actions**.
   - Site will be available at:
     - `https://<your-username>.github.io/<repo-name>/`

Note: if you have a custom host path, keep `manifest.webmanifest` `start_url` and relative asset paths unchanged for clean hosting.

## Controls

- Filter by category and difficulty.
- Filter by suite tracks to run themed strategic campaign days (for example, "Game Theory", "Markets & Ops", or "Security & Resilience").
- `Random` and `Hard focus random` for training sessions.
- `Perfect drill` opens high-confidence games and explains the perfect-streak process.
- `Training mode` raises variance and stricter targets for expert/adversarial/Apex drills.
- `Adaptive streak-safe` queue mode now prioritizes strong streak-safe candidates.
- `Shuffle catalog` regenerates the full suite from a new seed.
- `Hints` toggles detailed evidence text.
- `Streak guide` adjusts coaching verbosity.
- `Streak curriculum` adds phase-specific coaching for building quality streaks.
- `Reset progress` clears your saved game history.

## Files

- `index.html` - UI + game generation logic (single-file app)
- `manifest.webmanifest` - install metadata
- `service-worker.js` - offline cache for resilient loading
- New: dedicated Strategic Thinking Program, Metagame Reality Lab, and Theory Synthesis Lab suites for progressive strategic depth

