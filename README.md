# Interactive PyTorch Guide

A responsive, single-page learning hub covering PyTorch foundations, architectures, transfer learning strategy, engineering practices, and mastery. Built with semantic HTML, Tailwind via CDN, and Chart.js. Ready for GitHub Pages.

- Live URL (after publish): `https://ashwani65.github.io/interactive-pytorch-guide/`
- Entry point: `index.html`

## Highlights
- Responsive layout with mobile drawer navigation
- Sectioned content: Foundations, Vision, Architectures, Strategy, Engineering, Mastery, Advanced, Pro Toolkit
- Chart.js comparison chart (Experiment Tracking tools)
- SEO meta tags and favicon
- GitHub Pages friendly: `.nojekyll` and `404.html` included

## Local Development
You can open `index.html` directly, but a tiny static server is recommended for consistent behavior:

```bash
# Python 3
python3 -m http.server 5500
# then open http://127.0.0.1:5500/
```

Or use VS Code “Live Server”.

## Deploy to GitHub Pages
Choose one approach.

### Option A — Personal site repo
If you use `ashwani65.github.io`:
```bash
# from personal site repo
rsync -a --delete /Users/ashwanisingh/Documents/github/interactive-pytorch-guide/ ./interactive-pytorch-guide/
git add .
git commit -m "Add interactive-pytorch-guide"
git push
```
Then in GitHub → Settings → Pages: Source = Deploy from branch (main), root.

URL: `https://ashwani65.github.io/interactive-pytorch-guide/`

### Option B — Dedicated project repo
```bash
cd /Users/ashwanisingh/Documents/github/interactive-pytorch-guide
git init -b main
git add .
git commit -m "Initial commit: interactive PyTorch guide"
git remote add origin git@github.com:ashwani65/interactive-pytorch-guide.git
git push -u origin main
```
Then in GitHub → Settings → Pages: Source = Deploy from branch (main), root.

## Optional: “Ask AI” (currently disabled)
The page includes an on-device AI chat integration (WebLLM) that is commented out to avoid blocking load:
- Requires a WebGPU-enabled browser (Chrome/Edge latest)
- First run downloads model weights (one-time)

To re-enable:
1) In `index.html`, uncomment the blocks labeled “Ask AI UI (temporarily disabled)”, the WebLLM script tag, and the Ask AI logic `<script>`.
2) Hard refresh the page. Use “Diagnose” in the Ask AI header if initialization stalls.

## Structure
- `index.html` — app content and behavior
- `favicon.svg` — icon
- `.nojekyll` — bypass Jekyll on GitHub Pages
- `404.html` — SPA-friendly redirect

## License
Specify a license here if you intend to open source (e.g., MIT).
# interactive-pytorch-guide
