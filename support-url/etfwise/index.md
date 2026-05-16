---
layout: default
title: ETFWise
app_icon: /app_public_pages/support-url/etfwise/icon_ETFWise.png
app_description: "Support"
---

Welcome to the ETFWise support page. Below you'll find answers to common questions and ways to get help.

## Frequently Asked Questions

### How do the daily recommendations work?

ETFWise surfaces curated ETF recommendations across seven categories: Major Index, Sector, Bond & Fixed Income, International, Commodity, Thematic, and Dividend. When you tap "View Today's Picks," the app first ranks all 200+ catalog ETFs by Assets Under Management (AUM) to determine which ones to show. The top 3 per section appear on the main screen with full live data. Tap "See More" on any section to browse subcategories (e.g., Technology, Health Care, Energy within Sector). The recommended list is pinned once per "recommendation day," which runs from 5:00 AM to 4:59 AM the next day. Within that window, the list stays fixed — only live data (prices, AUM, sentiment) refreshes automatically every 5 minutes.

### Do I need an internet connection?

An internet connection is needed to fetch live prices, news, sentiment, prediction markets, and fund data. However, the on-device AI model (Gemma 3 270M) runs entirely offline once downloaded — no internet required for bull and risk case generation.

### What is the Finnhub API key and do I need one?

Finnhub provides real-time ETF quotes, news, and analyst data. You can get a free API key at [finnhub.io](https://finnhub.io). Enter it on first launch to see live data. If you skip this step, the app runs with built-in mock data so you can still explore the interface.

### Where is my data stored?

All data — recommendations, cached prices, sentiment scores, AI-generated analysis — is stored in the app's memory on your device. Data is refreshed daily and never uploaded to external servers. Your Finnhub API key is stored securely in the iOS Keychain.

### What is the on-device AI model?

ETFWise includes Google's Gemma 3 270M model (~290 MB, Q8_0 quantization), which runs locally via llama.cpp. It generates bull cases, risk cases, and fund introductions using all on-screen metrics as context. The model can be downloaded from HuggingFace on first launch or bundled with the app.

### How do I download the Gemma model?

If the model isn't bundled with the app, you'll see a "Download Model" card on the main screen and in ETF detail views. Tap it to download (~290 MB) from HuggingFace. The download shows a progress bar and the model is saved to your device for future use.

### What are the seven ETF categories?

| Category | What It Covers |
|---|---|
| Major Index | S&P 500, Nasdaq 100, Russell 2000, Dow Jones, Total Market |
| Sector | Technology, Health Care, Energy, Financials, and all 11 GICS sectors |
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
| Polymarket | Prediction market probabilities from the Finance section |
| Gemma 3 270M | On-device AI for bull cases, risk cases, and fund introductions |

### How does news sentiment work?

ETFWise fetches recent news articles (7-day window) from Finnhub for each ETF and scores them using keyword-based sentiment analysis (~100 financial keywords). The result is a score from -1.0 to +1.0, displayed as Bearish, Negative, Neutral, Positive, or Bullish. Up to 3 recent headlines are shown alongside the score.

### How do prediction markets work?

The app fetches active prediction market events from Polymarket's Finance section and matches them to ETF categories using keyword-based filtering. Each ETF detail view shows the most relevant events with crowd-sourced probabilities, trading volume, and resolution dates.

### How much does ETFWise cost?

ETFWise is available on the App Store. There are no subscriptions and no ads.

## Troubleshooting

### Prices aren't loading

Make sure you've entered a valid Finnhub API key. You can get a free key at [finnhub.io](https://finnhub.io). Also check that your device is connected to the internet. If you skipped the API key step, the app shows mock data instead of live prices.

### The app shows "Unable to load ETF data"

This usually means the network request failed. Check your internet connection and try tapping "Retry." If you're using a Finnhub API key, verify it's correct in the app settings.

### Bull and risk cases aren't generating

The on-device Gemma model must be downloaded first. Look for the "Download Model" card on the main screen or in the ETF detail view. The model is ~290 MB and requires a one-time download.

### Fund data (holdings, performance) isn't loading

Top holdings, fund performance, and AUM data come from Yahoo Finance, which doesn't require an API key but does need an internet connection. If data fails to load, try closing and reopening the ETF detail view.

### The app is crashing

Please make sure you're running the latest version of ETFWise from the App Store. If the problem continues, try restarting your device.

## Contact Us

If your question isn't answered here, please email us at [bartlettbutter@gmail.com](mailto:bartlettbutter@gmail.com) and we'll get back to you.
