# Connect Four AI: A Minimax Approach

This is a Python-based Connect Four game where a **human player (RED)** plays against an **AI (WHITE)** powered by the **Minimax algorithm with Alpha-Beta Pruning**. The game was developed as a semester project for the Artificial Intelligence course at Air University.

## Game Overview

Connect Four is a two-player connection game on a **6x7 board**. The goal is to strategically insert tokens into columns to **connect four** in a **row, column, or diagonal**.

- The **AI always plays first** and drops the **WHITE** token.
- The **human player uses RED** and interacts via drag-and-drop.
- The game includes **animated token drops**, **move counters**, and a **starry night background**.
- After every match, a **winner or tie screen** is displayed.


## 🧠 AI Logic: Minimax + Alpha-Beta Pruning

There are **4,531,985,219,092** unique board states—making it impossible to brute force. Instead, the AI uses:

- **Minimax Algorithm**: Alternates between maximizing and minimizing future outcomes.
- **Alpha-Beta Pruning**: Eliminates branches of the game tree that do not affect the outcome, drastically speeding up decision-making.

### 🧮 Score Function

The algorithm evaluates only terminal (leaf) nodes using:

| Leaf Node Condition | Score Computation                     |
|---------------------|----------------------------------------|
| AI Win              | `22 - moves played` (Positive score)   |
| Player Win          | `-(22 - moves played)` (Negative score)|
| Draw                | `0`                                    |

---

## 🧱 Board Representation

A **board** is used to represent the current state. Bitwise operations help:

- Track AI vs Player moves
- Validate legal moves
- Detect win/draw conditions

---

## 🖥️ GUI Features (Using Pygame)

- 🔁 Animated token drop
- 🌌 Starry background
- 🔴 Drag-and-drop RED token for player
- 🟡 AI moves animate from side
- 🧮 Move counter displayed
- 🏆 End screen for **Win / Lose / Tie**

---

## 🚀 Getting Started

### ✅ Prerequisites

- Python 3.x
- [Pygame](https://www.pygame.org/news)

### 🛠️ Installation

```bash
git clone https://github.com/Aqsarehman230489/connect-four-ai-game.git
cd connect-four-ai-game
to run: python main.py
