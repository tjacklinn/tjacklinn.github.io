# Tiia Jacklin portfolio site

Static personal portfolio website for GitHub Pages. The site is built with plain HTML, CSS, and a small amount of inline JavaScript, so it does not require Node, npm, a build step, or a theme framework.

## Files

```text
.
├── index.html   # Page content, tab behavior, theme toggle, expandable abstracts
├── styles.css   # Layout, typography, light/dark themes, responsive styling
└── README.md    # Setup and editing instructions
```

Only `index.html` and `styles.css` are required for the website to run. This README is included so the repository documents how to edit and deploy the page.

## Recommended GitHub Pages setup

For a personal GitHub Pages site, create a repository named exactly:

```text
tjacklinn.github.io
```

When GitHub Pages is enabled, the site will be available at:

```text
https://tjacklinn.github.io/
```

## Setup using the GitHub website

1. Log in to GitHub as `tjacklinn`.
2. Create a new public repository named `tjacklinn.github.io`.
3. Upload these files to the repository root:
   - `index.html`
   - `styles.css`
   - `README.md` if you want the instructions saved in the repository
4. Commit the files to the `main` branch.
5. Open the repository settings.
6. Go to Pages.
7. Under “Build and deployment,” choose:
   - Source: `Deploy from a branch`
   - Branch: `main`
   - Folder: `/ (root)`
8. Save the settings.
9. Wait a minute or two, then open `https://tjacklinn.github.io/`.

## Setup using the command line

If you prefer using Git locally, place the files in a folder and run:

```bash
git init
git add index.html styles.css README.md
git commit -m "Initial portfolio site"
git branch -M main
git remote add origin https://github.com/tjacklinn/tjacklinn.github.io.git
git push -u origin main
```

Then enable GitHub Pages in the repository settings as described above.

## Editing the site

- **Main text content**: edit `index.html`.
- **Visual design**: edit `styles.css`.
- **Tabs**: tab buttons and tab panels are in `index.html`; each button uses a matching `data-tab` / `data-panel` value.
- **Publications**: each publication is an `<li class="pub">` item in the Publications panel.
- **Expandable abstracts**: published items use a `.pub-title-button` with `aria-controls` pointing to a matching `.pub-abstract` block.
- **Open access badges**: use `.access-badge.oa` for open access and `.access-badge.closed` for non-open access. A closed-access example is included as an HTML comment in the Publications section.
- **Contact links**: edit the Contact panel in `index.html`.

## Updating the site later

After editing files locally:

```bash
git add index.html styles.css README.md
git commit -m "Update portfolio site"
git push
```

GitHub Pages will automatically redeploy the site after each push to `main`.

## Notes

- The site uses external web fonts loaded from Fontshare and Google Fonts.
- The light/dark theme toggle works in the browser only and does not store user data.
- The source is intentionally simple so it can be maintained without a web framework.
