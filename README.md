# Tick (PWA)

A simple app to tick off your daily activities. Ticks clear by themselves every new day. 

## What's inside

| File | What it does |
|---|---|
| `index.html` | The whole app (look, buttons, saving, daily reset) |
| `manifest.json` | App name, icon and colors, so phones can install it |
| `sw.js` | Service worker: saves the files so the app works offline |
| `icons/` | App icons |

## Change the default activities

Open `index.html`, find `const DEFAULTS = [` and edit the list:

```js
{ name: "Drink 8 glasses of water" },
```

Note: the defaults only load the **first time** the app opens. After that, **swipe a task left** to delete it, **hold and drag** a task to change the order, or use the box at the bottom to add new ones.

## Put it online (free) so you can install it on your phone

A PWA must be on an **https** link. The easiest free way:

1. Go to **https://app.netlify.com/drop**
2. Drag the whole `tick` folder onto the page.
3. You get a link like `https://something.netlify.app`. Open it on your phone.

Other free options: GitHub Pages, Vercel, Cloudflare Pages.

## Install it on your phone

- **Link:** https://aniqmohdf231005.github.io/Tick/
- **Android (Chrome):** open the link → tap the **Install this app** button (or menu ⋮ → *Install app*).
- **iPhone (Safari):** open the link → tap **Share** → **Add to Home Screen**.

## Updating the app later

If you change any file, open `sw.js` and raise the number in `tick-v19` (for example to `tick-v20`). This tells phones to get the new version.

## Good to know

- Your list and ticks are saved **on your device only**. Clearing browser data will erase them.
- The reset uses your phone's own clock, so it clears at your local midnight.
