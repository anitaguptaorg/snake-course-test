# Project Overview
This project is a classic implementation of the Snake game using Python's built-in `turtle` module. It is designed to be lightweight, requiring no external dependencies, and provides a smooth, grid-based gameplay experience with real-time score tracking.

- **Main Technology:** Python 3.x
- **Core Module:** `turtle` (for graphics and input handling)
- **Architecture:** Single-file event-driven script with a central game loop.

# Building and Running
As a pure Python script using only the standard library, there is no build step required.

- **Run the Game:**
  ```bash
  python snake.py
  ```
- **Testing:**
  - Currently, there are no automated tests.
  - TODO: Implement unit tests for core game logic (e.g., collision detection, score calculation) using `unittest` or `pytest`.

# Development Conventions
- **Coding Style:** The codebase follows standard Python naming conventions (snake_case for functions and variables).
- **Environment:** Designed to run in any environment with Python 3.x and access to a graphical display.
- **Modularity:** Game logic is encapsulated in functions (`move`, `reset_game`, `update_scoreboard`), making it easy to extend or refactor.
- **Input Handling:** Uses `screen.onkeypress` for responsive controls via arrow keys.
