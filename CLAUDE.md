# Black Jack's BlackJack

**Code:** BBJ  
**Remote:** https://github.com/Lexxicc/CrackedJack.git  
**Version:** v0.0.6 (`Black Jack's BlackJack v0.0.6.html`)  
**Genre:** Card game / blackjack

## Tech
- DOM-based rendering (no canvas)
- Vanilla JS + Tailwind CSS via CDN
- Single-file HTML — no build step

## localStorage

- `BJ_stats` — player stats (ELO, match history)

## Colour palette
- `#0b1a10` — dark background
- `#152d1c` — felt green / panel
- `#c9952a` — primary gold
- `#e6b84d` — accent gold
- `#f7d76e` — glow
- `#4ade80` — hit button green
- `#f97316` — stand button orange

## Assets
- `Black Jack Black Playing BlackJack.png` — dealer character reference (J. Black)
- `BBJ-logo.svg` — logo / dealer avatar (placeholder, to be polished)

## Notes
- GitHub repo is named `CrackedJack` (original working title) — game is now Black Jack's BlackJack
- localStorage key migrated from `CrackedJack_stats` to `BJ_stats`
- Dealer character is J. Black — dark complexion, curly salt-and-pepper hair, burgundy bow tie, ornate waistcoat
- Game format: 3 hands per match, best-of-5 matches per series, ELO rating system
