# chhaoguo.github.io

Personal academic website for Chenghao Guo, built as a single static page
(`index.html`) with the CV and PhD thesis stored under `assets/`.

## One-time setup

1. Create the new GitHub account with username **`chhaoguo`** (if you haven't
   already), and sign in as that account.

2. Create a new **public** repository on that account named exactly:
   `chhaoguo.github.io`
   (a repo with this exact name — `<username>.github.io` — is automatically
   served at `https://chhaoguo.github.io/`, no extra config needed).

## Deploy

From this folder:

```bash
cd chhaoguo.github.io
git init
git add .
git commit -m "Initial personal website"
git branch -M main
git remote add origin https://github.com/chhaoguo/chhaoguo.github.io.git
git push -u origin main
```

If prompted for credentials, use a GitHub personal access token (not your
password) — GitHub no longer accepts account passwords for git operations.

In the repo on GitHub, go to **Settings → Pages** and confirm the source is
set to `Deploy from a branch`, branch `main`, folder `/ (root)` (usually
already the default for a `<username>.github.io` repo).

Wait 1–2 minutes, then visit `https://chhaoguo.github.io/`.

## Updating later

Edit `index.html`, then:

```bash
git add .
git commit -m "Update site"
git push
```

Changes go live within a minute or two.

## Custom domain (optional)

If you buy a domain later: add a file named `CNAME` to this folder containing
just the domain (e.g. `chenghaoguo.com`), point the domain's DNS at GitHub
Pages per [GitHub's docs](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site),
and set the custom domain in **Settings → Pages**.
