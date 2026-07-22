# Bernardo Lin — Personal Website

A static personal portfolio site for RTL Design & Design Verification roles.
Plain HTML, CSS, and JavaScript — no build step, no framework.

## Structure

```
.
├── index.html                     # All page content
├── css/style.css                  # Styles + light/dark theme
├── js/main.js                     # Theme toggle, mobile menu, footer year
├── files/Bernardo_Lin_Resume.pdf  # Resume (linked from Resume buttons)
├── .nojekyll                      # Serve as plain static files on GitHub Pages
└── README.md
```

## Preview locally

Open `index.html` directly in a browser, or serve it (recommended, so the
resume link and relative paths behave):

```bash
python -m http.server 8000
# then visit http://localhost:8000
```

## Deploy to GitHub Pages

Your site will live at `https://<username>.github.io`. Since your GitHub
username is **kingsmanbl**, the repository must be named exactly
`kingsmanbl.github.io`.

1. Create a **public** repo named `kingsmanbl.github.io` on GitHub.
2. From this folder, push everything to it:

   ```bash
   git init
   git add .
   git commit -m "Initial personal website"
   git branch -M main
   git remote add origin https://github.com/kingsmanbl/kingsmanbl.github.io.git
   git push -u origin main
   ```

3. On GitHub: **Settings → Pages → Build and deployment**. Set **Source** to
   "Deploy from a branch", branch `main`, folder `/ (root)`. Save.
4. Wait ~1 minute, then open **https://kingsmanbl.github.io**.

To update the site later, edit files and `git add . && git commit && git push`.

## Things you may want to change

- **Resume**: replace `files/Bernardo_Lin_Resume.pdf` with a newer version
  (keep the same filename, or update the two links in `index.html`).
- **Photo**: the hero photo is `images/profile.jpg` (pulled from your GitHub
  avatar). Swap the file to change it — keep the name, or update the
  `hero-avatar` `src` in `index.html`.
- **Favicon**: `images/favicon.svg` (a purple "BL" tile). Edit the SVG to change it.
- **Social preview**: `images/og-image.png` (1200×630) is the card shown when
  the link is shared on LinkedIn/Slack/iMessage. The `og:image` / `twitter:image`
  meta tags in `index.html` point to `https://kingsmanbl.github.io/images/og-image.png`
  — that absolute URL must match your final site URL for previews to load.
- **Links**: LinkedIn, GitHub, and email are set in `index.html`.
- **Colors**: the accent is UW Purple (`--accent: #4b2e83` light / `#b69cf0`
  dark), with UW gold as the secondary. Edit the CSS variables at the top of
  `css/style.css` to change the palette — everything (buttons, tags, gradient
  bar, section numbers) is driven from those `--accent*` / `--grad` variables.
- **Fonts**: Space Grotesk (headings), IBM Plex Sans (body), IBM Plex Mono
  (labels, nav, tags) — loaded from Google Fonts in `index.html`.
- **Repo links** in the "More on GitHub" section assume repo names under
  `github.com/kingsmanbl/...` — adjust if you rename any.
```
