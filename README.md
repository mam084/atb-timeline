# AT Battle Timeline

A Trails-style Active Time Battle (ATB) turn tracker for tabletop RPGs. The GM runs it on a laptop; players follow the turn order and battle log live on their phones.

**Live app:** https://mam084.github.io/atb-timeline/

## Features
- **Turn order strip** in the style of the Trails games: the current turn, everyone queued behind it, and spells being cast as their own events.
- **Confirm with preview:** picking an action shows a ghost card where that character will land, along with the AT bonus waiting there. Players see the preview too.
- **AT bonuses** (CRIT, HEAL, EP, CP) are tied to timeline positions, so delaying or hastening someone changes which bonus they get. The GM can edit any slot's bonus.
- **Delay modifiers:** each character has a modifier (default −2 to +2). It can scale every delay proportionally (default 10% per point) or add/subtract a flat amount. You choose which in Settings.
- **Arts casting, Impede, S-Break, KO/revive**, delay/hasten tools, undo, and a battle log.
- **Player view:** a link or QR code that shows the timeline and log on phones, read-only, updating live.

## Run it
Open `index.html` in a browser. Your encounter is saved in that browser. Live sharing needs the one-time setup below.

## One-time setup for live sharing (about 10 minutes, free)
Live sharing uses a free Firebase Realtime Database. The Spark plan's limits are far beyond what a game table needs.

1. Go to https://console.firebase.google.com, click **Create a project**, and give it a name (e.g. `atb-timeline`). You can turn Google Analytics off.
2. **Turn on anonymous sign-in:** Build → Authentication → Get started → Sign-in method → **Anonymous** → Enable → Save.
3. **Create the database:** Build → Realtime Database → Create database → choose a location → **Start in locked mode**.
4. **Add the rules:** in Realtime Database, open the **Rules** tab, replace everything with the contents of `database.rules.json`, then click **Publish**.
5. **Get your config:** Project settings (gear icon) → General → Your apps → click the web icon `</>` → register the app (Hosting isn't needed). Copy the values from the `firebaseConfig` it shows into `config.js`. Make sure `databaseURL` is filled in; if it's missing, copy the URL shown at the top of the Realtime Database page.
6. Commit `config.js`. GitHub Pages updates within a minute or two.

The values in `config.js` aren't secret; Firebase web configs are meant to be public. The database rules are what protect the table. Anyone can read a table, but only the browser that created a table can change it.

## At the table
1. On your laptop, click **Share with players** (bottom left). Players scan the QR code or open the link.
2. On each turn, pick the acting character's action, check the preview, then **Confirm**.
3. **Player view** turns your own screen into the player display, useful for a TV.

Notes:
- Your laptop remembers its table, so reloading reconnects to the same code.
- To run the game from a different computer, click **New table code** there and send players the new link.

## How delay works
`next turn = now + delay`, where `delay` is the action's base delay adjusted by the character's modifier:
- **Proportional:** `base × (1 + mod × step%)`, rounded.
- **Flat:** `base + mod`.

Delays never drop below 1. Ties go to whoever was already waiting.

## Files
| File | Purpose |
| --- | --- |
| `index.html` | The whole app (no build step). |
| `config.js` | Your Firebase web config (empty means no live sharing). |
| `database.rules.json` | Security rules to paste into Firebase. |
