# Panther Speed

Sprint training for Wenatchee High School — 100m, 200m, 400m.

Athletes pick their event (100, 200 or 400) and see today's workout in plain
language — built for their event and the time of year.

## Live app

Once Pages is turned on, the app is at:

`https://YOUR-USERNAME.github.io/panther-speed/`

That's the link you text athletes.

## Putting it on GitHub Pages

1. On GitHub, click **New repository**. Name it `panther-speed`. Set it to
   **Public** — Pages is only free on public repos. Click Create.
2. On the empty repo page, click **uploading an existing file**.
3. Drag in everything from this folder, including the `docs` folder and the
   `.nojekyll` file. Click **Commit changes**.
4. Go to **Settings → Pages**. Under "Build and deployment", set Source to
   **Deploy from a branch**, branch **main**, folder **/ (root)**. Save.
5. Wait about a minute, then refresh. GitHub shows the link at the top.

## Changing something later

Open `index.html` on GitHub, click the pencil icon, edit, commit. The site
rebuilds itself in under a minute and the link never changes. The workouts are
plain lists near the top of the script (`ACCEL`, `MAXV`, `EVENT_DAY`, …).
After any change, bump `VERSION` in `sw.js` so phones load the new copy.

Everything is in that one file — the workouts, the colors, the layout. There
is nothing to install and nothing to build.

## What's in here

| File | What it is |
|---|---|
| `index.html` | The entire app. |
| `manifest.json` | Lets phones install it to the home screen. |
| `sw.js` | Keeps the app working with no signal. |
| `icon-192.png`, `icon-512.png` | Home screen icon. |
| `logo.png` | Panthers mark, background removed. |
| `.nojekyll` | Tells GitHub to serve the files as-is. Don't delete it. |
| `docs/` | What the app is, what's been decided, what's next. |

## For athletes

Open the link, then:

- **iPhone** — Share button, then *Add to Home Screen*
- **Android** — menu, then *Install app*

It opens full screen with the Panthers icon after that.

## Status

Working and usable. See `PROGRESS.md`.

## Logo

The Panthers mark belongs to Wenatchee School District. Check with your
athletic director before sending this to athletes. Note that a public GitHub
repo makes the image file publicly downloadable.
