# Greeshma & Yedu — Wedding Invitation (BRIDE-SIDE)

Bride-side version of the groom-side invitation. Same design, animations, video flow and music
controls — only content and ordering differ (Greeshma T and her family first; hosted by
Mr. Girish V Nair & Mrs. Rajani T).

Plain HTML5 / CSS3 / vanilla JavaScript. No build step — deploy the folder to any static host
(GitHub Pages, Netlify, Vercel, S3, shared hosting).

## Run locally
    python3 -m http.server 8080      # then open http://localhost:8080

## Things to do before going live
1. **Set the domain (required for share previews).** `index.html` contains the placeholder
   `https://YOUR-BRIDE-SIDE-DOMAIN` in og:url, og:image, og:image:secure_url and twitter:image.
   Replace it with this site's own address (not the groom-side one), e.g.:

       sed -i 's#https://YOUR-BRIDE-SIDE-DOMAIN#https://your-real-domain.com#g' index.html

2. **Photos** — drop files into `assets/images/gallery/` (folder is created automatically when you add it):
   `bride.jpg`, `groom.jpg` (portraits, 3:4) and `photo-01.jpg` … `photo-06.jpg`.
   Until then, labelled placeholders are shown. Bride-first slot labels:
   01 Greeshma · 02 Yedu · 03 Greeshma & Yedu · 04 Greeshma · 05 Yedu · 06 Greeshma & Yedu.
3. **Maps buttons** — Google Maps *search* links for the two venue names (unchanged from the
   groom-side site). Swap in the venues' own "Share" links once confirmed.
4. **Music** — `assets/audio/inkem-inkem_g300U6Yp.mp3` is carried over from the template.
   Replace with a track you are licensed to use (same filename, or update `index.html`).

## Key files
| Role | Path |
|------|------|
| Opening video (bride-first, 720×1280, 8 s) | `assets/video/invitation-reveal.mp4` |
| Share image (1200×630, bride-first) | `assets/images/share/og-thumbnail.jpg` |
| Cover / hero (no names baked in) | `assets/images/cover/cover.png`, `assets/images/hero/` |
| Countdown target | `js/main.js` → 2026-12-30 10:30 IST (`+05:30`, correct in any time zone) |
