# Developer website (GitHub Pages)

Contents of this folder are published as the OmniShift Studios developer site at
**https://omnishiftstudios.github.io** (user-site repo `omnishiftstudios/omnishiftstudios.github.io`, branch `main`).

Why it exists: AdMob requires `https://<developer-website-root>/app-ads.txt` to
authorise ad sellers. The Play listing's "Website" field must point at this domain.

- `app-ads.txt` — AdMob publisher authorisation (`pub-2017450468818575`). Must stay at the site root.
- `index.html` — landing page (Play link, privacy policy, contact).
- `sort-spectrum/privacy.html` — copy of `../privacy-policy.html`.

## Publishing changes

```bash
git clone git@github.com:omnishiftstudios/omnishiftstudios.github.io.git /tmp/site
cp -r store-assets/site/. /tmp/site/ && cd /tmp/site && git add -A && git commit -m "Update site" && git push
```

After changing `app-ads.txt`: AdMob → Apps → app-ads.txt → "Check for updates" (crawl takes up to 24 h).
