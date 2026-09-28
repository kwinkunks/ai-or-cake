# AI or Cake?

A tiny static browser game: you're shown a cake image and must decide whether it's a
**real** photo or **AI-generated**. Six rounds, then a score. Built to play with a small
group during a presentation.

## Run locally

Because the game loads images from the `images/` folder, open it through a local web
server rather than double-clicking the file:

```bash
python3 -m http.server 8000
# then open http://localhost:8000/
```

## Publish on GitHub Pages

1. Push to GitHub (the `main` branch).
2. Repo **Settings → Pages** → *Build and deployment* → **Deploy from a branch**.
3. Select branch **main**, folder **/ (root)**, then **Save**.
4. The game will be live at `https://<user>.github.io/<repo>/` after a minute.

## Files

- `index.html` — layout and styling (self-contained, no dependencies)
- `script.js` — game logic + the embedded list of image paths
- `images/real/`, `images/synthetic/` — the cake images

If you add or remove images, update the `REAL` / `SYNTHETIC` arrays at the top of
`script.js`.
