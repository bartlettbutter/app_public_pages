---
layout: default
title: ETFWise
app_icon: /app_public_pages/support-url/etfwise/icon_ETFWise.png
app_description: "Support"
---

Welcome to the ETFWise support page. Below you'll find answers to common questions and ways to get help.

## Frequently Asked Questions

### How do the daily recommendations work?

ETFWise surfaces curated ETF recommendations across seven categories: Major Index, Sector, Bond & Fixed Income, International, Commodity, Thematic, and Dividend. When you tap "View Today's Picks," the app selects top ETFs per category and displays them on the main screen with full live data. Tap "See More" on any section to browse subcategories (e.g., Technology, Health Care, Energy within Sector). The recommended list is pinned once per day. Within that window, the list stays fixed and only live data (prices, sentiment) refreshes automatically every 5 minutes.

### Do I need an internet connection?

An internet connection is needed to fetch live prices, news, sentiment, prediction markets, and fund data. However, the on-device AI model runs entirely offline once downloaded, so no internet is required for AI-generated analysis.

### What is the Finnhub API key and do I need one?

Finnhub provides real-time ETF quotes, news, and analyst data. You can get a free API key at [finnhub.io](https://finnhub.io). Enter it on first launch to see live data. If you skip this step, the app runs with built-in demo data so you can still explore the interface.

### Where is my data stored?

All data, including recommendations, cached prices, sentiment scores, and AI-generated analysis, is stored locally on your device. Data is refreshed daily and never uploaded to external servers. Your Finnhub API key is stored securely on your device.

### What is the on-device AI model?

ETFWise includes a lightweight on-device language model that runs locally on your device. It generates bull cases, risk cases, and fund introductions using all on-screen metrics as context. The model may need to be downloaded on first launch.

### How do I download the AI model?

If the model isn't bundled with the app, you'll see a "Download Model" card on the main screen and in ETF detail views. Tap it to download. The download shows a progress bar and the model is saved to your device for future use.

### What are the seven ETF categories?

| Category | What It Covers |
|---|---|
| Major Index | S&P 500, Nasdaq 100, Russell 2000, Dow Jones, Total Market |
| Sector | Technology, Health Care, Energy, Financials, and more |
| Bond & Fixed Income | Government bonds, corporate bonds, high yield, TIPS, munis |
| International | Developed markets, emerging markets, single-country ETFs |
| Commodity | Gold, silver, oil, agriculture, broad commodity baskets |
| Thematic | AI & robotics, clean energy, cybersecurity, cloud, EVs |
| Dividend | High yield, dividend growth, aristocrats, income strategies |

### What data sources does ETFWise use?

| Provider | What It Provides |
|---|---|
| Finnhub | Real-time quotes, financial news, sentiment scoring, analyst recommendations |
| Yahoo Finance | AUM, expense ratios, top holdings, sector weights, fund performance, historical charts |
| Polymarket | Prediction market probabilities |
| On-Device AI | Bull cases, risk cases, and fund introductions |

### How does news sentiment work?

ETFWise fetches recent news articles (7-day window) for each ETF and scores them for positive or negative sentiment. The result is a score from -1.0 to +1.0, displayed as Bearish, Negative, Neutral, Positive, or Bullish. Up to 3 recent headlines are shown alongside the score.

### How do prediction markets work?

The app shows active prediction market events relevant to each ETF, with crowd-sourced probabilities, trading volume, and resolution dates. Not all ETFs will have matching events. The prediction markets section only appears when relevant events exist.

### How much does ETFWise cost?

ETFWise is available on the App Store. There are no subscriptions and no ads.

### Is my data private?

Yes. All data stays on your device. No personal data is collected or transmitted. See our full [Privacy Policy](https://bartlettbutter.github.io/app_public_pages/privacy-policies/etfwise/) for details.

## Troubleshooting

### Prices aren't loading

Make sure you've entered a valid Finnhub API key. You can get a free key at [finnhub.io](https://finnhub.io). Also check that your device is connected to the internet. If you skipped the API key step, the app shows demo data instead of live prices.

### The app shows "Unable to load ETF data"

This usually means the network request failed. Check your internet connection and try tapping "Retry." If you're using a Finnhub API key, verify it's correct in the app settings.

### Bull and risk cases aren't generating

The on-device AI model must be downloaded first. Look for the "Download Model" card on the main screen or in the ETF detail view. The model requires a one-time download.

### Fund data (holdings, performance) isn't loading

Top holdings, fund performance, and AUM data come from Yahoo Finance, which doesn't require an API key but does need an internet connection. If data fails to load, try closing and reopening the ETF detail view.

### The app is crashing

Please make sure you're running the latest version of ETFWise from the App Store. If the problem continues, try restarting your device.

## Compatibility

- iOS 18.0 or later
- iPhone

## Contact Us

If your question isn't answered here, please email us at [bartlettbutter@gmail.com](mailto:bartlettbutter@gmail.com) and we'll get back to you.
