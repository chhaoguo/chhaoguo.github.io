# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this is

Chenghao Guo's personal academic website, served via GitHub Pages at `https://chhaoguo.github.io/`. It is a single static HTML page — there is no build system, no package manager, no framework, and no test suite.

## Structure

- `index.html` — the entire site: markup, embedded `<style>` CSS, and a one-line inline `<script>`. All edits happen in this one file.
- `assets/Chenghao_Guo_CV.pdf`, `assets/Chenghao_Guo_PhD_Thesis.pdf` — downloadable documents linked from the page. Replace these files in place (keep the filenames) when the CV or thesis is updated.
- No CSS/JS files, no `node_modules`, no CI config.

## Working with this repo

- Edit `index.html` directly. There's nothing to install and nothing to build.
- To preview locally, just open `index.html` in a browser (or run a simple static server, e.g. `python3 -m http.server`).
- Styling uses CSS custom properties defined in `:root` at the top of the `<style>` block, with a `@media (prefers-color-scheme: dark)` override block for dark mode. When changing colors/spacing, edit the variables rather than hardcoding new values inline.
- The page is a single long scroll divided into `<section id="...">` blocks (`about`, `publications`, `thesis`, `service`, `contact`) linked from the `nav.tabs` anchor menu in the header — keep section `id`s and nav anchors in sync if renaming.
- Publications are listed as hand-written `<li>` entries in `.pub-list` (newest first), each with title, arXiv link, authors (self bolded via `.me` span), and venue. Follow the existing entry markup when adding a new paper.

## Deploying

Changes go live automatically via GitHub Pages once pushed to `main`:

```bash
git add .
git commit -m "Update site"
git push
```

No separate deploy/build step — GitHub Pages serves `index.html` from the repo root directly. See `README.md` for one-time repo/DNS setup details (already done).
