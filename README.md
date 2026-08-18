# 🐍 Snake AI — Deep Reinforcement Learning (DQN)

An autonomous Snake game agent built with Pygame and trained using Deep Q-Learning (PyTorch).

---

## 🧠 How It Works

* **State (11 inputs):** Danger ahead/left/right, current heading (one-hot), and relative food direction.
* **Actions (3 outputs):** `[Straight, Turn Right, Turn Left]`.
* **Rewards:** `+10` for food, `-10` for death, `0` for normal steps.
* **Model:** Deep Q-Network (`Linear_QNet`) with Experience Replay and $\epsilon$-greedy exploration.

---

## 📦 Installation

```bash
git clone [https://github.com/your-username/snake-ai.git](https://github.com/your-username/snake-ai.git)
cd snake-ai
pip install pygame torch torchvision matplotlib
### 🎮 Manual Play Mode (Testing Environment)

Test game physics, mechanics, and boundary collisions manually:

```bash
python snake_game.py

```

* 
**Controls:** ↑ ↓ ← → Arrow keys.



---

## ⚙️ Hyperparameter Reference

Key configuration settings across `agent.py` and `game.py`:

| Parameter | Default | Description |
| --- | --- | --- |
| `MAX_MEMORY` | `100_000` | Experience replay buffer size 

 |
| `BATCH_SIZE` | `1000` | Mini-batch sample size for gradient updates 

 |
| `LR` | `0.001` | Adam Optimizer learning rate 

 |
| `GAMMA` ($\gamma$) | `0.9` | Future reward discount factor 

 |
| `BLOCK_SIZE` | `20` | Pixel dimensions per grid block 

 |
| `SPEED` | `40+` | Clock tick speed for training acceleration 

 |

```

```
