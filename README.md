# Physical AI — group website (GitHub Pages)

Static site files for the **Physical AI** research group at the University of Melbourne.

## Expected live URL

After setup, the site should be available at:

**https://uom-physical-ai.github.io/**

That uses the special repository name `uom-physical-ai.github.io` under the organisation [uom-physical-ai](https://github.com/uom-physical-ai).

## One-time GitHub setup (organisation owner)

1. On GitHub, create a **new public** repository in the `uom-physical-ai` organisation named exactly **`uom-physical-ai.github.io`** (leave “Add a README” unchecked if you will push this folder’s contents from git).
2. Open the repository → **Settings** → **Pages**.
3. Under **Build and deployment**, set **Source** to **Deploy from a branch**, branch **`main`**, folder **`/ (root)`**, then save.

## Publish this folder

From this directory:

```bash
git init
git add index.html styles.css .nojekyll README.md
git commit -m "Add Physical AI group site"
git branch -M main
git remote add origin https://github.com/uom-physical-ai/uom-physical-ai.github.io.git
git push -u origin main
```

If the remote already has commits (for example a README created on the web), use `git pull origin main --rebase` before pushing, or follow GitHub’s instructions to merge.

## Alternative: project site

If you prefer a repository name such as `physical-ai`, the Pages URL becomes **https://uom-physical-ai.github.io/physical-ai/** and you may need to set `base` paths for assets or use relative URLs as in this template (root-relative `styles.css` is fine for that layout when the site is served from the repo root).

## Local preview

Open `index.html` in a browser, or run a static server, for example:

```bash
python3 -m http.server 8080
```

Then visit `http://127.0.0.1:8080`.
