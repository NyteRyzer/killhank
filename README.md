# Kill Hank

Kill Hank is a dark-comedy incremental (clicker) game. You're the lead researcher at a black-site lab. Your test subject, Hank, is strapped to a steel table and has a healing factor you can't beat. Hurt him, harvest his DNA, and spend it on worse hardware.

## Play

The whole game is one file, `index.html`, with no build step. You can:

- open `index.html` in any modern browser, or
- serve the folder with a static server (`python3 -m http.server`) or turn on GitHub Pages.

Your progress saves in the browser's local storage. Gadgets keep harvesting at half speed while you're away, for up to 8 hours.

## How it plays (from the game bible)

| Rule | Value |
| --- | --- |
| Hank's base health | 100 HP |
| Regeneration | +2% of max HP every second |
| On death (0 HP) | DNA payout equal to the max HP you just destroyed, then he revives with ×1.5 max HP |
| DNA | 1 DNA for every point of damage dealt |
| Shop prices | ×1.15 per level owned |

**Weapons (click damage):** Bare Fists (1), Spiked Bat (5), Chainsaw (25), Plasma Scalpel (150), Particle Cannon (1,000).

**Gadgets (automatic DPS):** Auto-Puncher (2/s), Tesla Coil (10/s), Acid Drip (50/s), Laser Grid (500/s), Orbital Strike (15,000/s).

If your total damage falls below Hank's regeneration, he out-heals you. Idle and save up, or click harder, until you can afford the next upgrade.

## Features

- Top-down security-camera view of the lab, drawn procedurally on a canvas
- Robotic arms that swing your best weapon at wherever you click
- A visible animation for every gadget: piston punches, tesla arcs, acid drips, sweeping lasers and orbital strikes
- Wounds that build up as his HP drops and fade as he heals
- Health bar with a live ECG monitor, an incident log, and Hank's running commentary
- x1 / x10 / MAX bulk buying, with new items unlocking as you earn DNA
- Optional synthesized sound effects
- Works on phones: the layout stacks into one column

All the tuning numbers are constants at the top of the script in `index.html`, so you can rebalance the game there.
