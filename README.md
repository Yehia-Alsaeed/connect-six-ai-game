# Connect Six AI Game

Connect Six AI Game is a Python notebook project that implements a playable Connect6 board game with a Pygame interface and heuristic AI opponents. The project was built for a Logic and AI course and demonstrates game-state modeling, rule enforcement, heuristic evaluation, minimax search, alpha-beta pruning, and interactive gameplay.

Connect6 is a strategy board game similar to Gomoku. Black places one stone on the first move, then players alternate by placing two stones per turn. The first player to connect six stones horizontally, vertically, or diagonally wins.

## Features

- Full Connect6 rule handling, including the one-stone opening move and two-stone turns afterward.
- Configurable board sizes: 19x19, 15x15, 13x13, and 9x9.
- Human vs human mode.
- Human vs AI mode with AI assigned as either black or white.
- Basic and advanced heuristic options.
- Minimax search with alpha-beta pruning.
- Smart move ordering to reduce search space.
- Transposition table support for repeated board states.
- Immediate win and threat detection.
- Hint button powered by the AI move evaluator.
- Undo, new game, quit, and visual winning-stone highlighting.
- Fullscreen Pygame interface with board, settings, and game-status panels.

## AI Approach

The AI uses a depth-limited minimax search with alpha-beta pruning. Since Connect6 has a large branching factor, the implementation narrows the candidate move list with smart move ordering before evaluating pairs of moves.

The heuristic system includes:

- Pattern scoring for consecutive stones.
- Defensive weighting for opponent threats.
- Critical pattern detection for immediate win or block opportunities.
- Center-control scoring.
- Connected-group scoring.
- Separate basic and advanced heuristic modes with different search settings.

## Project Structure

```text
connect-six-ai-game/
  ConnectSixGame.ipynb   Main notebook with game logic, AI, and Pygame UI
  requirements.txt       Python dependencies
  .gitignore             Local Python/Jupyter files to ignore
  README.md              Project documentation
```

## Requirements

- Python 3.10 or newer
- Jupyter Notebook or VS Code with notebook support
- Pygame
- NumPy

Install dependencies:

```bash
pip install -r requirements.txt
```

## How to Run

Clone the repository:

```bash
git clone https://github.com/Yehia-Alsaeed/connect-six-ai-game.git
cd connect-six-ai-game
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Open the notebook locally:

```bash
jupyter notebook ConnectSixGame.ipynb
```

Run all cells. The game opens a Pygame window, so it should be run on a local machine with desktop display support rather than inside GitHub's static notebook preview.

## Gameplay

1. Select the player mode: human vs human, human vs AI as black, or human vs AI as white.
2. Select the AI heuristic: basic or advanced.
3. Select the board size.
4. Press `New Game`.
5. Place stones by clicking on board intersections.
6. Use `Hint` to preview an AI-recommended move.
7. Use `Undo` to revert recent moves.

## What This Project Demonstrates

- Object-oriented board-game implementation in Python.
- Interactive game UI development with Pygame.
- AI search for adversarial games.
- Heuristic design for a large board-game search space.
- Alpha-beta pruning and move ordering for performance.
- State tracking, move history, undo behavior, and win detection.

## Notes

This is a notebook-based academic project. The current repository keeps the original notebook workflow while documenting how to run and understand the implementation. A future production version could split the notebook into reusable Python modules, add automated tests for board logic, and package the game as a standalone desktop application.
