# Brainrot Blasters

A solo or two-player split-screen space runner in a single HTML file — no build step, no dependencies. Everything (art and music) is generated in code at runtime in a glossy, oversaturated "AI brainrot" style. The caption font, Anton, loads from Google Fonts, with Impact as the fallback.

**Play:** open `index.html` in a browser, click the game, pick **Single Player** or **1v1 Duel**.

| | Player 1 | Player 2 |
|---|---|---|
| Switch lane | A / D | ← / → |
| Jump | W | ↑ |
| Slide (fast-fall in the air) | S | ↓ |

In single player the arrow keys work too. `M` toggles sound (music, effects and spoken brainrot shouts). Touch: swipe or tap in your own half.

## How it plays
- Your blaster fires nonstop. Blast Tung Tung Tung Sahur, Ballerina Cappuccina, Cappuccino Assassino, Tralalero Tralala, Bombardino Crocodilo and Lirilì Larilà. Quick kills build a combo multiplier.
- Destroy rocks, `?` crates and bombs; dodge freighters; slide under red lasers. 4 hearts to start.
- **Route portals:** every planet (~25 s) ends with three portals. Each leads to a different planet with a modifier:
  - ⚔️ **Danger Zone**: more brainrots, +50% kill points (high risk, high score)
  - 🪙 **Gold Rush**: coins everywhere, more freighters (more attacks/nukes, faster skin unlocks)
  - 💚 **Chill Orbit**: fewer hazards, heal 1 heart (play it safe when you're low)
- **Upgrades:** after every portal, pick one of three cards (Firepower, Triple Espresso, Split Shot, Extra Heart, Coin Magnet, Combo Master, Lucky Crates, Moon Boots…). Duel adds competitive cards: Saboteur, Jammer, Coin Thief, Mirror Shield. Solo adds Second Wind.
- **Coins:** in a duel every 10 coins sends a brainrot squad at your rival; solo it triggers a Brainrot Nuke. Killing Lirilì Larilà jams your rival's blaster (solo: makes you invincible for 3 s).
- In a duel each player runs their own world (different start planet and layout).
- After the run you get a score summary; press **Continue** to return to the home screen.
- **Play as a brainrot:** pick your character on the home screen. Tung Tung Tung Sahur and Ballerina Cappuccina are free. Coins you collect are banked across runs (saved in your browser) and unlock Cappuccino Assassino (150), Tralalero Tralala (350), Bombardino Crocodilo (600) and Lirilì Larilà (1000).
- **Special ability:** each character has one. The round button at the bottom right charges from kills, coins and time; press **E** (P1 / solo) or **Enter** (P2), or click/tap the button, when it's full:
  - 🥁 Tung Tung Tung Sahur, **Sahur Storm**: sends 3 Tungs at your rival (solo: smashes everything ahead)
  - 🩰 Ballerina Cappuccina, **Pirouette**: 5 s invincible spin + shield
  - 🗡️ Cappuccino Assassino, **Shadow Strike**: kills every brainrot ahead + rapid fire
  - 🌊 Tralalero Tralala, **Trala Wave**: 8 s triple shot + coin magnet
  - 💣 Bombardino Crocodilo, **Carpet Bomb**: drops 5 bombs on your rival's track (solo: blows up everything ahead)
  - ⏰ Lirilì Larilà, **Time Freeze**: jams your rival's blaster for 4 s (solo: 4 s invincible)

## Performance notes
- Complex art (characters, scenery, items, portals) is drawn once into cached offscreen canvases and reused as images every frame; characters use 12-frame animation loops that are pre-built while the home screen is showing.
- The render resolution adapts automatically: it drops when frames take too long and climbs back when there's headroom.
