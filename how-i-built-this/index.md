---
title: "How I Built This E-Portfolio"
layout: single
author_profile: false
classes: wide
toc: true
toc_label: "On this page"
toc_icon: "list"
permalink: /how-i-built-this/
---

Hi! I’m Brenda Laime. This page is a simple walkthrough of what I did to build my e-portfolio on GitHub Pages. I wrote it the way I wish someone explained it to me. 

**Live site:** [https://brendalaime.github.io](https://brendalaime.github.io)

---

## 1) Create the site repository
- I logged into GitHub and created a **public** repo named **brendalaime.github.io** (the name matters; it makes the site live at `https://brendalaime.github.io`).
- I cloned it to my computer with **GitHub Desktop** so I could edit files locally.

## 2) Start with the Minimal theme (class starter)
- I downloaded the **Minimal** theme zip from GitHub and copied its files into my repo.
- I committed and pushed. The site deployed and matched the Minimal demo — good sanity check.

## 3) Switch to the Minimal Mistakes theme (side quest for class)
- I removed the leftover Minimal theme files (like `_layouts`, `_includes`, `_sass`, `Gemfile`, etc.) so nothing conflicted.
- I enabled **Minimal Mistakes** with a remote theme and a tiny CSS file:
  - `_config.yml` highlights:

    ```yaml
    remote_theme: "mmistakes/minimal-mistakes@4.24.0"
    plugins:
      - jekyll-remote-theme
      - jekyll-include-cache
    minimal_mistakes_skin: "default"
    ```

  - `assets/css/main.scss` (this loads the theme):

    ```scss
    ---
    # Only the main Sass file needs front matter
    ---
    @import "minimal-mistakes/skins/{{ site.minimal_mistakes_skin | default: 'default' }}";
    @import "minimal-mistakes";
    ```

## 4) Configure site settings
- In `_config.yml` I set:
  - `title`, `description`
  - social links
  - `logo` path: `/assets/img/logo.png`
  - `author.avatar`: `/assets/img/brenda-headshot-180.png`
- I kept everything small and readable. Commit → push.

## 5) Replace stock images and add my headshot
- I put images into `assets/img/`.
- I renamed my headshot to **brenda-headshot-180.png** and set it as my avatar in `_config.yml`.

## 6) Add my résumé (PDF) and link it
- I put my PDF in `assets/resume/Laime_Brenda_Resume.pdf`.
- In `index.md` I added a link: **[Download my résumé (PDF)](/assets/resume/Laime_Brenda_Resume.pdf)**

## 7) Write my homepage (index.md)
- I replaced the sample text with my own sections:
  - **Summary**
  - **Work Experience**
  - **Education**
  - **Selected Projects**
  - **Skills**
  - **Achievements**
  - **Résumé** (the link above)
  - **Links**
- I used Markdown basics: `#` headers, **bold**, *italics*, lists, and links.

## 8) Verify deployments
- After every commit, I checked **Actions ▸ pages build and deployment**.
- Green check = published. Then I refreshed `https://brendalaime.github.io`.

## 9) Screenshots
- **Home page:**  
  ![Home screenshot of my finished homepage](/assets/img/home-screenshot.png){: width="30%" }
  *My homepage after switching to Minimal Mistakes.*

## Troubleshooting I hit (and fixed)
- **Red X in Actions:** I clicked the failed run, opened **build** logs, and fixed the file mentioned. Next commit turned green.
- **Avatar not showing:** The image path in `_config.yml` didn’t match the actual filename in `assets/img/`.
- **Wrong paths:** Most issues were tiny typos in file paths.

---

## What I learned
- GitHub Pages publishes automatically from the **main** branch.
- A page becomes a **subpage** when you put an `index.md` inside a folder (like this page).
- Minimal Mistakes is powerful but simple to enable with a **remote theme**.

## Helpful links
- Minimal theme: https://github.com/pages-themes/minimal  
- Minimal Mistakes: https://github.com/mmistakes/minimal-mistakes  
- GitHub Pages docs: https://docs.github.com/pages

[← Back to home](/)
