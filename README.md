# Simple Go (Baduk / Weiqi)

A lightweight, high-performance **Go game** implementation built with HTML5 Canvas and Vanilla JavaScript. This project features a strategic AI, support for multiple board sizes, and a built-in scoring engine.



---

## 🎮 Game Rules

Go is an abstract strategy board game for two players. The primary goal is to use your stones to form territories by surrounding vacant areas of the board.

### 1. The Basics
* **Players:** Black moves first, followed by White.
* **Placement:** Stones are placed on the **intersections** (points) of the grid lines.
* **Movement:** Once placed, stones are stationary unless they are captured.

### 2. Capture & Liberties
* **Liberties:** These are the empty adjacent intersections (horizontal and vertical) around a stone or a connected group.
* **Capture:** When a stone or group is completely surrounded by opponent stones and has **zero liberties**, it is captured and removed from the board.



### 3. Special Rules
* **Suicide Rule:** You cannot place a stone where it would immediately have no liberties, unless that move captures an opponent's group.
* **Ko Rule:** To prevent infinite loops, you cannot make a move that returns the board to the exact state it was in on your previous turn.
* **Komi:** White receives **+7.5 points** at the end of the game to compensate for Black's first-move advantage.

### 4. Game End & Scoring
* **Ending:** The game ends when both players **Pass** consecutively.
* **Scoring:** This app uses **Area Scoring** (Chinese Style):
  $$Score = \text{Stones on Board} + \text{Surrounded Empty Points}$$

---

## 🤖 AI Logic (Heuristics)

The "Hard" difficulty utilizes a weighted heuristic engine to evaluate potential moves without a heavy tree search.

### Scoring Factors:
| Factor | Weight | Description |
| :--- | :--- | :--- |
| **Capture Value** | +15 per stone | Prioritizes moves that immediately remove opponent stones. |
| **Atari Avoidance** | -50 | Penalizes moves that leave the AI's own group with only 1 liberty. |
| **Positional Bias** | +5 | Early game preference for the 3rd and 4th lines (Star points). |
| **Edge Penalty** | -3 | Discourages playing on the 1st line during the opening phase. |

---

## ✨ Features

* **Adjustable Board Sizes:** 9x9, 13x13, or 19x19.
* **Three AI Levels:** From random play to strategic positioning.
* **Interactive Scoring:** Mark "dead" stones manually before finalizing the score.
* **Responsive UI:** Fully optimized for mobile touch and desktop clicks.

---

## 🛠️ Installation & Usage

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/yourusername/simple-go.git](https://github.com/yourusername/simple-go.git)
   
