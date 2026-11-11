# ASA BIOP Dynamic Borrowing Working Group: Website Prototype

Quarto website deployed to GitHub Pages via GitHub Actions.

## Deploy (one-time)

1. **Create the repo** on GitHub (e.g., `asa-dynamic-borrowing-wg`), empty, no README. Pages on a free plan requires a **public** repo.
2. **Edit `_quarto.yml`**: replace `YOUR-ORG` in the GitHub link with your user/org name.
3. **Push the files** from this folder:

   ```bash
   git init -b main
   git add .
   git commit -m "Initial site prototype"
   git remote add origin https://github.com/YOUR-ORG/asa-dynamic-borrowing-wg.git
   git push -u origin main
   ```

4. **Enable Pages**: repo **Settings → Pages → Build and deployment → Source: GitHub Actions**.
5. Go to the **Actions** tab. The "Publish site" workflow runs on each push to `main` (re-run it if the first run happened before step 4). When it finishes, the site is at `https://YOUR-ORG.github.io/asa-dynamic-borrowing-wg/`.

## Preview locally (optional)

Install [Quarto](https://quarto.org/docs/get-started/), then:

```bash
quarto preview
```

## Editing content

- Pages are `.qmd` (Markdown) files: `index`, `members`, `meetings`, `resources`.
- Meeting notes go in `meetings/`; documents go in `docs/` (PDFs and zips are copied to the site).
- Commit and push to `main` and the site rebuilds in about a minute.
- Members can propose edits through pull requests.

## Notes

- Everything in a public repo and its Pages site is visible to anyone. Keep confidential material in a separate private repo.
- Sites are served from `github.io` by default; a custom domain can be set under Settings → Pages.
