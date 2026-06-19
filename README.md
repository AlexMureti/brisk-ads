# Brisk Credit — Web Screens & Ads

Self-contained, animated brand screens for the web (and office signage). Pure static HTML/CSS/JS + images — no build step, no dependencies.

## Pages
| File | What it is |
|------|------------|
| `index.html` | Launcher / landing page linking to each screen |
| `fathers-day.html` | Father's Day ad (auto-updating countdown to the 3rd Sunday of June) |
| `signage.html` | Evergreen office/branch signage screen |
| `og-card.png` | 1200×630 social share image for link previews |

Press **F** on any screen for fullscreen. They loop forever; fonts fall back to a system font if offline.

## Deploy to GitHub Pages

1. Create a new repo on GitHub named **`brisk-ads`** (public).
2. From this folder, push it up:
   ```bash
   git remote add origin https://github.com/YOURNAME/brisk-ads.git
   git branch -M main
   git push -u origin main
   ```
3. On GitHub: **Settings → Pages → Build and deployment → Source: "Deploy from a branch"**, branch **`main`**, folder **`/ (root)`**, then **Save**.
4. Your site goes live in ~1 minute at:
   `https://YOURNAME.github.io/brisk-ads/`

### One thing to update for nice link previews
The social-share (`og:`) tags in `index.html` and `fathers-day.html` contain a placeholder base URL `https://YOURNAME.github.io/brisk-ads/`. After you know your live URL, find-and-replace **`YOURNAME`** with your GitHub username (and adjust the repo name if you used a different one) so WhatsApp/Facebook/Twitter previews show the Father's Day card.

## Custom domain (optional)
To serve at e.g. `ads.brisk-credit.co.ke`, add a `CNAME` file containing that hostname and point a DNS CNAME record at `YOURNAME.github.io`.
