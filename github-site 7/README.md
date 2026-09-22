# K.SO* — Andrew Caso

Portfolio site. Static HTML — no build step, no dependencies to install.

## What's here

```
index.html                          entry point (redirects to the landing page)
Andrew Caso Landing - Combined.dc.html   landing page
About.dc.html  Contact.dc.html
Commercial/          index + 14 project pages (13 visible) + template
Music Videos/        index + 23 project pages + template
Photoshoot/          index + 16 project pages + template
Creative Direction/  index + 4 project pages (1 visible) + template
assets/   logo marks
stills/   photography
support.js  image-slot.js            page runtime
```

## Put it on GitHub

1. github.com → **New repository** → name it (e.g. `andrew-caso`), Public, **no** README.
2. On the empty repo page: **uploading an existing file** → drag in everything from
   this folder (select all files *and* folders) → **Commit changes**.
3. Optional, to publish it live: **Settings → Pages → Source: Deploy from a branch →
   `main` / `root` → Save.** The site appears at
   `https://<user>.github.io/<repo>/` in a minute or two.

Command line instead:

```sh
cd path/to/this/folder
git init
git add .
git commit -m "Andrew Caso portfolio"
git branch -M main
git remote add origin https://github.com/<user>/<repo>.git
git push -u origin main
```

## Notes

- Pages need an internet connection: fonts (Google Fonts), the page runtime (unpkg)
  and the films (YouTube / Vimeo) all load from the network.
- Opening a file straight off disk (`file://`) works, but images dropped through the
  editor read from `.image-slots.state.json` via fetch, which some browsers block on
  `file://`. Serve locally instead: `python3 -m http.server` then open
  `http://localhost:8000`.
- Filenames contain spaces — that is fine on GitHub Pages; links are already encoded.
- Vimeo films must stay public or unlisted **with embedding allowed**.
