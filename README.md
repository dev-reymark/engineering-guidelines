# Engineering Guidelines — GitHub Pages Project

This repository publishes the **Software Project Engineering & AI-Agent Development Standard v1.1** as a browsable documentation website while preserving Markdown as the source of truth.

## How it works

- `index.html` is a static documentation shell.
- `content/` contains the complete v4.1 engineering scaffold.
- `nav.json` defines documentation navigation.
- Markdown is rendered in the browser with **Marked**.
- Rendered HTML is sanitized with **DOMPurify**.
- No build step is required.

## Local preview

Because browsers restrict `fetch()` from `file://`, serve the directory locally.

Python:

```bash
python -m http.server 8000
```

Then open `http://localhost:8000`.

## Publish with GitHub Pages

1. Create a GitHub repository.
2. Copy this project's contents to the repository root.
3. Commit and push.
4. In GitHub, open **Settings → Pages**.
5. Under **Build and deployment**, choose **Deploy from a branch**.
6. Select your default branch and `/ (root)`.
7. Save.

GitHub Pages will publish `index.html`.

## Editing guidelines

Edit the Markdown files under `content/`.

If you add or rename Markdown files, also update `nav.json` so they appear in navigation.

## Using the scaffold in a software project

The website is the human-readable guideline reference. The reusable scaffold itself is the complete directory tree under `content/`.

For a new project, copy the applicable scaffold files from `content/` into the project repository root. Preserve `AGENTS.md`, `docs/`, and `.agents/` so coding agents can follow the standard.

## Dependency note

The site loads Marked and DOMPurify from jsDelivr at runtime. If you require a fully offline/self-hosted site, vendor those libraries into the repository and update `index.html`.

## Version

Engineering Standard: **1.1**  
Scaffold: **v4.1**
