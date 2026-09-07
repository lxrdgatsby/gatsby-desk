# Gatsby Desk

Dark luxury command center for Path A. Live GitHub Pages site, not a file dump.

## Live URL

https://lxrdgatsby.github.io/gatsby-desk/

Open that URL in Safari (phone) or any browser (desktop). JavaScript must run: the clock ticks, the ridge/chord draw, and numbers fill from `desk.json`. Do not use htmlpreview, jsDelivr, or raw.githubusercontent.com as the site.

## Add to Home Screen (Safari only)

1. Open https://lxrdgatsby.github.io/gatsby-desk/ in Safari on iPhone.
2. Tap Share.
3. Tap Add to Home Screen.
4. Tap Add.

## Public contract (`desk.json` is the account bus)

This static site never calls Robinhood from the browser.

Writers (push a new `desk.json` to `main`):

- Grok chat, on demand
- Existing hourly automation **Gatsby Desk refresh**

Readers:

- This Pages site fetches `./desk.json?t=<epoch>` every 30 seconds
- After each GitHub Actions deploy, the new file is live on the same origin

Binance SOLUSDT is polled every 15 seconds for last price display only. Robinhood bid / ask / mark in `desk.json` stay the source of truth for the gate.

### How fills show up

Write `desk.json` with `order.filled > 0` or `order.state` closed with a position. On the next 30s poll (or the next Actions deploy):

- Gate text becomes **FILLED**
- Crew hot outline moves to **HELSINKI**
- A HELS log line is appended
- Sparkline steps to the new equity

Flatten or a dead order (`cancelled` / `rejected` / gate DEAD or FLAT):

- Gate text **DEAD** or **FLAT**
- Crew hot outline moves to **BERLIN**

While resting, Palermo stays hot and the red pin marks the reserved working order.

Human confirm for ASTRA preview/place happens in Grok, not in this page. There is no trade button.

## Turn Pages on

If a deploy is waiting:

Settings -> Pages -> Source -> GitHub Actions

Later pushes to `main` auto-deploy.
