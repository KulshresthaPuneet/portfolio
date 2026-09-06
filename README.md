# Puneet Kulshrestha — Portfolio

A single-page portfolio built with plain HTML, CSS, and JavaScript — no build step, no dependencies, no framework. Open `index.html` in a browser and it works.

## Files

```
portfolio/
├── index.html      # all content lives here
├── style.css       # design system + layout
├── script.js       # mobile nav, active-link highlighting, scroll reveal
├── assets/
│   └── resume.pdf  # powers the "Download résumé" buttons
└── README.md
```

## Before you publish

1. **Swap the résumé.** Replace `assets/resume.pdf` with your latest PDF (keep the filename, or update the two `href="assets/resume.pdf"` references in `index.html`).
2. **Check the links.** GitHub, LinkedIn, email, and phone are wired up in `index.html` — search for `KulshresthaPuneet`, `linkedin.com`, `mailto:`, and `tel:` to confirm they're current.
3. **Add real project links, if you have them.** The project cards currently have no individual links since no repo/live URLs were provided. If any of the four projects (AI Virtual Assistant, Lung Disease Classification, Resume Builder, OCR Web App) live in a public repo, add a link inside `.project-card` in `index.html`.
4. **Optional: project screenshots.** Each project card currently uses a small line-art icon (`.project-icon`) instead of a screenshot. Swap in real screenshots by replacing the `<svg>` with an `<img>` if you'd like.

## Deploying

Pick whichever is easiest — all three are free for a static site like this.

### GitHub Pages
1. Push this folder to a GitHub repo (e.g. `KulshresthaPuneet/portfolio`).
2. Repo → **Settings → Pages** → Source: `Deploy from a branch` → Branch: `main`, folder `/ (root)`.
3. Your site goes live at `https://kulshresthapuneet.github.io/portfolio/`.
4. To use `puneetkulshrestha.dev` or similar, add a `CNAME` file with your domain and point your DNS `A`/`CNAME` records at GitHub Pages.

### Vercel
1. `npm i -g vercel` (or use the Vercel dashboard → "Add New Project" → import this folder/repo).
2. From inside the `portfolio` folder, run `vercel` and follow the prompts. No build command needed — it's static.

### Netlify
1. Drag and drop the `portfolio` folder onto [app.netlify.com/drop](https://app.netlify.com/drop), **or**
2. Connect the GitHub repo in the Netlify dashboard with build command left blank and publish directory set to `/`.

## Customizing the design

All design tokens (colors, fonts, spacing) live at the top of `style.css` under `:root`. The palette is:

| Token       | Hex       | Used for                          |
|-------------|-----------|------------------------------------|
| `--ink`     | `#0A1120` | Page background                    |
| `--panel`   | `#101B2E` | Cards, panels                      |
| `--signal`  | `#E4A33E` | Primary accent (buttons, highlights) |
| `--foam`    | `#7FCBBE` | Secondary accent (used sparingly)  |
| `--paper`   | `#EAEFF6` | Primary text                       |
| `--slate`   | `#9AA6BC` | Secondary text                     |

Headings use **Fraunces** (serif), body text uses **IBM Plex Sans**, and the small mono labels (dates, the hero diagram's caption) use **IBM Plex Mono**. All three are loaded from Google Fonts in `index.html`.

## Accessibility notes already handled

- Skip-to-content link for keyboard users
- Visible focus rings on every interactive element
- `prefers-reduced-motion` respected (disables the flowing pipeline animation and scroll-reveal)
- Semantic landmarks (`header`, `nav`, `main`, `section`, `footer`)
- Color contrast checked for text-on-background pairs

## Contact form

There isn't one — a static site has nowhere to send form submissions without a backend or a third-party service (Formspree, Netlify Forms, etc.). Instead, the contact section links straight to email and phone, which is more reliable than a form that silently goes nowhere. If you want a real form later, Netlify Forms is the fastest way to add one without writing backend code.
