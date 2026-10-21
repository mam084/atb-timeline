# AT Battle Timeline

Turn trackers for tabletop RPGs. The GM runs them on a laptop, and players follow along live on their phones. There are two tabs:

- **ATB:** a Trails-style Active Time Battle timeline.
- **Initiative:** a classic D&D initiative tracker.

**Live app:** https://mam084.github.io/atb-timeline/

## Features
- **Turn order strip** in the style of the Trails games: the current turn, everyone queued behind it, and spells being cast as their own events.
- **Confirm with preview:** picking an action shows a ghost card where that character will land, along with the AT bonus waiting there. Players see the preview too.
- **AT bonuses** (CRIT, HEAL 10% / 20% / 50%, EP, CP) are tied to timeline positions, so delaying or hastening someone changes which bonus they get. The GM can edit any slot's bonus.
- **Speed:** + is faster. Party speed comes from each character sheet (frame speed −1, 0 or +1); enemy speed is set in the Combatants list. Three ways to apply it, chosen in Settings: **turn rate** (the default and the rulebook formula, `base × 10 / (10 + speed)`: each point is the same 10% more or fewer turns, so stacking speed never snowballs), proportional (each point changes the delay by 10%), or flat.
- **Party HP / EP / CP:** every party member has HP, EP and CP (capped at 200). A **Party** panel shows everyone's bars plus speed, crit range, art DC and AC; edit any value, or tap the CP buttons (+10 hit, +5 crit, +5 hurt, +15 big hit, +10 kill — adjustable in Settings). Dropping to 0 HP knocks a character out.
- **CP and EP spend themselves:** crafts take a CP cost and arts an EP cost when you confirm them. S-Crafts and S-Breaks need 100 CP and spend 100; at 200 CP they can be empowered and spend all 200. A character needs a regular turn between S-Crafts. HEAL / EP / CP AT bonuses apply to whoever takes that turn.
- **Character sheets:** each party member has a sheet with level, frame, the six ability scores, armor, movement, crafts and S-Craft. Picking one of the 10 frames sets hit die, speed and armor proficiency (or choose Custom and set them yourself). It works out max HP the 5e way (full hit die + CON at level 1, then the die's average + CON per level, plus a Bonus HP box for rolls, feats and accessories), AC from the armor table (Light 11/12 + DEX, Medium 13/14 + DEX max 2, Heavy 16/18; heavy armor without the STR costs 2 squares of movement; plus quartz and statuses), proficiency, art attack (prof + INT), art DC (8 + prof + INT), the WIS bonus to heals and buff turns, the WIS reduction to ailments, and the weapon crit range (20 − positive CHA modifier; ×1.5 damage). It warns when armor is heavier than the frame is proficient with. Open one from **Open sheet** on a party card; players edit their own from the **Sheet** tab on their phone. Every build change shows in your battle log (tagged SHEET) but stays out of the players' log.
- **Agency funds:** one shared mira pool for the party, editable by you and by players from their phones.
- **Orbment builder:** on each character's sheet. You design the orbment (center + 6 line slots split into lines, e.g. 4+2), unlock slots, and lock slots to an element; players place quartz from the starter list or type in a custom one (name, element, value, bonus), or tick **Type line totals** to enter each line's element values by hand. The center slot counts toward every line. The app lists every art from Zero's list that one line meets, plus the arts one element point away. Max EP comes from unlocked slots (center 60; by depth 20, 45, 80, 125, 180, 245 — 80 EP at the start of play) plus EP quartz, and quartz bonuses (AC, max HP, speed from Action 1 — one per orbment — movement, weapon/art bonuses, status on a 20) feed the sheet. **EP Cut 1** (Space) takes 10% off every art's EP cost and **Cast 1** (Time) cuts cast times by 10% (Daybreak's versions); both show in the arts lists and fill in when an art is cast.
- **Status effects:** add any status from the Arts d20 tab (ailments, stat downs, buffs) to anyone from the form under Combatants; remove one with its ×. Statuses show on timeline cards, party cards, the roster and players' phones, and count down on the target's own turns. Default turns follow the rulebook (ailments and stat downs shorten by the target's WIS, minimum 1; add the caster's WIS to buffs yourself). Chrono Drive/Down and Calamity Claw change speed, Crest/Saint add AC, Sylphid/Claw/Dark Matter change movement. Burn rolls 1d6 and Regen/Impassion apply at the start of a turn. Freeze and Faint put a **Skip turn** prompt on that turn and end after it; Sleep and Petrify stop the character until removed (damage wakes a sleeper). Mute locks Arts and cancels a charging art; Seal locks crafts, S-Crafts and S-Breaks. Knock-outs and New battle clear statuses. A status put on someone during their own turn starts on their next one.
- **Crafts:** each sheet lists the character's crafts (name, CP cost, delay, effect) and their S-Craft. When you choose Craft on the turn panel, pick one from the sheet to fill in its name, CP and delay.
- **Players act from their phones:** on their turn, a player's phone shows the actions with their delays. Arts opens the arts their orbment can cast (with EP after EP Cut, rolls, cast and recovery), Craft opens their crafts, and S-Craft offers regular or empowered. Their pick shows as a preview on the timeline for everyone, and they **confirm it on their phone** (or cancel). Your tracker checks it's their turn and that they can pay before it goes through. You see it tagged FROM PHONE and can still confirm or cancel it yourself. Phones also get Resolve when their art goes off and Skip turn when they're frozen.
- **Casting from the list:** when an art is cast, typing or picking its name fills its cast time, recovery and EP cost, shows its area, roll and effect with the caster's numbers, and warns if it isn't on that character's orbment.
- **Arts casting, Impede, S-Break, KO/revive**, delay/hasten tools, undo, and a battle log.
- **Player view:** a link or QR code that shows the timeline, party bars and log on phones, updating live.
- **Phones track their own character:** in the ATB tab a player picks their character once (the phone remembers it), then updates their HP, EP and CP from the phone. Changes go to the GM's tracker, which only accepts changes to the character that phone is linked to. The GM's Party panel marks linked characters with **PHONE**.

## Rules the app follows (Oct 20)
- **Timing on Zero's scale:** an attack is a 30-tick turn; move, defend and item 20; crafts 25 / 30 / 35; S-Craft recovery 40; each art uses its own cast and recovery from the Arts d20 tab. Speed caps at ±3. Saved tables convert automatically: default delays become these, custom ones and the timeline in progress are tripled, crafts are scaled to match.
- **LCK replaces CHA.** It sets the weapon crit range, adds to ailment rolls, and makes ailments and stat downs you inflict last longer.
- **Vantages:** pick a History arcana (+2 to a score) and a Destiny arcana (+1); type base scores and the sheet adds the bonuses. Fighting style is recorded for flavor.
- **Gear:** weapon, armor, boots and two accessories. Light boots (+1 move), Vigor ring (+5 HP), Focus pendant (+10 EP), Fighter's medal (+10 CP when you press New battle) and Ward charms (immune to one status) apply themselves; the rest show as notes.
- **Status durations:** the Add status form has a **From** box. Buffs last their listed turns + the caster's WIS. Ailments last listed − the target's WIS (the caster's LCK no longer lengthens them); stat downs last listed + the caster's LCK − the target's WIS (minimum 1). **Stuns** (Freeze, Faint, Sleep, Petrify) always last 2 turns: each stunned turn the character can't act and presses **Pass turn**, which costs only the **Stunned turn** delay (20, in Settings). Freeze also takes 10% of max HP at the start of each stunned turn, from party members and from enemies with tracked HP. Mark an enemy as **Boss** to halve all of these (a stun lasts 1 turn), make it immune to Petrify, and remind you that rolls to inflict ailments on it have disadvantage.
- **Quartz (Daybreak versions):** EP Cut 1 (Space 1) cuts art EP costs by 10%; Cast 1 (Time 1) cuts cast times by 10%; Defense 1 is −1 weapon damage taken; Evade 1 is +1 AC.
- **Whole ticks:** every percentage (speed, Cast quartz) is applied first and the delay is rounded once to a whole tick. Cast 1 no longer changes the cast time you type: the panel shows "−10% Cast" and the landing spot includes it (15 → 14 at speed ±0).
- **Arts list per caster:** on the GM's turn panel, a party member's Arts form shows buttons for the arts their orbment can cast, and the name box only suggests those. A known art that isn't on their orbment can't be confirmed (enemies, and party members without an orbment, can still cast anything; custom names still work).
- **Starting a battle:** clear the last fight's enemies with **Clear enemies** (the party stays), add new ones, pick an **Opening** and press **Start battle** (also in the top bar). Everyone rolls d20 + initiative bonus (DEX from the sheet; enemies have an **Init** box in Combatants, the add form and the test encounters). The first turn lands (25 − roll) ticks in, scaled by speed. Party advantage puts enemies 15 ticks later; enemy advantage does that to the party. The log shows the party's totals; the full rolls are in a GM-only line. HP, EP and CP carry over; statuses and KOs clear.
- **Skills & saves:** a Skills tab on phones (and a Skills section in the GM's sheet panel) shows all six saving throws and the 18 5e skills with totals. Each frame grants two save proficiencies (Bulwark CON/STR, Vanguard WIS/STR, Spellblade CON/INT, Duelist DEX/STR, Balanced CON/LCK, Marksman DEX/INT, Tactician WIS/INT, Phantom DEX/LCK, Adept WIS/LCK, Sage WIS/INT); a custom frame picks its own two. Players set each skill to —, Prof or Expert; Persuasion, Deception and Performance use LCK and Intimidation uses STR. Sturdy boots (+1 STR saves), Silver badge (+1 to a save you pick), DEX-save quartz and Scout's lens (+2 Perception) are added in; armor you aren't proficient in marks STR/DEX saves and skills with disadvantage. It also shows Passive Perception, a skill count against the 4 + 1-per-3-levels guideline, and a free-text Tools line. The sheet's chips now include **Craft DC** (8 + proficiency + STR or DEX).

## GM tools
- **Quartz search:** tap a slot and type to find a quartz by name, element or bonus (each word matches the start of a word: "fire", "ac", "weapon damage"). Enter picks the first match; Remove empties the slot; custom quartz are still there.
- **Enemy HP:** the Combatants list has an HP column. Type current/max HP, or use the Hit box to subtract damage; at 0 the enemy is defeated (KO), and Revive brings it back at 1 HP. A thin HP bar shows on your timeline cards. Players never see enemy HP.
- **Test encounters:** Combatants › Test encounter › Add enemies loads one of four playtest fights for 3 level-3 PCs (Back-Alley Shakedown, Geofront Vermin, Orbal Security Sweep, Almata Enforcer) with HP, speed, Boss flag and a stat line under each name. Full write-ups are in the rules doc's Test Encounters tab.

## Initiative tab (D&D)
- Add your party and monsters. Monsters with no initiative roll d20 + bonus automatically (**How many** adds Goblin A, B, C…).
- Players open the same link, pick their character (or add a new one), and **send their initiative** from their phone. It drops straight into the order.
- **Start combat**, then **Next turn** (or press **N**). The current turn is highlighted, the next one is marked, and rounds are counted.
- On a player's turn, their phone shows **End my turn**, which advances the tracker for you.
- **Hide** keeps a monster off players' screens until you reveal it. **Down** marks someone at 0 HP. **New encounter** clears monsters and initiative but keeps the party.
- Ties go to the higher bonus; type a decimal like 15.5 to place someone by hand.

## Run it
Open `index.html` in a browser. Your encounter is saved in that browser. Live sharing needs the one-time setup below.

## One-time setup for live sharing (about 10 minutes, free)
Live sharing uses a free Firebase Realtime Database. The Spark plan's limits are far beyond what a game table needs.

1. Go to https://console.firebase.google.com, click **Create a project**, and give it a name (e.g. `atb-timeline`). You can turn Google Analytics off.
2. **Turn on anonymous sign-in:** Build → Authentication → Get started → Sign-in method → **Anonymous** → Enable → Save.
3. **Create the database:** Build → Realtime Database → Create database → choose a location → **Start in locked mode**.
4. **Add the rules:** (update them whenever `database.rules.json` changes) in Realtime Database, open the **Rules** tab, replace everything with the contents of `database.rules.json`, then click **Publish**.
5. **Get your config:** Project settings (gear icon) → General → Your apps → click the web icon `</>` → register the app (Hosting isn't needed). Copy the values from the `firebaseConfig` it shows into `config.js`. Make sure `databaseURL` is filled in; if it's missing, copy the URL shown at the top of the Realtime Database page.
6. Commit `config.js`. GitHub Pages updates within a minute or two.

The values in `config.js` aren't secret; Firebase web configs are meant to be public. The database rules are what protect the table. Anyone can read a table, but only the browser that created it can change it. Players can only drop off requests ("here's my initiative", "end my turn"), which the GM's tracker checks before applying.

## At the table
1. On your laptop, click **Share with players** (bottom left). Players scan the QR code or open the link.
2. On each turn, pick the acting character's action, check the preview, then **Confirm**.
3. **Player view** turns your own screen into the player display, useful for a TV.

Notes:
- Your laptop remembers its table, so reloading reconnects to the same code.
- To run the game from a different computer, click **New table code** there and send players the new link.

## How delay works
`next turn = now + delay`, where `delay` is the action's base delay adjusted by speed (+ is faster):
- **Turn rate:** `base × 100 / (100 + speed × step%)`, kept to one decimal. At 10% that's the rulebook's `base × 10 / (10 + speed)`: +1 gives 9.1 on a base of 10, −1 gives 11.1.
- **Proportional:** `base × (1 − speed × step%)`, rounded.
- **Flat:** `base − speed`.

Tables saved before speed existed are converted automatically: the old delay modifier becomes speed with the sign flipped, so turn order doesn't change. Existing tables keep the mode they were using; switch to Turn rate under Settings → Speed.

Delays never drop below 1. Ties go to whoever was already waiting.

## Files
| File | Purpose |
| --- | --- |
| `index.html` | The whole app (no build step). |
| `config.js` | Your Firebase web config (empty means no live sharing). |
| `database.rules.json` | Security rules to paste into Firebase. |
