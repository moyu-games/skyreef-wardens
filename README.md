# 英雄亂鬥：雲礁之戰

**English** · [繁體中文](README.zh-TW.md)

A real-time card tower-defense game that runs entirely in the browser. Build an eight-card deck, deploy troops and heroes onto a floating sky-reef arena, and knock down the enemy towers before the clock runs out.

**Play now: <https://moyu-games.github.io/skyreef-wardens/>**

No install and no account needed. Progress is saved in your browser.

---

## Features

**Battles**
- Three-minute matches on a two-lane arena with two side towers and a main tower for each player.
- Troops, heroes and spells with their own animations, hit effects and sound.
- Double energy in the last minute, with a big countdown over the final ten seconds.
- Practice against computer opponents with several play styles.

**Two-player mode**
- Create a room and share the code or link (`?room=CODE`) to play a friend in real time.
- Stickers and quick taunts during a match.

**Progression**
- Card collection, upgrades and trophies.
- Chests, a free chest every four hours and a daily shop.
- Daily login rewards and daily quests.
- Three deck slots.

**Interface**
- Designed for phones in portrait, and also playable on desktop.
- A first-match tutorial, sound and vibration toggles, and a power-saving effects mode.

---

## How it works

The whole game is a single static `index.html` served by GitHub Pages. Graphics are drawn on a canvas and sound effects are synthesized with the Web Audio API, so there are no image or audio files to download.

Two-player matches are relayed through public MQTT brokers. Room traffic is not encrypted, so anyone who knows a room code could read it; the game never sends personal data, only moves and stickers.

The page checks `version.txt` and reloads itself when a new version is published, but never in the middle of a battle.

## Credits

Some card art uses photos from Wikimedia Commons under CC0, CC BY, CC BY-SA or public-domain terms. The in-game credits list each photo and its author.
