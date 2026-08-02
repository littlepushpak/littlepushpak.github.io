# Little Pushpak — Website

A single-page site for **Little Pushpak** ("Khushiyon ka pitara") — Gift Hampers,
Customized Gift Hampers, Festive Gifting & Corporate Gifting.

## Before you launch

1. **Add your logo.** Save your logo file as:
   - `assets/logo.png`

   The header, hero, and browser tab icon all reference this path. If the file
   isn't there yet, the header falls back to an "LP" badge automatically —
   nothing will look broken, just less branded.

2. **Add real product photos (optional, anytime).** The Gallery section
   currently shows 6 placeholder tiles. To replace one:
   - Drop an image into `assets/` (e.g. `assets/gallery-1.jpg`)
   - In `index.html`, find the `<div class="gallery-tile placeholder">` blocks
     under `<!-- GALLERY -->` and swap a tile for:
     ```html
     <div class="gallery-tile"><img src="assets/gallery-1.jpg" alt="Describe the photo"></div>
     ```

3. **Preview locally** (optional). From this folder, run:
   ```bash
   python3 -m http.server 8000
   ```
   then open `http://localhost:8000` in your browser.

## Publish to GitHub Pages

1. **Create a GitHub account** at github.com if you don't have one.

2. **Create a new repository:**
   - Go to github.com → click **+** (top right) → **New repository**
   - Name it something like `little-pushpak` (any name works)
   - Keep it **Public** (required for free GitHub Pages)
   - Don't initialize with a README (you already have files)
   - Click **Create repository**

3. **Push this folder to GitHub.** In this folder, run:
   ```bash
   git init
   git add .
   git commit -m "Launch Little Pushpak website"
   git branch -M main
   git remote add origin https://github.com/<your-username>/<your-repo-name>.git
   git push -u origin main
   ```
   Replace `<your-username>` and `<your-repo-name>` with your actual GitHub
   username and the repo name you chose.

4. **Enable GitHub Pages:**
   - On GitHub, open your repository → **Settings** → **Pages** (left sidebar)
   - Under **Build and deployment → Source**, choose **Deploy from a branch**
   - Under **Branch**, select `main` and folder `/ (root)` → **Save**

5. **Get your live link.** After ~1 minute, refresh the same Settings → Pages
   screen — it'll show your site URL:
   ```
   https://<your-username>.github.io/<your-repo-name>/
   ```

6. **(Optional) Custom domain.** If you own a domain, add it under
   Settings → Pages → Custom domain, and point your domain's DNS to GitHub
   Pages per [GitHub's custom domain docs](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site).

## Making future updates

Any time you change a file locally:
```bash
git add .
git commit -m "Describe your change"
git push
```
GitHub Pages redeploys automatically within a minute or two.

## Project structure

```
index.html                    Main page (all sections)
css/style.css                 All styling
js/script.js                  Mobile nav toggle + footer year
assets/logo.png                ← add your logo here
assets/illustrations/*.svg     Placeholder product category art
```
