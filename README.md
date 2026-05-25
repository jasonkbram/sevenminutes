# Seven Minutes — Digital Companion

A mini website for *Seven Minutes* by Jason Bram, linked from the QR code in the printed book.

## Contents

- **index.html** — Single-page companion with all sections (about, characters, themes, timeline, author note, cover design)
- **styles.css** — Cover-matched cream / charcoal / yellow aesthetic
- **assets/** — Cover image, author portrait, PDF of the book

## Local preview

Open `index.html` in a browser, or run a simple server:

```bash
cd "Seven Minutes"
python3 -m http.server 8080
```

Then visit http://localhost:8080

## Deploying on GitHub Pages

Upload **the whole project**, including the `assets` folder (images + PDF). The site will not show images if only `index.html` is uploaded.

```bash
cd "Seven Minutes"
git init
git add index.html styles.css script.js base-path.js .nojekyll README.md assets/
git commit -m "Add Seven Minutes companion site"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git
git push -u origin main
```

On GitHub: **Settings → Pages → Build from branch `main` → folder `/ (root)`**.

Your site will be at `https://YOUR_USERNAME.github.io/YOUR_REPO_NAME/` (use this URL for the QR code).

### Images not showing?

1. **Check files are on GitHub** — Open your repo in the browser. You must see `assets/cover.png` and `assets/author.png`. If `assets` is missing, run `git add assets/` and push again.

2. **Test the image URL directly** — Open  
   `https://YOUR_USERNAME.github.io/YOUR_REPO_NAME/assets/cover.png`  
   If you get 404, the files were not pushed.

3. **Repo name with a subfolder** — If your site lives at `github.io/My-Repo/`, `base-path.js` fixes paths automatically. If you use a custom host, you can set this in `index.html` before `base-path.js` loads:  
   `window.SITE_BASE_PATH = '/My-Repo/';`

4. **Wait a minute** after pushing — GitHub Pages can take 1–2 minutes to update.

## Deploying elsewhere

Host this folder on Netlify, Vercel, school web space, etc. Point your QR code at the live URL. Include the full `assets` folder.

## Files

| File | Purpose |
|------|---------|
| `assets/cover.png` | Book cover |
| `assets/author.png` | Jason Bram portrait |
| `assets/seven-minutes.pdf` | Full digital novel |
| `assets/flyer.jpg` | Back-cover flyer (reference; not required on site) |
