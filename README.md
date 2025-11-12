# Treasure Map Adventure

Treasure Map Adventure is a browser-based coding playground designed to teach **computational thinking**. Students break problems into commands, reason about control flow, and debug logic as they steer an explorer across grid-based maps using simple pseudo-code (MOVE, TURN LEFT, REPEAT, IF/ELSE, WHILE, etc.). They refine one algorithm, then run or step through it to watch the avatar reach the treasure while avoiding obstacles.

The project now includes two distinct modes:

- **Practice Mode** – open map editing, adjustable speed/grid size, manual controls, and a live run log.
- **Challenge Mode** – a four-level gauntlet where students must write one algorithm that succeeds on every fixed map. Scores (fewest total steps) are stored locally in a Hall of Fame leaderboard for friendly competition.

The UI is styled in a neo-brutalist theme with bold outlines, chunky buttons, and playful copy surfaced through the run log and footer credits (crafted by ATLverse).

## Features

- **Algorithm editor** supporting MOVE, TURN LEFT/RIGHT, PICK TREASURE, nested REPEAT blocks, IF/ELSE conditionals (PATH AHEAD CLEAR/BLOCKED, ON TREASURE, with optional NOT), and WHILE loops.
- **Stepper & autoplay** controls with adjustable speed slider; errors pause execution with log messages.
- **Map builder** (Practice mode) to place/remove obstacles, move the start or treasure, or randomize layouts.
- **Challenge workflow** that locks the 4 curated maps, requires a student name, and runs the same AST on each level, capturing total steps for the Hall of Fame.
- **Persisted data** (localStorage) for player names, saved algorithms between sessions, and leaderboard entries.
- **Accessibility niceties** like keyboard shortcuts (Ctrl/Cmd + Enter to run, F8 to step) and detailed log output for each command.

## Getting Started

1. Open `games.html` in any modern browser.
2. Enter a player name (required for both practice runs and challenge attempts).
3. Compose your algorithm in the text area using one command per line.
4. Choose **Practice** to freely edit the map or **Challenge** to tackle the fixed levels.

## Practice Mode Tips

- Use the Run/Step controls on the right-hand “Session Control” panel.
- Adjust `Speed` to slow down or speed up animations.
- Modify the grid or place obstacles/treasure/start points with the Map Builder buttons.
- The log beneath the map captures every command, evaluation, and hint—use it to debug.

## Challenge Mode Tips

- Your editor becomes read-only once the challenge starts, ensuring one consistent algorithm.
- The Run/Step buttons disable automatically while the multi-map run is underway.
- Completing all four levels records your total steps in the Hall of Fame (top 10 stored locally).
- Need to bail out? Use Reset; the original practice map snapshot will be restored afterward.

## Customization

- To tweak the challenge levels, edit the `challengeLevels` array near the top of `games.html`. Each entry defines grid size, start/treasure coordinates, and obstacle coordinates.
- Styling lives in the `<style>` block inside `games.html`. The key CSS variables (`--bg`, `--accent`, etc.) drive the neo-brutalist palette if you want to re-theme the experience.

Enjoy guiding students toward algorithmic thinking—one treasure hunt at a time!  
_“Brought to life with a lot of heart by ATLverse (atlverse.xyz).”_
