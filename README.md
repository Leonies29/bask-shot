# Bask-shot

A desk-basketball card game for parties, with a playable single-file web version.

Everyone shoots a mini basketball at the same time, following the rule on the card that was just flipped. The first player to score wins the card, and gives out shots to the others.

> **Adults only.** Drink at your own pace. Any shot can be swapped for water, and nobody drives afterwards.

## The cards

The deck has **20 cards**: 4 colors × 5 cards. Each color is one basketball team, and each card shows a player and a value from **1 to 5** in the top-right corner.

| Color  | Team     | Shooting rule                     |
| ------ | -------- | --------------------------------- |
| Red    | Bulls    | Shoot with your usual hand        |
| Blue   | Mavericks| Switch hands (non-usual hand)     |
| Green  | Celtics  | Shoot with one eye closed         |
| Yellow | Lakers   | Lob shot (arc the ball, like a bell) |

## How to play

1. Shuffle all the cards and put the pile in the middle, face down.
2. Flip the top card. Everyone shoots according to the card.
3. The **first player to score a basket wins the card** and keeps it.
4. The winner **gives out shots**: split them between the other players, or give them all to a single person.
5. Flip the next card and repeat until the pile is empty.

### Three ways to win

- **Most cards.** No points to count. Whoever won the most cards wins.
- **Most points.** Add up the values in the top-right corner of your cards. Highest total wins.
- **Points + bonus.** Same as above, but **owning all 5 cards of one color is worth +10 points**.

### Full set

If a player collects **all 5 cards of the same color** (the same team), **everyone else takes a shot**.

## Web version

`bask-shot.html` is a complete, playable version of the game in a single file.

### Features

- 2 to 8 players, with editable names
- The three winning modes above
- Shots per won card: **Free** (you count yourselves), **1 shot**, or **the card's value**
- Flip a card, tap who scored first, then split the shots with the + / − buttons
- Live scoreboard, including a per-color counter (for example 3/5 red) to track sets
- A bonus banner when someone completes a set of 5
- Fix a wrong winner without losing the round
- End screen with ranking, shots given and received, and tie detection
- Light and dark theme, following the device setting
- Settings (players, mode, shots) saved in the browser

### Run it

Open `bask-shot.html` in any modern browser. There is nothing to install and no build step.

The file is about 640 KB because all 21 card images (20 cards and the card back) are embedded as base64 WebP. The game works offline. The two web fonts (Alfa Slab One and Fredoka) load from Google Fonts, and without a connection the game falls back to standard system fonts.

### Host it

To put it online, for example on GitHub Pages:

1. Rename `bask-shot.html` to `index.html`.
2. Push it to a repository.
3. In the repository settings, enable GitHub Pages on the main branch.

## Customize

Everything is in the single file.

| What                         | Where                                                        |
| ---------------------------- | ------------------------------------------------------------ |
| Shooting rule for each color | `COL` (title and description) in the script                  |
| Mode names and descriptions  | `VERS` in the script                                         |
| Card images                  | `IMG`, keyed by color and value, for example `rouge3`, plus `dos` for the back |
| Colors                       | CSS variables `--y`, `--g`, `--b`, `--r` (yellow, green, blue, red) |
| Fonts                        | CSS variables `--display` and `--body`, and the Google Fonts `<link>` in the head |

Color keys in the code are French: `rouge` (red), `bleu` (blue), `vert` (green), `jaune` (yellow).

## Credits

Cards, rules and design by the game's author. The card artwork uses photos of basketball players and team logos, which belong to their respective owners. This is a personal, non-commercial party game.
