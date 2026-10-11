# SLAP SUMMIT

A tiny, absurd, mobile-friendly browser game where you slap fifteen completely fictional, over-the-top caricatures of world leaders and tech tycoons until they have zero dignity left.

Single HTML file. No build step, no dependencies, no frameworks. Open `index.html` and play.

> **Parody disclaimer.** Every character is an invented cartoon. Any resemblance to real people is a coincidence we are very proud of. No actual people were slapped.

## Play

- **Desktop:** click on the victim to slap, or hold and drag across the screen to swipe-slap.
- **Mobile:** tap or swipe on the victim. Vibration feedback is used where the device supports it.
- **Sound:** every weapon has its own synthesized sound (Web Audio API, no audio files). Use the speaker button to mute.

## Game modes

| Mode | What it is |
| --- | --- |
| **Classic** | Pick a victim and slap until their dignity hits zero. Meme K.O. animation, stamp, confetti and a share card. |
| **Rush 45s** | 45 seconds on the clock, the timer starts on your first slap, every K.O. adds 6 seconds. Humble all 15 dignitaries to clear the summit, get a bonus and land on the leaderboard. |
| **Endless** | Pick one victim and slap nonstop. Every 100 slaps he is knocked out and you get a 5 second break. Finish whenever your arm gives up. |

## Features

- 15 original parody characters, drawn procedurally as SVG (no image assets)
- 12 weapons unlocked by your total slap count
- Combos, critical slaps, and a "2x TODAY" victim that changes every day
- 14 trophies
- Nickname entry and a leaderboard
- Share to X (Twitter) with a pre-written multi-line post
- Progress is saved in `localStorage`
- Light and dark theme, reduced-motion friendly

## Weapons

| Weapon | Unlocks at (total slaps) | Bonus |
| --- | --- | --- |
| Open Hand | 0 | The classic |
| Slipper | 20 | +25% damage |
| Wet Fish | 60 | +20% points |
| Baguette | 120 | +50% damage |
| Rubber Chicken | 250 | +50% points |
| Frying Pan | 400 | 2.2x damage |
| Boxing Glove | 600 | 1.8x damage |
| Smelly Sock | 800 | +40% points |
| Cheese Wheel | 1100 | 1.6x damage, +20% points |
| Rubber Duck | 1500 | +70% points |
| Angry Octopus | 2200 | 1.4x damage, +50% points |
| Giant Pizza | 3000 | 2.5x damage |

## Run it locally

Just double-click `index.html`, or serve the folder with any static server:

```bash
python3 -m http.server 8000
# open http://localhost:8000
```

## Deploy on GitHub Pages

1. Create a repository and upload `index.html` and this `README.md` to the root.
2. Go to **Settings, Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**, select `main` and `/ (root)`, and save.
4. After a minute your game is live at `https://<your-username>.github.io/<repo-name>/`.

## Configuration

Open `index.html` and search for these spots near the top of the `<script>`:

- `SHARE_URL`: put your public game link here (for example your GitHub Pages URL). It is then appended automatically to the "Post on X" text and the "Copy text" button. Leave it empty to share text only.
- `C` (the characters array): change names, titles, colors, quotes and accessories, or add more characters.
- `W` (the weapons array): change damage, point multipliers, unlock thresholds and pop-up words.
- `TROPHIES`: add or edit trophies.

## Leaderboard note

The game was built to run inside Claude artifacts, where the "Crew" leaderboard is stored in a shared database that only people with access to the artifact can use.

On GitHub Pages that shared database does not exist, so:

- The **My runs** tab (best runs on the current device, kept in `localStorage`) works everywhere.
- The **Crew** tab shows a note that the shared board is unavailable.

If you want a real global leaderboard on GitHub Pages, connect your own backend (Firebase, Supabase, or similar). The only places to change are the `initCloud()` and `submitScore()` functions in `index.html`: read the top scores in `initCloud()` into the `board` array, and write a cleared Rush run in `submitScore()`.

## Tech notes

- Plain HTML, CSS and JavaScript in one file
- SVG faces generated from a small character config
- Web Audio API for all sound effects
- Google Fonts (Bangers, Rubik) with system fallbacks, so the game still works offline
- Pointer events for unified mouse and touch input

## License

Add the license of your choice (MIT is a good default for a project like this).
