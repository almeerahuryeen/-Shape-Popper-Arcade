<div align="center">

# 🎈 Shape Popper Arcade

### A colorful, browser-based shape-catching game built with HTML, CSS and JavaScript.

[![HTML5](https://img.shields.io/badge/HTML5-Canvas-E34F26?logo=html5&logoColor=white)](https://developer.mozilla.org/docs/Web/HTML)
[![CSS3](https://img.shields.io/badge/CSS3-Styling-1572B6?logo=css3&logoColor=white)](https://developer.mozilla.org/docs/Web/CSS)
[![JavaScript](https://img.shields.io/badge/JavaScript-Vanilla-F7DF1E?logo=javascript&logoColor=111)](https://developer.mozilla.org/docs/Web/JavaScript)
[![Platform](https://img.shields.io/badge/Platform-Web-brightgreen?logo=googlechrome&logoColor=white)](https://developer.mozilla.org/docs/Web)
[![No Build Required](https://img.shields.io/badge/Build-Not%20Required-success)](#getting-started)

**Choose a mode, pop the shapes, beat your score — and watch out for bombs!**

</div>

---

## 📖 About

**Shape Popper Arcade** is a lightweight arcade game that runs directly in a modern web browser. Shapes fall from the top of the play area, and players interact with them using a mouse or touch screen.

The game includes three play modes, selectable visual themes, adjustable starting speed, sound effects, score tracking and a pause menu. The interface and gameplay are rendered using a single HTML page and the HTML5 Canvas API.

## ✨ Features

- **Three game modes**
  - 🎯 **Match Challenge** — pop only the shape that matches the target color and shape. Incorrect pops and missed target shapes cost a life. The round starts with three lives.
  - 💥 **Free Pop** — pop shapes to build your score while avoiding black bombs. Hitting a bomb reduces the score by five points.
  - ⚔️ **1v1 Turn-Based** — two players take timed turns; the player with the higher score wins.
- **Three themes** — Space Exploration, Candy Kingdom and Deep Ocean.
- **Adjustable starting speed** — choose a starting speed from the settings screen.
- **Sound controls** — enable or mute generated game sound effects.
- **Mouse and touch input** — play on desktop and touch-enabled devices.
- **Pause and resume** — pause the game, reset the current score or return to the main menu.
- **Canvas animation** — falling shapes and the game HUD are drawn dynamically.
- **Responsive game area** — the canvas adapts to its displayed size.
## 🕹️ Screenshots

The screenshots below are included in [`assets/screenshots/`](assets/screenshots/).

| Main menu | Theme selection |
|:---:|:---:|
| <img src="assets/screenshots/01-main-menu.png?raw=true" alt="Main menu" width="350"> | <img src="assets/screenshots/02-theme-selection.png?raw=true" alt="Theme selection" width="350"> |

| Match Challenge | Free Pop |
|:---:|:---:|
| <img src="assets/screenshots/03-match-challenge-gameplay.png?raw=true" alt="Match Challenge gameplay" width="350"> | <img src="assets/screenshots/04-free-pop-gameplay.png?raw=true" alt="Free Pop gameplay" width="350"> |

| 1v1 gameplay | Match result |
|:---:|:---:|
| <img src="assets/screenshots/05-versus-gameplay.png?raw=true" alt="Versus gameplay" width="350"> | <img src="assets/screenshots/06-versus-result-tie.png?raw=true" alt="Versus tie result" width="350"> |

<div align="center">

**Game Over screen**

<img src="assets/screenshots/07-game-over-screen.png?raw=true" alt="Game Over screen" width="350">

</div>


## 🚀 Getting Started

### Requirements

- A modern browser such as Google Chrome, Microsoft Edge, Firefox or Safari.
- No package installation, build tools, server or database is required.

### Run locally

1. Download or clone this repository.
   ```bash
   git clone https://github.com/YOUR-USERNAME/shape-popper-arcade.git
   ```
2. Open the project folder.
   ```bash
   cd shape-popper-arcade
   ```
3. Open `index.html` in your browser.

You can also double-click `index.html` from your file manager. The game is a standalone front-end project.

## 🎮 How to Play

1. On the main menu, choose a theme, starting speed and sound setting.
2. Select one of the three game modes.
3. Click or tap a falling shape to pop it.
4. In **Match Challenge**, check the target shown in the top bar before popping.
5. In **Free Pop** and **1v1**, avoid black bombs.
6. Use the pause control in the top-right corner to pause the game.

### Mode rules

| Mode | Goal | Scoring / penalties |
|---|---|---|
| Match Challenge | Match both the target color and shape | Correct match: +1. Incorrect pop or missed target: lose 1 life. Starts with 3 lives. |
| Free Pop | Pop shapes and avoid bombs | Shape: +1. Bomb: −5 points (score cannot go below 0). |
| 1v1 Turn-Based | Earn more points than the other player | Each player gets a 10-second turn. Bomb: −5 points for the current player (score cannot go below 0). |

## 🧰 Built With

| Technology | Purpose |
|---|---|
| **HTML5** | Page structure and game canvas |
| **CSS3** | Layout, menus, buttons, themes and visual styling |
| **JavaScript (Vanilla)** | Game state, input handling, scoring, spawning and animation |
| **Canvas 2D API** | Drawing shapes, bombs and the in-game HUD |
| **Web Audio API** | Programmatically generated pop, incorrect-action and bomb sounds |
| **Vibration API** | Optional device vibration when the game ends, where supported |

## 📁 Project Structure

```text
shape-popper-arcade/
├── index.html
├── README.md
└── assets/
    └── screenshots/
        ├── 01-main-menu.png
        ├── 02-theme-selection.png
        ├── 03-match-challenge-gameplay.png
        ├── 04-free-pop-gameplay.png
        ├── 05-versus-gameplay.png
        ├── 06-versus-result-tie.png
        └── 07-game-over-screen.png
```

## 🧩 Implementation Overview

- **Game state:** JavaScript variables track the current screen, selected mode, score, lives, theme, falling items and player turns.
- **Game loop:** `requestAnimationFrame()` repeatedly updates the game while it is in the playing state.
- **Shape generation:** items are spawned at random horizontal positions with randomized sizes, colors, shapes and falling speeds.
- **Collision/input handling:** mouse and touch events are converted to canvas coordinates and checked against falling items.
- **Theme configuration:** a theme map supplies the background and target label for each available theme.
- **Audio:** Web Audio oscillators generate short sound effects without external audio files.

## ⚙️ Customization

The main settings are available on the start screen:

- **Game Theme:** Space Exploration, Candy Kingdom or Deep Ocean.
- **Initial Speed:** range from `1` to `5`, with half-step increments.
- **Game Sound:** Enabled or Muted.

The source is contained in `index.html`, so you can customize colors, shape behavior, spawn frequency, scoring and interface styling directly.

## 🌱 Possible Future Improvements

- Add persistent high scores using browser storage.
- Add difficulty progression and additional levels.
- Add keyboard controls and accessibility improvements.
- Add more shapes, power-ups and sound options.
- Improve turn transitions with an in-game countdown instead of a browser alert.
- Add automated gameplay tests and a dedicated mobile layout.

## 🤝 Contributing

Contributions and suggestions are welcome.

1. Fork the repository.
2. Create a feature branch: `git checkout -b feature/your-feature`.
3. Commit your changes: `git commit -m "Add your feature"`.
4. Push the branch and open a Pull Request.

## 📄 License

No license file is included in this repository kit. Add a `LICENSE` file if you want to publish the project under a specific open-source license.

---

<div align="center">

**Made for fun. Built for the browser. 🎈**

If you enjoy the game, consider giving the repository a ⭐.

</div>
