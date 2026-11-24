# BAFS Workforce & Succession Intelligence

Interactive Strategic Workforce Planning (SWP) & Retirement Horizon Executive Console (2026–2036).

## Deployment Structure

This folder contains only the standalone files required for GitHub / GitHub Pages deployment:

- `index.html` — Self-contained HTML5 / CSS3 / Vanilla JS application (logo, favicon, styles, scripts, and datasets are embedded inline).
- `.nojekyll` — Disables Jekyll processing on GitHub Pages so static assets are served directly.
- `.gitignore` — Blocks OS metadata and raw HR spreadsheets (`*.xlsx`, `*.csv`, `retirees_compact.json`) from being committed accidentally.
- `README.md` — Project documentation and deployment guide.

## ⚠️ PDPA & Confidentiality Notice

`index.html` currently embeds real employee names inside `RETIREES_0_10`.
- **Do NOT deploy this file to a Public GitHub repository / free Public GitHub Pages** as-is, because anyone can inspect the HTML source (`View Source` / DevTools) and read employee PII.
- Use one of these safer deployment options:
  1. **Private Repository + GitHub Enterprise/Organization Private Pages** (or internal hosting / SharePoint / Intranet).
  2. **Private GitHub Repo connected to Cloudflare Access / Vercel Auth / Netlify Password Protection** restricted to BAFS accounts.
  3. **Anonymize `RETIREES_0_10`** (replace employee names with anonymized codes) if you intend to host on a public URL.

## Quick Deploy to GitHub Pages

```bash
cd github-deploy
git init
git add .
git commit -m "Initial deploy: BAFS Workforce Horizon Console"
git branch -M main
git remote add origin https://github.com/<your-org-or-username>/<repo-name>.git
git push -u origin main
```

Then in GitHub Repository **Settings → Pages → Build and deployment**:
- Source: **Deploy from a branch**
- Branch: `main` / `/ (root)`
