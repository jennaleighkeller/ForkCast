# Healthy & Easy Recipes — Meal Planner

A single-file, no-build static site: pick recipes, get a combined shopping
list, plan your week, and export it as an image. All data (recipes, kitchen
items, weekly plan) is saved in the visitor's own browser via `localStorage`
— nothing is sent to a server.

## Deploy to GitHub Pages (free hosting)

1. Create a new **public** repository on GitHub (e.g. `meal-planner`).
2. Upload `index.html` to the root of that repository (drag-and-drop on
   GitHub's web UI works fine, or `git add / commit / push`).
3. In the repo, go to **Settings → Pages**.
4. Under "Build and deployment", set **Source** to `Deploy from a branch`,
   branch `main`, folder `/ (root)`, then **Save**.
5. GitHub will give you a URL like:
   `https://YOUR-USERNAME.github.io/meal-planner/`
   It can take a minute or two to go live the first time.

That's it — no build step, no dependencies to install. The only external
resource is the `html2canvas` library, which loads automatically from a CDN
the first time someone clicks "Export as image."

## Notes

- Data is stored per browser (`localStorage`), not per account — clearing
  browser data or switching devices/browsers will start fresh.
- Works fully offline after the first load, except image export (needs the
  CDN once) and if you're loading Google/system fonts.
