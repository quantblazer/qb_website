# Quant Blazer Website — Plan

## Goal
A public site for Quant Blazer that presents three pieces of work and how they fit together:

1. **IQFeed Downloader** — back-adjusted continuous futures, hourly and daily CSVs.
2. **Kraken Downloader** — daily OHLCV for every USD crypto pair on Kraken.
3. **Real Test Pilot** — desktop app and service that runs RealTest scripts on a schedule: daily backtests
   for monitored strategies, order files for live ones.

## Folder layout
```
index.html
styles.css
assets/logo.png   transparent, cropped logo (455x566, solid navy #0F2738)
PLAN.md           this file
```

This is the first design (previously kept in a `v1` subfolder). Two later drafts, v2 and v3, were
dropped on 2026-10-01 and the chosen version was moved to the root.

## What is built
**Stack:** plain HTML and CSS. No JavaScript, no build step, no dependencies. Open `index.html` in a
browser, or serve the folder from any static host (GitHub Pages, Netlify, Cloudflare Pages).

**Design:** colours taken from the logo (navy ink on warm paper, one rust accent), system fonts, light
theme only. Responsive down to phone width.

**Page sections, in order:**

| Section | Content |
|---|---|
| Header | Wordmark and anchor links to each section (sticky) |
| Hero | Headline, one-paragraph summary, logo |
| How it fits | Diagram: market data on disk → Real Test Pilot → reports and order files. States that Pilot does not download data or send orders |
| IQFeed Downloader | What it does, four key points (full refresh, shrink guard, atomic writes, unattended runs), markets covered, example commands and CSV output, GitHub link |
| Kraken Downloader | What it does, four key points (two sources, delisted pairs, exact values, verify), example commands and CSV output, GitHub link |
| Real Test Pilot | Five steps (import, refresh, run, report, deliver), how it works, status list with Built / Possible labels |
| Footer | Copyright and "not investment advice" line |

**Source of the content:** the README and PLAN files of the three projects. The site only claims
what those files say is built. Checked against the Real Test Pilot plan on 2026-10-10 (replanned 2026-10-07): Pilot now only
schedules RealTest backtests and orders runs and delivers the results. Data download and broker
execution were removed from it, so the site no longer shows them. All five parts of its status list
are shown as built; three of its "possible next steps" are shown as "possible".

## Open items
- **GitHub links.** `github.com/quantblazer/iqfeed_download` and `github.com/quantblazer/kraken_download`
  are public (checked 2026-10-01) and the page links to them. Real Test Pilot has no public repo, so
  it has no link.
- **Contact.** No email, Substack or social links yet. Add them to the footer once decided.
- **Domain and hosting.** Not chosen. The repo is `github.com/quantblazer/qb_website`; GitHub Pages
  would serve it as is.
- **Screenshots.** Real Test Pilot would benefit from a screenshot of the Dashboard or Data screen.
- **Logo.** A true SVG would scale better than the current PNG.

## Ideas for later
- Separate page per project with fuller documentation.
- Writing section linked to the Substack, once there is a URL.
- Dark theme, once there is a light-coloured logo. The current mark is navy on transparency.
- Update the Real Test Pilot roadmap as phases are completed.
