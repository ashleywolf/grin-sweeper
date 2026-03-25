# :grinning: Grin Sweeper

Minesweeper, but you reveal tiles by smiling at your webcam. Hit a mine and your panicked grin gets screenshotted forever.

## [Play Now](https://ashleywolf.github.io/grin-sweeper/) (Chrome/Edge)

## What Is This

Classic minesweeper with a physical twist: smile to reveal tiles, smile wider to reveal more. The AI reads your face through 52 blendshapes, so a nervous half-smile reveals one tile while a full cheese clears a whole area. Hit a mine and the game captures your face at the exact moment of regret.

## Features

- Smile-controlled tile reveal with intensity scaling (bigger smile = bigger area)
- Normal, Hard, and Expert difficulty with separate leaderboards
- Shame screenshot when you hit a mine, victory trophy screenshot when you win
- 4-frame blendshape smoothing so twitchy smiles don't misfire
- Last-10-tiles heartbeat tension mode that raises the stakes
- Recalibrate button for different lighting or if you have resting smile face
- Ambient drone audio that shifts with danger proximity
- Screen shake on mine hit because you earned it
- localStorage records tracked per difficulty level

## How to Play

- Hover your mouse over a tile, then smile to reveal it.
- Wider smile = more tiles revealed at once. Subtle smirk = cautious single-tile reveal.
- Right-click to flag suspected mines.
- Clear the board without hitting 3 mines to win.

## Tech

- MediaPipe FaceLandmarker running in-browser via CDN
- 52 facial blendshapes tracked in real-time (key: mouthSmileLeft, mouthSmileRight)
- 4-frame temporal smoothing for stable detection
- HTML5 Canvas rendering with webcam overlay

## Browser Support

Chrome or Edge recommended. Requires webcam access. Good lighting helps with smile detection accuracy.

## Part of Browser Party Games

8 single-file browser games built with MediaPipe, Transformers.js, Web Audio, and Web Speech. No servers, no build steps, no installs.

| Game | Input | Tech |
|------|-------|------|
| [Type or Die](https://ashleywolf.github.io/type-or-die/) | Keyboard | Vanilla JS |
| [Grin Sweeper](https://ashleywolf.github.io/grin-sweeper/) | Smile (webcam) | MediaPipe Face |
| [Show & Tell](https://ashleywolf.github.io/show-and-tell/) | Real objects (webcam) | Transformers.js DETR |
| [Pitch Climber](https://ashleywolf.github.io/pitch-climber/) | Voice pitch (mic) | Web Audio API |
| [Spell Caster](https://ashleywolf.github.io/spell-caster/) | Shout spells (mic) | Web Speech API |
| [Stone Face](https://ashleywolf.github.io/stone-face/) | Don't react (webcam) | MediaPipe Face |
| [Ninja Hands](https://ashleywolf.github.io/ninja-hands/) | Hand tracking (webcam) | MediaPipe Hands |
| [Duck & Cover](https://ashleywolf.github.io/duck-and-cover/) | Duck + yell (webcam+mic) | MediaPipe Pose + Web Audio |

---
Built with vanilla JS + browser ML. Each game is one HTML file. Fork it, break it, make it yours.
