# brisk-ads

Office-screen loops and web brand screens for Brisk Credit, a Kenyan lender. Each page is a self-contained HTML file meant to run full-screen on a branch TV or in a browser: a staff-learning broadcast, product and seasonal ads, an animated branch map, and a pre-rendered video loop with a date-switched campaign cut.

## Live

https://alexmureti.github.io/brisk-ads/ — the index links to every screen. Press F on any screen for fullscreen.

## Stack

- Static HTML, CSS and vanilla JavaScript. No framework, no build step, no package manager.
- GSAP 3.14.2, vendored, drives the timeline loops (`branches.html`, `brisk-live-animated.html`); the Kenya outline and branch coordinates are data in `branches/map.js`.
- Canvas 2D and SVG for ambient animation; HTML5 video for the rendered loop.
- Manrope and Playfair Display from Google Fonts; Geist self-hosted.
- Hosted on GitHub Pages (`.nojekyll`).

## Run locally

There is no package.json and nothing to build. Open `index.html` in a browser, or serve the folder with any static file server. `brisk-live.html` polls `brisk-live/version.json` every 15 minutes to swap its video in place; that fetch needs the folder served over HTTP, not opened from disk.

## Status

Live and maintained; last push 12 October 2026. Three older pages (`partner`, `kilimo`, `fathers-day`) still carry a placeholder base URL in their social-share tags.
