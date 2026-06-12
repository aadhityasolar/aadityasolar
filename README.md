# Aadhitya Solar — Website

Fast, multi-page static site for GitHub Pages. No frameworks, optimized WebP images (~770 KB total for all photos).

Pages: index.html (Home) · about.html · services.html · gallery.html · contact.html

## How to upload to GitHub (replace the old site)

1. Open your repo: github.com/sethu-pathi/aadhityasolar
2. Delete the old files in the repo (or upload over them).
3. Click **Add file → Upload files** and drag in EVERYTHING inside this folder:
   - index.html, about.html, services.html, gallery.html, contact.html
   - the whole `assets` folder
   - CNAME
4. Commit. The site will be live at https://sethu-pathi.github.io/aadhityasolar/ in 1–2 minutes.

## Connect your GoDaddy domain (www.aadhityasolar.in)

1. The `CNAME` file in this folder already contains: www.aadhityasolar.in — keep it in the repo root.
2. In GoDaddy → My Products → your domain → **DNS**:
   - Add a **CNAME** record:  Name: `www`  →  Value: `sethu-pathi.github.io`
   - Add four **A** records for the root domain (Name: `@`), one for each IP:
     185.199.108.153
     185.199.109.153
     185.199.110.153
     185.199.111.153
3. In GitHub repo → **Settings → Pages**: set Custom domain to `www.aadhityasolar.in` and tick **Enforce HTTPS** (appears after DNS propagates, up to 24–48 h, usually under 1 h).

## Why this version is fast

- Old site embedded photos as base64 inside one huge HTML file → slow first load.
- Now images are separate compressed WebP files with lazy loading, so the page paints instantly.
- The hero animation is pure CSS (zero image weight) and works on both desktop and mobile.

## Things you may want to edit

- Home page stats: "100% Customer Satisfaction" and "2 MW+ Power Generated" are estimates — update the numbers in index.html (search for `data-count`).
- Add more gallery photos: drop .webp/.jpg files into `assets/img/` and copy one `<div class="g-item">…</div>` block in gallery.html.
