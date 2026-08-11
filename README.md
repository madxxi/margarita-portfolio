# margarita Diaz — Portfolio Site

Built with [Hugo](https://gohugo.io) + the [hugo-profile](https://github.com/gurusabarish/hugo-profile) theme.
Deploys automatically to GitHub Pages via GitHub Actions on every push to `main`.

## 1. Push this to GitHub

```bash
# From inside this folder
git add -A
git commit -m "Initial portfolio site"

# Create a new repo on GitHub named "margarita-portfolio" (or whatever you like),
# then:
git remote add origin https://github.com/YOUR-GITHUB-USERNAME/margarita-portfolio.git
git branch -M main
git push -u origin main
```

## 2. Turn on GitHub Pages

In the GitHub repo: **Settings → Pages → Build and deployment → Source → GitHub Actions**.
That's it — the included workflow (`.github/workflows/hugo.yml`) builds and deploys the
site automatically. Your site will be live at:

```
https://YOUR-GITHUB-USERNAME.github.io/margarita-portfolio/
```

## 3. Fill in the placeholders

Everything you need to edit lives in one file: **`hugo.yaml`**. Search for `YOUR-GITHUB-USERNAME`,
`[ADD:`, and `YOUR_EMAIL` and replace them:

- `baseURL` at the top — your actual GitHub Pages URL
- `hero.socialLinks` — your GitHub URL (LinkedIn is already filled in)
- `experience` — dates and the `[ADD: ...]` metrics/details for your Amadeus role;
  add earlier roles as additional `company` blocks (a commented-out example is included)
- `achievements` — swap in real certifications or metrics once you have exact numbers
- `projects` — once you push your sanitized PromQL library, Grafana dashboard exports,
  and runbook template as their own GitHub repos, update the `link`/`url` fields to point
  to them
- `contact.btnLink` — your real email

## 4. Add a resume PDF (optional but recommended)

Drop a PDF at `static/documents/margarita-diaz-resume.pdf` — the "Download Résumé" button
on the hero section already points there.

## 5. Swap the placeholder images (optional)

- `static/fav.png` — favicon
- `static/images/hero.svg` — hero illustration
- `static/images/me.png` — your photo for the About section
- `static/images/projects/*.png` — thumbnails for each project card (these are
  referenced in `hugo.yaml` but not included yet — add your own or remove the
  `image:` line for a project to hide it)

## Ongoing updates

This is the whole point of the git-based setup: whenever you want to update anything —
a new role, a new project, an updated metric — edit `hugo.yaml`, commit, and push.
GitHub Actions rebuilds and redeploys the site automatically within a minute or two.
No dashboard, no separate CMS login, no manual "publish" step.

## Local preview (optional)

If you ever want to preview changes before pushing, install Hugo locally
(`brew install hugo` on Mac, or see https://gohugo.io/installation/) and run:

```bash
hugo server -D
```


Then open http://localhost:1313/margarita-portfolio/
