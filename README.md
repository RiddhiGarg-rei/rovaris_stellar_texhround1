# rovaris_stellar_texhround1
# Rovaris Run – Mars Sample Mission

A browser-based rover obstacle game built for **Task 3: Build an event-themed game**, based on the **Rovaris** event.

**Play online:** https://claude.ai/artifact/RpgQKLmELwuuUtfsTbCSez

## Concept and event theme

Rovaris is a rover-themed event, so the game puts you in control of a Mars rover on a science mission. The theme shapes the setting, the objective, and the core mechanic:

- **Setting:** a Martian surface with rocky mountains, craters, red dust, and the moon Phobos in the sky.
- **Objective:** a rover's mission is to gather samples while staying powered, so the game is built around collecting samples and managing battery.
- **Gameplay:** the rover drives automatically. You time jumps to clear terrain hazards and grab floating samples.

## Objective

Collect **15 samples** to complete the mission. The battery drains constantly, and the mission ends when it reaches 0%. After completing the mission you can keep driving to beat your best score.

## Controls

| Action | Keyboard | Touch / Mouse |
|---|---|---|
| Jump (hold for a higher jump) | `Space`, `↑`, or `W` | Tap / click the game screen |
| Start / Restart | `Enter` or `R` | Click the **Start / Restart** button, or tap after game over |
| Mute / unmute sound | `M` | Click the **Sound** button |

## Rules and hazards

| Element | Effect |
|---|---|
| Sample (cyan crystal) | +1 sample, +25 score, +10% battery |
| Rock | -25% battery on collision |
| Crater | -25% battery if you drive into it, so jump over it |
| Flying dust debris | -25% battery on collision |
| Time / distance | Battery drains continuously; speed increases the further you go |

After a hit the rover blinks and is briefly invulnerable.

## Feedback on progress and score

- **HUD:** live score, samples collected (x/15), best score, and a colour-coded battery bar (green, yellow, red).
- **Screen flash** and a **sound effect** on every hit or sample pickup.
- A **"Mission Complete"** banner appears at 15 samples.
- **End screen** shows score, samples collected, and best score.
- The **best score** is saved in the browser (`localStorage`) when available.

**Score formula:** `distance / 10 + 25 × samples`

## Restart / replay

Press `Enter` or `R` at any time, use the **Start / Restart** button, or tap/press jump on the game-over screen to start a new run instantly.

## How to run

**Option 1 – Online:** open the link above.

**Option 2 – Locally:**
1. Download `rovaris-run.html`.
2. Double-click it to open in any modern browser (Chrome, Edge, Firefox, Safari).
3. No installation, server, or internet connection is needed.

## Screenshots / demo

Add your screenshots or recording here:

- `screenshots/start.png` – start screen
- `screenshots/gameplay.png` – mid-game with HUD
- `screenshots/mission-complete.png` – end screen
- Demo video (optional): _link_

## Technology

- HTML5, CSS, and vanilla JavaScript in a single file
- HTML5 Canvas API for all rendering
- Web Audio API for generated sound effects

## Credits

- **Code, game design, and graphics:** original work, with no external libraries or frameworks.
- **Images:** none used. All visuals are drawn with Canvas shapes.
- **Audio:** no audio files. Sounds are synthesised in the browser with the Web Audio API.
- **Fonts:** default system fonts.
- **Event theme:** Rovaris.
