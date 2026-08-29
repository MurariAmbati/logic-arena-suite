# Logic Arena Suite

Logic Arena is a phone-first training suite for strategic reasoning, game theory, scenario planning, and hard logic puzzles.

Play the public build at [logic-arena-suite on GitHub Pages](https://murariambati.github.io/logic-arena-suite/).

## Local preview

```powershell
python -m http.server 4173 --directory work
```

Open `http://localhost:4173/` on desktop or your phone on the same network.

## Deployment

- GitHub Pages deploys automatically from `main` through `.github/workflows/gh-pages.yml`.
- Vercel can deploy the repository directly; `vercel.json` routes the site from `work`.

The app is a static PWA and can be installed from a supported mobile browser.
