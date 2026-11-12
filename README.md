# 🕹️ Kira's Arcade

A collection of mobile-first browser games: four party games you play together on your phones, and six arcade games for playing solo. Every game is a single self-contained HTML file. There's no build step and nothing to install.

## Play it

Open `index.html` in a browser to get the arcade hub, which links to every game. To serve it locally:

```bash
python3 -m http.server 8000
```

Then visit <http://localhost:8000>. The games are made for phones: open the hub on your phone and add it to your home screen.

## 🎉 Party games

Play these with friends in the same room. One phone hosts a game and gets a room code, and everyone else joins by typing that code on their own phone.

| Game | Players | What it is |
|---|---|---|
| 🕵️ **Mafia** (`mafia.html`) | 4–12 | Secret roles, night kills and lying to your friends. |
| ⚡ **Reflex Royale** (`reflex.html`) | 2–8 | 8 quick mini-rounds with a live leaderboard. The fastest fingers win. |
| 🎨 **Sketch & Guess** (`sketch.html`) | 2–8 | One player draws live and everyone races to guess the word. Available in English and Arabic. |
| 🎭 **Al-Fakh (الفخّ)** (`trivia.html`) | 3–8 | Bluffing trivia in Arabic. Write fake answers to fool your friends, then try to spot the real one. |

## 🕹️ Arcade games

Solo games. Each run adds coins to your wallet, and your best scores are saved on your device.

| Game | What it is |
|---|---|
| 🍬 **Candy Smash** (`candy.html`) | Match-3 with striped candies and color bombs. |
| 🏗️ **Sky Stack** (`stack.html`) | One-tap tower stacking. Chase PERFECT drops. |
| 🐦 **Glow Bird** (`bird.html`) | Flap through neon gates. |
| ⚡ **2048** (`2048.html`) | Swipe and merge tiles to reach 2048. |
| 🐍 **Neon Snake** (`snake.html`) | Eat orbs and grow long without biting yourself. |
| 🧱 **Brick Blast** (`breaker.html`) | Breakout: smash every brick and catch the falling perks. |

## How it works

- **Single-file games:** each game's HTML, CSS and JavaScript live in one `.html` file. Sound effects and music are generated with the Web Audio API, so there are no asset files.
- **Multiplayer:** the party games connect phones directly to each other over WebRTC using [PeerJS](https://peerjs.com/), loaded from a CDN. The host's phone runs the game, and there's no game server.
- **Saved progress:** coins and high scores are stored in the browser's `localStorage`. Nothing leaves your device.

## Deployment

GitHub Pages serves the live site from the `gh-pages` branch. To publish a change, merge it into the `claude/mobile-gambling-game-ka501a` branch and then into `gh-pages`. Pages rebuilds the site a minute or so after each push to `gh-pages`.

The workflow in `.github/workflows/pages.yml` isn't what publishes the site, and its runs fail.

## Project structure

```
index.html        Arcade hub: lists every game and shows your coin wallet
mafia.html        Party: Mafia
reflex.html       Party: Reflex Royale
sketch.html       Party: Sketch & Guess
trivia.html       Party: Al-Fakh (الفخّ)
candy.html        Arcade: Candy Smash
stack.html        Arcade: Sky Stack
bird.html         Arcade: Glow Bird
2048.html         Arcade: 2048
snake.html        Arcade: Neon Snake
breaker.html      Arcade: Brick Blast
.github/workflows/pages.yml   Unused Pages workflow (the site is served from gh-pages)
```
