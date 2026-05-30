# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Running the Game

```bash
python snake.py
```

Requires Python 3.x and a graphical display (the `turtle` module opens a GUI window). No external dependencies or build step needed.

## Architecture

Single-file script (`snake.py`) with a global event loop. Key design points:

- **Global state**: `SCORE`, `HIGH_SCORE`, and `segments` (list of body `Turtle` objects) are module-level globals mutated throughout the loop.
- **Grid**: 600×600 window, 20px grid steps. Border collision triggers at ±290 on either axis.
- **Game loop**: `while True` + `time.sleep(DELAY)` drives timing. `screen.tracer(0)` / `screen.update()` controls rendering manually.
- **Snake body**: Each body segment is a separate `Turtle` object appended to `segments`. On each tick, segments shift positions in reverse order, then segment 0 copies the head's prior position.
- **Collision detection**: Distance-based (`< 20`) for both food and self-collision.
- **Reset**: `reset_game()` hides segments by teleporting them off-screen (`goto(1000, 1000)`), clears the list, and resets score — it does **not** destroy/recreate `Turtle` objects.

## Controls

Arrow keys (Up/Down/Left/Right). Reverse direction is blocked (e.g., can't go Down while moving Up).
