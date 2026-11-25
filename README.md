# Varada V N A Santosh — ML Notes

A simple, static portfolio site covering GPU/CUDA GEMM optimization, Transformers
& attention, distributed & large-scale LLM training (DDP to ZeRO), and generative
models.

The site is self-contained — no build step and no external CDNs for code. KaTeX
(math) and highlight.js (code highlighting) are vendored under `assets/`, so it
works offline and renders identically anywhere.

> Note: the two GEMM articles embed a few diagrams hosted on Hashnode's image CDN
> (plus one NERSC roofline image). These load over the web when the site is viewed
> online. Everything else — including all LLM-training figures — is local.

## Preview locally

Open `index.html` in a browser, or serve the folder:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Deploy to GitHub Pages

1. Push the **contents** of this folder to a new repo (so `index.html` is at the repo root):

   ```bash
   git init
   git add .
   git commit -m "Portfolio site"
   git branch -M main
   git remote add origin https://github.com/<your-username>/portfolio.git
   git push -u origin main
   ```

2. On GitHub: **Settings -> Pages -> Build and deployment**, Source *Deploy from a
   branch*, branch **main**, folder **/ (root)**, Save.

3. Live at `https://<your-username>.github.io/portfolio/` within a minute or two.

> To host at `https://<your-username>.github.io/` (no `/portfolio/` suffix), name
> the repository `<your-username>.github.io`.

## Structure

```
index.html          Home, notes index, about
posts/*.html        One page per note
images/             Local figures (CUDA, transformers, LLM-training)
assets/style.css    Styling
assets/katex/       Vendored KaTeX (math)
assets/hljs/        Vendored highlight.js (code)
```
