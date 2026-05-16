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
├── _config.yml                  # Root Jekyll config (placeholder, not used directly)
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
- `_config.yml` — Jekyll site configuration (title, description, icon, URL)
- `index.md` — Page content in Markdown
- `icon_<AppName>.png` — App icon displayed in the page header

## Layout System

All pages share a single layout at `_layouts/default.html`. The layout reads configuration from each sub-site's `_config.yml`:

| Config Field | Purpose |
|---|---|
| `title` | App name — shown in the page header and browser tab |
| `description` | Tagline (marketing) or page type label (privacy/support) — shown below the icon |
| `icon` | Filename of the app icon PNG — displayed as an 80×80 rounded image in the header |
| `url` | Canonical URL for the page on GitHub Pages |

### Conditional Icon Header

The icon header section only renders when `site.icon` is defined in `_config.yml`. If omitted, the page renders content directly without the branded header.

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

Run any sub-site locally with Jekyll:

```bash
jekyll serve -s marketing-url/barkpedia --layouts-path _layouts
```

Then open http://localhost:4000. Use `--port <number>` to run multiple pages simultaneously.

## Adding a New App

1. Create folders: `marketing-url/<app>/`, `privacy-policies/<app>/`, `support-url/<app>/`
2. Add `_config.yml` to each with `title`, `description`, `url`, and `icon` fields
3. Add `index.md` with the page content (follow conventions above)
4. Place the app icon as `icon_<AppName>.png` in each folder
