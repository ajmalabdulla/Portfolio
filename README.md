# Portfolio Site

A single-page portfolio: About, CV, Projects, Photos, Contact. No build tools needed — just HTML/CSS/JS.

## 1. Add your content

Open `index.html` and search for the comments marked `EDIT ME`:

- **About** — rewrite the paragraph in your own words.
- **CV** — put your resume file at `assets/cv.pdf` (exact filename). The download button and the inline preview both point to that path. If you don't want the inline PDF preview, delete the `<div class="cv-embed">...</div>` block.
- **Projects** — three are pre-filled (SME Scan Station, Employee Asset Management System, Device Inventory Dashboard). Edit the text, or copy a `<div class="work-order">...</div>` block to add more (bump the `WO-0x` number).
- **Photos** — replace each `<div class="frame empty mono">photo-01.jpg</div>` with:
  ```html
  <div class="frame"><img src="assets/photo-01.jpg" alt="Describe the photo"><span class="cap mono">photo-01</span></div>
  ```
  Put your image files in `assets/`.
- **Contact** — replace the email, LinkedIn, and GitHub placeholders with your real links.

## 2. Folder structure

```
portfolio/
├── index.html
├── README.md
└── assets/
    ├── cv.pdf
    ├── photo-01.jpg
    ├── photo-02.jpg
    └── ...
```

Create the `assets/` folder yourself and drop your files in — it isn't included by default.

## 3. Host it for free — GitHub Pages

1. Create a GitHub account if you don't have one, and create a new **public** repository — name it anything, or specifically `your-username.github.io` if you want it at the root of your GitHub domain.
2. Upload `index.html`, `README.md`, and your `assets/` folder to the repository (via the GitHub web UI's "Add file → Upload files", or via git):
   ```
   git init
   git add .
   git commit -m "Initial portfolio"
   git branch -M main
   git remote add origin https://github.com/your-username/your-repo.git
   git push -u origin main
   ```
3. In the repository, go to **Settings → Pages**.
4. Under **Build and deployment → Source**, choose **Deploy from a branch**, set branch to `main` and folder to `/ (root)`, then save.
5. Wait a minute or two — GitHub will give you a live URL:
   - `https://your-username.github.io/your-repo/` (or `https://your-username.github.io/` if you named the repo `your-username.github.io`).

That's it — free hosting, HTTPS included, and every future `git push` updates the live site.

### Alternatives
- **Netlify** or **Vercel** — drag-and-drop the folder in their dashboard, or connect the GitHub repo for auto-deploys on every push.
- **Cloudflare Pages** — similar git-based free deploys.

All three are free for a static site like this one.
