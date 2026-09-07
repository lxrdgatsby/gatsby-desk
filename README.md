# Gatsby Desk

Dark mobile dashboard for Path A.

## Live URL

https://lxrdgatsby.github.io/gatsby-desk/

Open that URL in Safari. It is a real GitHub Pages site that runs JavaScript (clock ticks, numbers fill). Do not use htmlpreview, jsDelivr, or raw.githubusercontent.com as the site.

## Add to Home Screen (Safari only)

1. Open https://lxrdgatsby.github.io/gatsby-desk/ in Safari on iPhone.
2. Tap the Share button.
3. Tap Add to Home Screen.
4. Tap Add.

Safari only. Other browsers and downloaded HTML files are not the home-screen app.

## Hourly restamp

A Grok Automation named **Gatsby Desk refresh** already exists. Each hour it rewrites `desk.json` on `main` (balance, P/L, SOL book, order state, log). This Pages site fetches `./desk.json` from the same origin every 60 seconds, so the phone updates without a file download.

Binance SOL last is polled every 15 seconds for the mark. Robinhood bid/ask stay on the values from `desk.json`.

## Turn Pages on

If the first deploy is waiting:

Settings -> Pages -> Source -> GitHub Actions

If Actions cannot flip the source, the same click on branch `main` / root also publishes. Later pushes to `main` auto-deploy.

Do not download HTML. Do not use htmlpreview.github.io.
