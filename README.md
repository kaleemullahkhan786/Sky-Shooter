# Sky Shooter (HTML5 Canvas)

A fast-paced, modern 2D arcade sky shooter built with vanilla HTML/CSS/JS and Canvas. Smooth controls, parallax background, enemy waves, power-ups, achievements, and a local leaderboard — in a single lightweight project.

## ✨ Features
- Smooth WASD/Arrow movement and auto-fire
- Responsive canvas (desktop + mobile) with DPR scaling
- Parallax stars + soft drifting clouds
- Enemy waves with increasing difficulty and types
- Power-ups: Shield, Double-Fire, Speed Boost, Extra Life
- Score, lives, health bar, local high score, and local leaderboard (top 10)
- Achievements (saved locally) + session badges on Game Over
- Menus: Start, Pause, Game Over (keyboard + touch friendly)
- Particle explosions and glowing visuals
- Persistent JSON save for score (survives refresh/next session)

## 🎮 Controls
- Move: WASD or Arrow Keys
- Shoot: Auto-fire (Space also triggers)
- Pause/Resume: P
- Mobile: Drag to move, tap to shoot

## 🧰 Tech Stack
- HTML5 Canvas, Vanilla JavaScript
- CSS3 UI
- LocalStorage for scores, leaderboard, achievements, and save JSON

## 🚀 Getting Started
1. Clone or download the repository.
2. Open `index.html` in a modern browser (Chrome/Edge/Firefox/Safari).
   - Recommended: serve locally for best performance.

Quick servers:
- Python 3: `python -m http.server 8080`
- Node: `npx serve`
- VS Code: Live Server

Open: `http://localhost:8080`

## 📦 Project Structure
```
sky shooter/
├─ index.html
├─ styles.css
└─ src/
   └─ game.js
```

## 🗄️ Persistence (Local JSON Save)
- Current score is saved under key `skyshooter:save`:
  ```json
  { "score": 12345 }
  ```
- High score: `skyshooter:highScore`
- Leaderboard: `skyshooter:leaderboard`
- Achievements: `skyshooter:achievements`
- Player name: `skyshooter:playerName`

Reset via DevTools console:
```js
localStorage.removeItem('skyshooter:save');
localStorage.removeItem('skyshooter:highScore');
localStorage.removeItem('skyshooter:leaderboard');
localStorage.removeItem('skyshooter:achievements');
localStorage.removeItem('skyshooter:playerName');
```

## 🛠️ Customization
- Visuals: `styles.css` (colors, fonts, HUD, menus)
- Difficulty: `src/game.js` (waves, speeds, HP)
- Auto-fire rate: `player.fireCooldownMs`
- Add enemies/power-ups in `game.js`


Have fun and happy shooting! 🔥

