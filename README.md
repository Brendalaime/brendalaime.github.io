# brendalaime.github.io

**E-portfolio for OM 620 — Fall 2025**  
**Student:** Brenda Raquel Laime Jalil

**Live site:** https://brendalaime.github.io

**Milestone II (tutorial subpage):** https://brendalaime.github.io/how-i-built-this/

This site runs on GitHub Pages using the **Minimal Mistakes** theme (`remote_theme`).

## What’s inside
- `index.md` — homepage with summary, experience, education, projects, skills, achievements, and résumé link
- `how-i-built-this/` — **Milestone II tutorial** (step-by-step guide)
- `assets/img/` — headshot & screenshot
- `assets/resume/` — résumé PDF (`Laime_Brenda_Resume.pdf`)
- `assets/css/main.scss` — Minimal Mistakes stylesheet imports
- `_config.yml` — site settings (theme, plugins, avatar/logo, nav)

## Tech
- Theme: `mmistakes/minimal-mistakes@4.24.0`
- Plugins: `jekyll-remote-theme`, `jekyll-include-cache`

## How to update
1. Edit content in **`index.md`** or add a new subpage as a folder with `index.md`.
2. Commit changes to **`main`**.
3. GitHub Actions builds & deploys automatically (check the **Actions** tab).

## Troubleshooting (summary)

- **Build failed (red X):** Open the failed run → check the end of **Build with Jekyll** logs.  
  **Common fixes:** remove leftover theme folders (`_layouts`, `_includes`, `_sass`) from other themes, confirm `assets/css/main.scss` exists, and verify file paths.
- **Image/PDF not loading:** Paths are **case-sensitive**. Use absolute paths like `/assets/img/...` and `/assets/resume/...`.
- **Avatar/logo not showing:** Make sure the file is in `assets/img/` and `_config.yml` points to the exact filename (e.g., `/assets/img/brenda-headshot-180.png`).

---

© 2025 Brenda Laime
