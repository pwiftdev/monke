# $MONKE — The Life of Monke

Static one-page site. No build step, no dependencies.

Monke is created by [@monkebiznis](https://www.youtube.com/@monkebiznis) on YouTube. 100% of $MONKE creator fees go to the creator, once he's onboarded.

## Before you deploy

1. **Contract address and links.** Open `index.html`, scroll to the bottom and edit the `CONFIG` block:

   ```js
   var CONFIG = {
     contractAddress: '',
     xUrl: 'https://x.com/Monke_Fun',
     telegramUrl: 'https://t.me/'
   };
   ```

   While `contractAddress` is empty the site shows "To be announced on X first." and hides the Copy buttons. Once it is set, every Buy button points to `https://pump.fun/coin/<contractAddress>`.

2. **Social preview image.** X and Telegram need a full URL for the preview card. Once you know your domain, replace the two `/og.png` values in the `<head>` of `index.html` with `https://YOUR-DOMAIN/og.png`.

## Deploy on Vercel

1. Push this folder to a GitHub repo (the files sit at the repo root).
2. In Vercel: **Add New → Project → Import** the repo.
3. Framework preset: **Other**. Leave Build Command and Output Directory empty.
4. Deploy.

To preview locally: `npx serve .` (or any static server) and open the printed URL.

## What happens on load

A short loader shows until the fonts and the hero artwork are ready, then the hero animates in and the credits popup opens. It closes with the button, the ×, a click outside, or Esc.

## Files

```
index.html               the whole page (styles + script inline)
assets/                  Monke artwork (SVG), paper grain, self-hosted fonts
og.png                   1200×630 social preview card
favicon-32.png           browser tab icon
apple-touch-icon.png     home-screen icon
vercel.json              cache headers for assets
```
