# jatinchopra.github.io

Personal / research website for Jatin Chopra — MSc Astrophysics, AIfA, Universität Bonn.

Plain HTML/CSS/JS, no build step, so it works directly with GitHub Pages.

## Pages

- `index.html` — home: intro, PhD search status, current research
- `astrophotography.html` — deep-sky imaging gallery
- `about.html` — name meaning, academics, interests, outreach, awards
- `css/style.css` — all styling
- `js/main.js` — mobile nav toggle
- `assets/docs/Jatin_Chopra_CV.pdf` — your CV (already included, linked from the nav bar and footer on every page)

## 1. Add your photos

Drop your images into `assets/images/` using these exact filenames (or update the paths in the HTML if you'd rather use your own names):

| File | Used on |
|---|---|
| `assets/images/portrait.jpg` | Home page hero |
| `assets/images/m51.jpg` | Astrophotography — M51 |
| `assets/images/m101.jpg` | Astrophotography — M101 |
| `assets/images/ngc891.jpg` | Astrophotography — NGC 891 |
| `assets/images/ngc7339.jpg` | Astrophotography — NGC 7339 |
| `assets/images/m1.jpg` | Astrophotography — M1 |

For each image, find the placeholder block that looks like this in the HTML:

```html
<div class="img-slot">
  <!-- Replace this div's contents with:
       <img src="assets/images/portrait.jpg" alt="Jatin Chopra"> -->
  add<br>portrait.jpg<br>here
</div>
```

and replace the placeholder text with the commented-out `<img>` line (uncomment it, delete the placeholder text). Do the same for each `.plate` block on the astrophotography page.

## 2. Update your CV

Swap `assets/docs/Jatin_Chopra_CV.pdf` for a newer export whenever you update it — keep the same filename and every link on the site keeps working automatically.

## 3. Deploy on GitHub Pages

1. Create a new repo — for a user site, name it exactly `<your-github-username>.github.io`; for a project site, any name works.
2. Copy every file in this folder into the repo root (keep the folder structure: `css/`, `js/`, `assets/`).
3. Commit and push:
   ```bash
   git init
   git add .
   git commit -m "Initial site"
   git branch -M main
   git remote add origin https://github.com/<username>/<repo>.git
   git push -u origin main
   ```
4. In the repo settings → **Pages**, set the source to the `main` branch, root folder.
5. Your site will be live at `https://<username>.github.io/` (user site) or `https://<username>.github.io/<repo>/` (project site).

## Notes

- Fonts (Fraunces, Inter, JetBrains Mono) load from Google Fonts via CDN — no local font files needed.
- The phone number from your CV was left off the public site; only your two emails are shown. Add it back into the footer/log card if you'd rather have it public.
- Everything is plain CSS with custom properties at the top of `style.css` (`:root`) — change `--accent` / `--accent-2` there if you want to shift the palette later.
