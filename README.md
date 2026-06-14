# Hop Runner

**AppADay #047 · 2026-06-23 · Category: G (Games)**

A Mario-style side-scrolling platformer set in a brewery universe. Play as a mustachioed brewer in a chef’s hat and apron — beer mug perpetually raised — running through 8 worlds of cobblestone streets, hop gardens, malt caves, and fermentation factories.

## Gameplay

Move left and right with the D-pad, jump with the JUMP button (double-jump available), and throw beer bottles with the THROW button. Collect glowing hop cones for points, stomp enemies to defeat them, and reach the END flag to clear each zone. Fall into a pit and you lose a life. Collect 100 hop cones to earn a 1UP.

## Worlds & Zones

Each of the 8 worlds contains 4 zones. Zones 1–3 are standard platforming levels with increasing enemy count and speed, narrowing platform gaps, and more frequent pits. Zone 4 of every world is a boss fight in a dedicated arena.

|World|Name           |
|-----|---------------|
|1    |Grain Fields   |
|2    |Hop Gardens    |
|3    |Malt Caves     |
|4    |Yeast Swamps   |
|5    |Ferment Factory|
|6    |Ice Lager Peaks|
|7    |Barrel Fortress|
|8    |Grand Brewery  |

## Enemies

**Keg Roller** — a rolling metal keg with angry pixel eyes that chases the player. Stomp from above or hit with a thrown bottle to defeat.

**Foam Goblin** — a bubbly foam blob with a waddling walk cycle and blinking eyes. Same defeat conditions as the keg roller.

## Boss: The Brewmaster

Zone 4 of every world pits you against the Brewmaster — a large side-profile chef character in an oversized hat who charges toward you and hurls beer bottles in arcs. Hit him 3 times (via stomp or thrown bottle) to defeat him and advance to the next world. Bottles fall with gravity and splash on the ground or on contact. Throw speed and frequency increase in higher worlds.

## Power-Ups

**Bottle** (green glowing beer bottle) — adds 3 bottles to your throw inventory (max 5). Thrown bottles arc through the air, kill enemies on contact, and deal one hit to the boss.

**Star** (gold star) — 8 seconds of full invincibility with a cycling rainbow shimmer masked to the character’s exact outline. Enemies and projectiles cannot hurt you.

**Speed** (cyan lightning bolt) — 8 seconds of 1.85× movement speed with a blue afterimage trail.

## Controls

|Input                         |Action                             |
|------------------------------|-----------------------------------|
|D-pad left / right            |Move                               |
|Up D-pad / JUMP button / Space|Jump                               |
|Double-tap jump               |Double jump                        |
|THROW button / X key          |Throw bottle                       |
|Land on enemy head            |Stomp (kills enemy, bounces player)|

## Scoring

- +10 per hop cone collected
- +50 per enemy stomped
- +30 per enemy killed by thrown bottle
- +200 per zone cleared
- +500 per boss defeated
- +1 per 15 frames survived (automatic distance score)
- +1UP every 100 hop cones collected

## Tech

Single-file vanilla HTML/CSS/JS. No frameworks, no build steps, no external dependencies beyond Google Fonts (Press Start 2P). Canvas 2D at 800×450 logical resolution, CSS-scaled to fill the viewport. Fully iOS/Safari safe — ES5 patterns, no nested function declarations, no `document.createElement` canvas, no `localStorage`, no emoji in JS strings, no template literals.

The player character is drawn with bezier capsule limbs (no rectangles), a side-profile oval head with iris/pupil/catch-light eye, a curled mustache, and a tall chef hat. The star power shimmer uses `globalCompositeOperation: source-atop` on the main canvas to mask the cycling hue color to the character’s exact drawn outline.

## Part of AppADay

One complete web app built and shipped every day.
Portfolio: [augustineiacopelli.github.io/appaday](https://augustineiacopelli.github.io/appaday/)
