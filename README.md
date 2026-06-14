# Logan Ramanathan — personal site

A static, single-page portfolio with per-project detail pages. No build step, no dependencies — just HTML, CSS, and a little vanilla JS.

## Structure

```
.
├── index.html            # the main page
├── favicon.svg
├── vercel.json           # Vercel config (clean URLs + asset caching)
├── .vercelignore         # keeps leftover source uploads out of the deploy
├── assets/               # images, résumé, report PDFs
└── projects/             # project detail pages + shared project.css
    ├── pioneer-camera.html
    ├── hydrogen-crm.html
    ├── cafe-search.html
    ├── guitar.html
    └── project.css
```

## Deploy to Vercel

It's a static site, so any of these work:

**A. Dashboard (no terminal)**
1. Go to vercel.com → **Add New… → Project**.
2. Drag this whole folder onto the import screen (or connect a Git repo containing it).
3. Framework Preset: **Other**. Build Command: *(leave empty)*. Output Directory: `.` (root).
4. **Deploy**.

**B. Vercel CLI**
```bash
npm i -g vercel
cd loganramanathan-website
vercel          # preview deploy
vercel --prod   # production deploy
```

**C. Git + Vercel**
Push this folder to a GitHub repo, then **Import Project** from that repo in Vercel. Every push auto-deploys.

## Custom domain

After the first deploy, add `loganramanathan.com` under **Project → Settings → Domains** and point the domain's DNS at Vercel (it shows the exact records).

## Editing

- Swap any image by replacing the file in `assets/` (keep the same filename).
- Project cards and copy live in `index.html`; each project's long write-up lives in `projects/<name>.html`.
