# Garden Retreat Games

A installable PWA (Progressive Web App) with five group games for a youth retreat, built for one iPad and a whole room of people:

- **Team Shuffle** — randomly split everyone into teams
- **Finger Frenzy** — multi-touch "last finger standing" elimination game
- **Prompt Deck** — icebreakers, would-you-rathers, faith talk, dares and challenges, with an optional name list and a group points tracker
- **Act It Out** — charades with Bible characters, animals, actions and movies
- **Word Bomb** — pass-the-iPad word game with a ticking timer, sound effects and forfeits

## Files

```
index.html              the whole app (one page, no build step)
manifest.webmanifest     PWA install metadata
sw.js                    service worker for offline play
icons/icon-192.png       app icon
icons/icon-512.png       app icon
```

## Deploy to GitHub Pages

1. Create a new GitHub repo (e.g. `garden-retreat-games`) and push these files to the root of the `main` branch.
2. In the repo, go to **Settings → Pages**.
3. Under **Build and deployment**, set **Source** to "Deploy from a branch", branch `main`, folder `/ (root)`.
4. Save. GitHub will give you a URL like `https://yourusername.github.io/garden-retreat-games/`.
5. Open that URL on the iPad in Safari.

## Installing it as an app

- **iPad (Safari):** tap the Share icon, then "Add to Home Screen". It'll open full-screen like a native app from then on.
- **Android/desktop Chrome:** an "Install App" button appears on the home screen automatically once the browser detects it's installable.

## Notes

- Everything runs client-side — no server or database needed.
- The service worker caches the app after the first load, so it keeps working with no signal (handy outdoors at a garden retreat).
- Word Bomb's sound effects use Tone.js, loaded from a CDN — the very first load needs internet, after that it's cached.
- Want to add more prompts, categories or charades words? They're plain JavaScript arrays near the top of the `<script>` section in `index.html` — easy to extend without touching the rest of the code.
