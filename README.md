
---

```markdown
# 🐍 Classic Snake Game in Pygame

[cite_start]A clean, modular implementation of the classic Snake game built using Python and Pygame[cite: 70]. [cite_start]Designed with clean architecture, strict data types (`Enum`, `namedtuple`), and a step-based game loop structured for easy adaptation into Reinforcement Learning (AI) environments[cite: 58, 72, 101].

---

## 🎮 Features

- [cite_start]**Grid-Based Movement:** Snaps strictly to a 20x20 pixel grid to ensure clean alignment[cite: 76, 219].
- [cite_start]**Safe State & Direction Handling:** Utilizes Python's `Enum` to eliminate typo-prone string bugs and magic numbers[cite: 2, 73].
- [cite_start]**Lightweight Coordinates:** Uses `namedtuple` (`Point(x, y)`) for readable, efficient coordinate handling[cite: 74, 230].
- [cite_start]**Collision Detection:** Full boundary detection and self-collision handling[cite: 95, 178].
- [cite_start]**AI-Ready Structure:** Employs a `play_step()` cycle that neatly separates action input, state updates, rendering, and terminal reward/score returns[cite: 58, 83, 93].

---

## 🛠️ Project Structure & Architecture

[cite_start]The codebase is split into modular components for clarity and maintainability[cite: 71, 162]:

| Section | Component | Description |
| :--- | :--- | :--- |
| **Part 1–3** | `Setup & Constants` | [cite_start]Pygame engine initialization, `Direction` Enum, `Point` namedtuple, colors, and grid configurations[cite: 142, 164, 166, 167]. |
| **Part 4–5** | `Initialization & Spawning` | [cite_start]`SnakeGame.__init__()` sets up the window and snake body[cite: 143, 168]; [cite_start]`_place_food()` spawns apples on open grid spots[cite: 143, 172]. |
| **Part 6** | `Game Loop Engine` | [cite_start]`play_step()` collects events, executes movement, detects collisions, manages eating logic, and updates frames[cite: 145, 173, 174, 175, 176]. |
| **Part 7–9** | `Helper Utilities` | [cite_start]`_is_collision()` (boundary/self checks) [cite: 146, 178][cite_start], `_update_ui()` (rendering display) [cite: 146, 180][cite_start], and `_move()` (coordinate math)[cite: 146, 182]. |
| **Part 10** | `Execution Entry` | [cite_start]Standard entry block running the game instance until `game_over` triggers[cite: 147, 148, 184, 185]. |

---

## 🕹️ Controls

| Key | Action |
| :--- | :--- |
| <kbd>↑</kbd> | [cite_start]Move Up [cite: 62] |
| <kbd>↓</kbd> | [cite_start]Move Down [cite: 62] |
| <kbd>←</kbd> | [cite_start]Move Left [cite: 61] |
| <kbd>→</kbd> | [cite_start]Move Right [cite: 61] |
| <kbd>X</kbd> (Window Button) | [cite_start]Quit Game [cite: 61] |

---

## 📦 Requirements & Installation

1. **Clone or Download the Repository:**
   ```bash
   git clone [https://github.com/your-username/snake-pygame.git](https://github.com/your-username/snake-pygame.git)
   cd snake-pygame

```

2. **Install Required Packages:**
Ensure you have Python 3.7+ and Pygame installed:


```bash
pip install pygame

```


3. **Font Setup (Optional):**
The project references `arial.ttf` locally. If you do not have this file in your project directory, toggle to the system font in the script:


```python
# font = pygame.font.Font('arial.ttf', 25)
font = pygame.font.SysFont('arial', 25)

```



---

## 🚀 Running the Game

Launch the game using Python:

```bash
python snake_game.py

```

---

## ⚙️ Game Configurations

You can adjust key variables directly in the script constants:

```python
BLOCK_SIZE = 20  # Pixel size of each snake segment and food block
SPEED = 20       # Frames per second (FPS) / snake movement speed

```

```

```