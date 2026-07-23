# home — gijo-mathew projects homepage

A single static `index.html` — a directory of all my projects (Yankees Legends Challenge, Kinfolk, Jonah's Train Town) with live thumbnails. No build step, no frameworks.

**Live:** https://mathew-gijo.github.io/home/

## Run locally

Open `index.html` in a browser, or serve it:

```bash
npx serve .
```

## Adding a project

1. Drop a screenshot into `thumbs/` (landscape ~1200px wide works best; portrait phone shots also work — the card crops from the top).
2. Copy one of the `<article class="card">` blocks in `index.html` and edit the image, emoji, title, description, tags, and links.
3. Commit and push — GitHub Pages redeploys automatically.

## Refreshing a thumbnail

Headless Chrome one-liner:

```bash
"/Applications/Google Chrome.app/Contents/MacOS/Google Chrome" --headless=new \
  --screenshot=thumbs/name.png --window-size=1280,800 --hide-scrollbars "https://the-app-url"
```

(For apps with a loading screen, take the screenshot with a delay via puppeteer-core.)
