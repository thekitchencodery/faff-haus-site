# FAFF.haus site

Static, single-page landing site. Built to be lightweight, accessible, and easy to deploy to Cloudflare Pages.

## Preview
- Live: https://faff.haus (update if different)
- Screenshot/Preview: see /src/favicon-512x512.png for brand accent; add a full-page screenshot at docs/preview.png if available.

## Files
- `src/index.html` — the site
- `src/favicon.ico` — favicon
- `src/favicon-16x16.png`, `src/favicon-32x32.png`, `src/favicon-48x48.png`, `src/favicon-64x64.png`, `src/favicon-128x128.png`, `src/favicon-180x180.png`, `src/favicon-256x256.png`, `src/favicon-512x512.png` — icons
- `src/manifest.json` — PWA manifest

## Switch out the favicon
```chatgpt
> Create a favicon bundle. It should look like an element symbol using the letters "FAFF" in a 2x2 grid black on white. Do not include a border. Use a font like 'Helvetica Neue'.
```

## Live reload
```bash
# First time
python3 -m venv .venv
source .venv/bin/activate
pip install livereload
livereload ./public --host 127.0.0.1 --port 5500
deactivate

# Next time
source .venv/bin/activate
livereload ./public   --host 127.0.0.1 --port 5500
deactivate
```

## Deploy (Cloudflare Pages)
- Connect repo (Framework: None, Build: blank, Output: `/src`), or
- Use Wrangler:
  ```bash
  npm i -g wrangler
  wrangler pages publish ./src --project-name=faff-haus
  ```
