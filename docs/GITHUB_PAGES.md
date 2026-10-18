# Publish your academic website on GitHub Pages

These instructions publish the prepared local website at **https://alirezaak2000.github.io/** using your documented GitHub username, **AlirezaAK2000**.

## 1. Create an empty website repository

Sign in to [GitHub](https://github.com/new) as `AlirezaAK2000` and create a repository:

- Name: **AlirezaAK2000.github.io**
- Visibility: **Public** (supports GitHub Pages on GitHub Free)
- Leave README, .gitignore, and license initialization unchecked: those files already exist locally.

If that repository already exists, inspect it before proceeding. Do not overwrite its content or force-push. Integrate this checkout with the existing website instead.

## 2. Point this checkout at your repository

Run these commands in Terminal. The website has its own Git checkout inside the positions workspace; run these from `website/`, not the parent repository.

```sh
cd /Users/alirezaak/Documents/positions/website
git remote -v
git remote rename origin upstream
git remote add origin https://github.com/AlirezaAK2000/AlirezaAK2000.github.io.git
git branch -M main
git add .
git commit -m "Personalize academic website for Alireza Akhoundi"
git push -u origin main
```

The `remote rename` command preserves the original al-folio source as `upstream`. Run it once. If you already ran these steps, use `git remote -v` to inspect the remotes before adding them again. Authenticate with GitHub's credential manager or a personal access token when prompted; an account password cannot authenticate HTTPS Git pushes.

## 3. Enable GitHub Pages

In the new repository, open **Settings → Pages**. Under **Build and deployment → Source**, choose **GitHub Actions**.

Then open **Actions → Deploy academic website → Run workflow**, select `main`, and run it. This manually retries the first build if the initial push happened before Pages was enabled. If Actions are disabled for the repository, enable them first.

The supplied `.github/workflows/deploy.yml` builds Jekyll, uploads `_site`, and deploys it using the official Pages actions. No separate `gh-pages` branch or custom deployment secret is required. Do not replace this with the basic branch-based Jekyll builder: al-folio uses additional plugins.

## 4. Open your website

Wait for both the **build** and **deploy** jobs to turn green. Visit:

**https://alirezaak2000.github.io/**

GitHub notes that publication can take up to ten minutes. The intended URL above is not a claim that the site has already been deployed.

The prepared `_config.yml` uses:

```yaml
url: https://alirezaak2000.github.io
baseurl: ""
```

The empty `baseurl` is correct for this user website. No custom domain or `CNAME` file is needed. If you use another GitHub account, change the repository name, `url`, and any absolute project links in `_data/cv.yml` to match it.

## 5. Update the website

Edit your Markdown pages or `_data/cv.yml`, preview locally if desired, then:

```sh
cd /Users/alirezaak/Documents/positions/website
git add .
git commit -m "Update academic website"
git push
```

Each push to `main` automatically rebuilds and republishes the website. To add published work later, update `_pages/research.md`; the empty `_bibliography/papers.bib` is available if you choose to enable bibliography-based publication listings.

## Troubleshooting

- **Build fails:** open the failed Actions job and inspect the first error. Ruby and all pinned dependencies are installed by the workflow.
- **Deploy fails or Pages reports not enabled:** confirm Settings → Pages → Source is GitHub Actions, then rerun the workflow.
- **404 immediately after deployment:** allow a few minutes, verify the repository name matches the account, and check Settings → Pages for the published URL.
- **Styles missing:** confirm `baseurl: ""`, `url` matches the account, and the latest build succeeded.
- **Push rejected:** confirm the remote URL and whether the repository already contains commits. Do not force-push over an existing website.

Official references: [GitHub Pages quickstart](https://docs.github.com/en/pages/quickstart), [custom Pages workflows](https://docs.github.com/en/pages/getting-started-with-github-pages/using-custom-workflows-with-github-pages), and [al-folio documentation](https://github.com/alshedivat/al-folio).
