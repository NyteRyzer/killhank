# Kill Hank

Kill Hank is a dark-comedy incremental (clicker) game. You're the lead researcher at a black-site lab. Your test subject, Hank, is strapped to a steel table and has a healing factor you can't beat. Hurt him, harvest his DNA, and spend it on worse hardware.

## Play

The whole game is one file, `index.html`, with no build step. You can:

- open `index.html` in any modern browser, or
- serve the folder with a static server (`python3 -m http.server`) or turn on GitHub Pages.

Your progress saves in the browser's local storage. Gadgets keep harvesting at half speed while you're away, for up to 8 hours.

## Core rules (from the game bible)

| Rule | Value |
| --- | --- |
| Hank's base health | 100 HP |
| Regeneration | +2% of max HP every second |
| On death (0 HP) | DNA payout equal to the max HP you just destroyed, then he revives with ×1.5 max HP |
| DNA | 1 DNA for every point of damage dealt |
| Shop prices | ×1.15 per level owned |

## Systems

- **Weapons (click damage):** Bare Fists, Spiked Bat, Chainsaw, Plasma Scalpel and Particle Cannon from the bible. Gravity Hammer, Antimatter Lance and Singularity Gauntlet come later.
- **Gadgets (automatic DPS):** Auto-Puncher, Tesla Coil, Acid Drip, Laser Grid and Orbital Strike from the bible. Nanite Swarm, Black Hole Generator and Time Loop Chamber come later.
- **Milestones:** each item doubles its output at levels 25, 50, 100, 150, 200, 300 and 400.
- **Research:** one-time projects that unlock as you play. Each item has two upgrades (×2, then ×3). There are also lab-wide projects, such as faster supply drones, a higher combo cap, Cauterization (Scalpel hits halve his regen) and Gene Splicers (+25% DNA).
- **Combat:**
  - **Combos:** each fast click in a row adds 1% damage, up to ×2 (×3 with research).
  - **Crits:** 5% chance for ×5 damage.
  - **Weak spot:** a glowing reticle that moves around his body. Hitting it deals ×10 damage (×20 with research).
- **Abilities (keys 1–4):**
  - Adrenaline: clicks ×5.
  - Cryo Freeze: stops his regeneration.
  - Overcharge: gadgets ×4.
  - Gene Harvest: DNA ×3.
- **Random events:**
  - **Supply drones:** fly across the lab. Click one for a DNA cache, Frenzy (clicks ×7) or Overclock (gadgets ×7).
  - **Escape attempts:** Hank strains against a restraint. Click it in time to earn hazard pay. If you miss it, he punches the camera, fully heals and doubles his regen for 20 seconds.
  - **Mutations:** every 10th life Hank comes back mutated (Iron Skin, Hyper-Regen, Dead Nerves or Swollen Mass) and pays out ×5 when you kill him.
- **Clone Protocol (prestige):** reset your run for Mutagen. Each point adds +10% to all damage, permanently.
- **Achievements:** 38 in total, each worth +2% damage.
- **Hank evolves:** he grows bone claws at 20 kills, glowing eyes at 50 and glowing veins at 75.
- **Lab Director hints** guide new players.

All the tuning numbers are constants at the top of the script in `index.html`, so you can rebalance the game there.
