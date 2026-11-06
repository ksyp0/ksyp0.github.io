# Kashyap Raj Karki — Portfolio

Personal portfolio site built with plain HTML, CSS and JavaScript (no build step), ready for GitHub Pages.

## Structure

```
.
├── index.html                    # All page content
├── 404.html                      # Redirects unknown paths to the homepage
├── .nojekyll                     # Tells GitHub Pages to serve files as-is
└── assets/
    ├── css/style.css             # Styles, dark/light theme, responsive rules
    ├── js/main.js                # Theme toggle, mobile menu, animations
    ├── favicon.svg
    └── Kashyap_Raj_Karki_CV.pdf  # Linked from the "Download CV" buttons
```

## Preview locally

```bash
python3 -m http.server 8000
# open http://localhost:8000
```

## Deploy to GitHub Pages

1. Create a repo on GitHub. Name it `ksyp0.github.io` to serve at `https://ksyp0.github.io/`
   (any other name serves at `https://ksyp0.github.io/<repo-name>/`).
2. Push this folder:
   ```bash
   git init
   git add .
   git commit -m "Initial portfolio"
   git branch -M main
   git remote add origin https://github.com/ksyp0/ksyp0.github.io.git
   git push -u origin main
   ```
3. On GitHub: **Settings → Pages → Build and deployment → Source: Deploy from a branch**,
   branch `main`, folder `/ (root)`. Save. The site is live in a minute or two.

### Custom domain (kashyaprajkarki.com.np)

1. Add a file named `CNAME` at the repo root containing only: `kashyaprajkarki.com.np`
2. At your DNS provider, add `A` records for the apex domain pointing to
   `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`,
   and a `CNAME` record for `www` pointing to `ksyp0.github.io`.
3. In **Settings → Pages**, enter the custom domain and tick **Enforce HTTPS** once available.

## Updating content

Everything lives in `index.html`, grouped by section comments (Hero, About, Skills, Experience,
Education, Contact). Replace `assets/Kashyap_Raj_Karki_CV.pdf` when your CV changes.
Colours are CSS variables at the top of `assets/css/style.css`.
