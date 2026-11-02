# Rovaris Rover Run

A side-scrolling rover obstacle course game built for **Task 3: Build an event-themed game**, inspired by the **Rovaris** rover theme.

**Author:** _Your Name_ · _Reg. No._ · VIT

---

## Objective

Drive your rover across the Martian surface to the **base camp** at the end of each sector. Keep your **hull** intact and your **battery** charged, and collect crystal samples for extra points.

## How the Rovaris theme shapes the gameplay

- **Setting:** a Martian terrain with craters, rocks and a distant base camp.
- **Rover mechanics:** the rover drives with momentum, and jumps in low-gravity style.
- **Resource management:** the battery drains faster the faster you drive, so you must plan your speed and reach solar stations in time.
- **Exploration:** collecting crystal samples rewards risky jumps.

## Controls

| Action | Keyboard | Touch |
|---|---|---|
| Drive forward | `→` or `D` | ▶ button |
| Reverse | `←` or `A` | ◀ button |
| Jump | `Space`, `↑` or `W` | ⤒ button |
| Restart sector | `R` | – |
| Start / next sector / retry | `Space`, `Enter` or the on-screen button | tap button |

## Rules and scoring

| Element | Effect |
|---|---|
| Rock | Hit it: −1 hull and a knock-back. Jump over it. |
| Crater | Fall in: −1 hull and you are moved back. Jump across it with enough speed. |
| Crystal sample (cyan) | +50 points |
| Solar station (⚡) | +35% battery, +25 points |
| Reaching base camp | Bonus for remaining battery, remaining hull and speed |

**You lose** when the hull reaches 0 or the battery runs out and the rover stops.
**You win a sector** by reaching the base camp. Each next sector is longer, faster and has more craters.

## Feedback shown on screen

- Score, sector number, hull hearts, battery bar, samples collected and best score
- A progress bar showing the distance to the base
- Pop-up messages for pickups and crashes, plus dust, screen shake and sound effects
- A results screen after each sector, with **Next sector** or **Retry**
- The best score is saved in the browser (localStorage)

## How to run

**No installation or internet is needed.**

1. Download or copy the project folder.
2. Double-click `rovaris-rover.html` (or `index.html` if you renamed it). It opens in Chrome, Edge or Firefox.
3. Click **Launch** (or press `Space`) and start driving.

**Optional (VS Code):** open the folder in VS Code, install the *Live Server* extension, right-click the HTML file and choose *Open with Live Server*.

## Project structure

```
rovaris-rover.html   – the complete game (HTML, CSS and JavaScript)
README.md            – this file
screenshots/         – gameplay screenshots
```

## Screenshots

| Start screen | Gameplay | Result screen |
|---|---|---|
| ![Start](screenshots/start.png) | ![Gameplay](screenshots/gameplay.png) | ![Result](screenshots/result.png) |

_Demo video (optional): add a link or file name here._

## Technical notes

- Built with plain **HTML, CSS and JavaScript**, with graphics drawn on an HTML5 `<canvas>`.
- The game runs in a `requestAnimationFrame` loop with separate update and draw steps.
- The course is generated from a seed for each sector, so a sector is the same every time you retry it.
- Collisions use simple rectangle and range checks.
- The screen layout adapts to the window size, and there are touch controls for phones.

## Credits

- **Libraries:** none. No external libraries or frameworks were used.
- **Graphics:** all drawn in code with the Canvas API. No image files.
- **Audio:** sound effects are generated in code with the Web Audio API. No audio files.
- **Fonts:** system fonts only.
- **Development:** vibecoding

## Possible future improvements

- A 3D version using Three.js
- More obstacle types (sandstorms, moving hazards)
- Sound toggle and a pause button
- An online leaderboard
