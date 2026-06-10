# 🎰 Lucky Spin

A fun, mobile-first slot machine game — virtual coins only, no real money involved.

## Play it

Open `index.html` in any browser (it's a single self-contained file, no build step or
dependencies), or serve it locally:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

For the best experience, open it on your phone and add it to your home screen.

## Features

- 🎡 **3-reel slot machine** with smooth, staggered spin animations
- 🪙 **Virtual coin economy** — start with 1,000 coins, balance saved between sessions
- 💰 **Adjustable bets** — 10 / 25 / 50 / 100 / 250 coins per spin
- 🃏 **Double-or-nothing Hi-Lo** — after any win, gamble it on a card guess up to 5 times
- 💥 **Jackpot** — triple 7s pays 100× your bet with a coin-rain celebration
- 🔊 **Sound effects** generated with WebAudio (no asset files)
- 📳 **Haptic feedback** on supported phones
- 🎁 **Free top-up** when you go broke, so the fun never stops

## Paytable

| Combo | Payout |
|---|---|
| 7️⃣ 7️⃣ 7️⃣ | ×100 |
| 💎 💎 💎 | ×40 |
| ⭐ ⭐ ⭐ | ×25 |
| 🔔 🔔 🔔 | ×15 |
| 🍀 🍀 🍀 | ×10 |
| 🍋 🍋 🍋 | ×8 |
| 🍒 🍒 🍒 | ×6 |
| 🍒 🍒 any | ×2 |
