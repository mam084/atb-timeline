# AT Battle Timeline

A Trails-style ATB turn tracker for tabletop play. One self-contained file: `index.html`.

## Run it
Open `index.html` in any browser. No install, no server. Your encounter is saved in that browser automatically.

## Deploy it (pick one)
- **Netlify Drop:** go to app.netlify.com/drop and drag this folder in. You get a public URL in seconds.
- **GitHub Pages:** create a repo, add `index.html`, then Settings → Pages → Deploy from branch (`main`, root).
- **Vercel / Cloudflare Pages:** create a project from the repo; no build step, output directory is the root.

## At the table
- GM view: pick the current actor's action; the app reschedules them (delay = base × 20 ÷ SPD).
- Arts put a cast event on the timeline; resolve or Impede it when it comes up.
- S-Break pulls any combatant to the front and steals the current slot's AT bonus.
- AT bonuses belong to timeline positions. Click a slot to change its bonus.
- Player view hides the GM controls (and the numbers, unless you turn them on). Put it on a second screen or TV.
