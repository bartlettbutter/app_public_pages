# App Public Pages

Public-facing pages for iOS apps, hosted on GitHub Pages. Each app has three page types: marketing, privacy policy, and support.

## Apps

### Barkpedia

Free dog breed identifier using on-device machine learning. Point your camera at any dog and get a breed match in seconds — no internet needed, no account required.

| | |
|---|---|
| **Price** | Free |
| **Platform** | iOS |
| **Privacy** | No data collection, no accounts, no analytics, no ads |
| **Offline** | Breed identification and favorites work offline |
| **Third-Party Services** | Dog CEO API, The Dog API, dogapi.dog, Wikipedia API |
| **Privacy Policy Date** | April 11, 2026 |

**Features:** Instant breed ID, breed details with photos and temperament, favorites, breed quiz, dog facts trivia.

**Pages:**
- [Marketing](https://bartlettbutter.github.io/app_public_pages/marketing-url/barkpedia/)
- [Privacy Policy](https://bartlettbutter.github.io/app_public_pages/privacy-policies/barkpedia/)
- [Support](https://bartlettbutter.github.io/app_public_pages/support-url/barkpedia/)

---

### ETFWise

Daily ETF recommendations with live market data, news sentiment, prediction markets, and on-device AI analysis across seven categories. No subscriptions, no ads.

| | |
|---|---|
| **Price** | Free (no subscriptions, no ads) |
| **Platform** | iOS |
| **Privacy** | No data collection, no accounts, no analytics, no ads |
| **Offline** | On-device AI runs offline once model is downloaded |
| **Third-Party Services** | Finnhub, Yahoo Finance, Polymarket, HuggingFace |
| **Privacy Policy Date** | April 25, 2026 |

**Features:** Daily picks across 7 categories (Major Index, Sector, Bond & Fixed Income, International, Commodity, Thematic, Dividend), 200+ ETFs, live prices refreshing every 5 minutes, news sentiment scoring, on-device AI bull/risk cases, prediction markets, analyst consensus, top holdings, fund performance, historical charts. Optional Finnhub API key for live data (sample data available without key).

**Pages:**
- [Marketing](https://bartlettbutter.github.io/app_public_pages/marketing-url/etfwise/)
- [Privacy Policy](https://bartlettbutter.github.io/app_public_pages/privacy-policies/etfwise/)
- [Support](https://bartlettbutter.github.io/app_public_pages/support-url/etfwise/)

---

### Journeyfolio

Trip planner with day-by-day itineraries, live weather forecasts, real-time flight tracking, and public holiday info. One-time purchase, no subscriptions.

| | |
|---|---|
| **Price** | One-time purchase |
| **Platform** | iOS |
| **Privacy** | No data collection, no accounts, no analytics, no ads |
| **Offline** | All trip data stored locally, accessible offline |
| **Third-Party Services** | Apple Weather, OpenWeatherMap (fallback), FlightAware AeroAPI, Nager.Date |
| **Privacy Policy Date** | April 12, 2026 |

**Features:** Day-by-day itineraries, live flight tracking, weather forecasts (Apple Weather with OpenWeatherMap fallback), hotel and accommodation details, public holidays for destinations, works offline.

**Pages:**
- [Marketing](https://bartlettbutter.github.io/app_public_pages/marketing-url/journeyfolio/)
- [Privacy Policy](https://bartlettbutter.github.io/app_public_pages/privacy-policies/journeyfolio/)
- [Support](https://bartlettbutter.github.io/app_public_pages/support-url/journeyfolio/)

---

### Nekopedia

Free cat breed identifier using on-device machine learning. Point your camera at any cat and get a breed match in seconds — no internet needed, no account required.

| | |
|---|---|
| **Price** | Free |
| **Platform** | iOS |
| **Privacy** | No data collection, no accounts, no analytics, no ads |
| **Offline** | Breed identification and favorites work offline |
| **Third-Party Services** | The Cat API, catfact.ninja |
| **Privacy Policy Date** | April 22, 2026 |

**Features:** Instant breed ID, breed details with photos and temperament, favorites, breed quiz, cat trivia with reward titles.

**Pages:**
- [Marketing](https://bartlettbutter.github.io/app_public_pages/marketing-url/nekopedia/)
- [Privacy Policy](https://bartlettbutter.github.io/app_public_pages/privacy-policies/nekopedia/)
- [Support](https://bartlettbutter.github.io/app_public_pages/support-url/nekopedia/)

---

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

### Page Content Conventions

- **Marketing pages** — Start with an `h1` tagline (auto-centered by CSS). The header provides app identity; the `h1` provides the marketing hook.
- **Privacy policy pages** — Start with the effective date in bold. No `h1` needed since the header shows "App Name / Privacy Policy".
- **Support pages** — Start with a welcome sentence. No `h1` needed since the header shows "App Name / Support".

## Live URLs

Pages are served at:
```
https://bartlettbutter.github.io/app_public_pages/{page-type}/{app-name}/
```

## Local Preview

```bash
jekyll serve
```

Then open http://localhost:4000/app_public_pages/.

## Adding a New App

1. Create folders: `marketing-url/<app>/`, `privacy-policies/<app>/`, `support-url/<app>/`
2. Add `index.md` to each with front matter (`layout`, `title`, `app_icon`, `app_description`)
3. Write the page content in Markdown (follow conventions above)
4. Place the app icon as `icon_<AppName>.png` in each folder
