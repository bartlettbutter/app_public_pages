# App Public Pages

Public-facing pages for iOS apps, hosted on GitHub Pages. Each app has three page types: marketing, privacy policy, and support.

## Apps

| App | Description |
|-----|-------------|
| **Barkpedia** | Free dog breed identifier using on-device ML |
| **ETFWise** | Daily ETF recommendations with live data and on-device AI |
| **Journeyfolio** | Trip planner with live weather and flight tracking |
| **Nekopedia** | Free cat breed identifier using on-device ML |

## Repository Structure

```
app_public_pages/
├── _config.yml                  # Root Jekyll config (GitHub Pages reads only this one)
├── _layouts/
│   └── default.html             # Shared layout for all pages
├── marketing-url/
│   ├── barkpedia/               # Marketing landing page
│   ├── etfwise/
│   ├── journeyfolio/
│   └── nekopedia/
├── privacy-policies/
│   ├── barkpedia/               # Privacy policy page
│   ├── etfwise/
│   ├── journeyfolio/
│   └── nekopedia/
└── support-url/
    ├── barkpedia/               # Support / FAQ page
    ├── etfwise/
    ├── journeyfolio/
    └── nekopedia/
```

Each app folder contains:
- `index.md` — Page content in Markdown with YAML front matter
- `icon_<AppName>.png` — App icon displayed in the page header

## How It Works

This is a single GitHub Pages site built from the root `_config.yml`. Each `index.md` uses YAML front matter to specify its layout and page-specific variables:

```yaml
---
layout: default
title: Barkpedia
app_icon: /app_public_pages/marketing-url/barkpedia/icon_Barkpedia.png
app_description: "Identify any dog breed instantly from a photo."
---
```

### Front Matter Fields

| Field | Purpose |
|---|---|
| `layout` | Always `default` — references `_layouts/default.html` |
| `title` | App name — shown in the page header and browser tab |
| `app_icon` | Absolute path to the icon PNG — displayed as an 80×80 rounded image |
| `app_description` | Tagline (marketing) or page type label (privacy/support) — shown below the icon |

### Conditional Icon Header

The icon header section only renders when `app_icon` is defined in front matter. If omitted, the page renders content directly without the branded header.

### Page Content Conventions

- **Marketing pages** — Start with an `h1` tagline (auto-centered by CSS). The header provides app identity; the `h1` provides the marketing hook.
- **Privacy policy pages** — Start with the effective date in bold. No `h1` needed since the header shows "App Name / Privacy Policy".
- **Support pages** — Start with a welcome sentence. No `h1` needed since the header shows "App Name / Support".

## Live URLs

Pages are served at:
```
https://bartlettbutter.github.io/app_public_pages/{page-type}/{app-name}/
```

For example:
- https://bartlettbutter.github.io/app_public_pages/marketing-url/barkpedia/
- https://bartlettbutter.github.io/app_public_pages/privacy-policies/etfwise/
- https://bartlettbutter.github.io/app_public_pages/support-url/journeyfolio/

## Local Preview

```bash
# From the repo root — serves the entire site
jekyll serve
```

Then open http://localhost:4000/app_public_pages/.

## Adding a New App

1. Create folders: `marketing-url/<app>/`, `privacy-policies/<app>/`, `support-url/<app>/`
2. Add `index.md` to each with front matter (`layout`, `title`, `app_icon`, `app_description`)
3. Write the page content in Markdown (follow conventions above)
4. Place the app icon as `icon_<AppName>.png` in each folder
