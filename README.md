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

