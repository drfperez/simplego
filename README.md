# Go Game vs AI

A simple **Go board game** implemented in **HTML, CSS, and JavaScript** where you can play against an AI. The game supports **9x9, 13x13, and 19x19 boards**, multiple difficulty levels, and is **mobile-first responsive**.  

---

## Features

- **Human vs AI** gameplay.
- Board sizes: **9x9**, **13x13**, **19x19**.
- AI difficulty levels: **Easy**, **Medium**, **Hard**.
- **Stone placement** with legal move checks, capture rules, and Ko rule enforcement.
- **Score calculation** including territory and komi.
- **Pass and show score** functionality.
- **Mobile-friendly**, fully responsive canvas.
- **"How to Play" modal** for beginners.

---

## How to Play

1. **Choose board size** and **difficulty**.
2. Click **New Game** to start.
3. **Black (You)** always plays first.
4. Click or tap intersections to place stones.
5. Stones cannot move once placed.
6. **Capture stones** by surrounding your opponent's group.
7. Use **Pass** when no moves are desired.
8. Game ends when both players pass consecutively.
9. Click **Show Score** to see the current score estimation.

---

## Controls

| Button          | Description                            |
|-----------------|----------------------------------------|
| New Game        | Starts a new game                       |
| Pass            | Pass your turn                          |
| Show Score      | Displays the current score             |
| How to Play     | Opens a modal with Go rules            |

---

## AI Difficulty Levels

The AI has three difficulty levels, each using increasingly complex logic to choose its moves:

### **Easy**
- **Behavior:** Chooses **random legal moves** from all available intersections.
- **Strategy:** No evaluation of captures, liberties, or board position.  
- **Result:** Unpredictable but weak; good for beginners.

### **Medium**
- **Behavior:** Evaluates moves based on **potential captures**.  
- **Algorithm:**
  1. For each legal move, calculate how many opponent stones would be captured.
  2. Keep a list of moves with the **maximum captures**.
  3. Randomly select one move from the best candidates.
- **Strategy:** Prioritizes immediate captures, but does not plan multiple turns ahead.  
- **Result:** Moderate challenge for casual players.

### **Hard**
- **Behavior:** Uses a **heuristic board evaluation** to maximize long-term advantage.
- **Algorithm:**
  1. Generate a set of legal moves (limited for larger boards to avoid slow computation).
  2. For each move:
     - Simulate the move temporarily.
     - Capture opponent stones.
     - Evaluate board score using a heuristic:
       - Stones owned by AI: +1 point each.
       - Stones owned by opponent: -1 point each.
       - Liberties (empty adjacent points) of AI groups: +0.5 points per liberty.
       - Liberties of opponent groups: -0.5 points per liberty.
  3. Restore the board and select the move with the **highest evaluated score**.  
  4. If multiple moves tie, pick one randomly.
- **Strategy:** Considers both immediate captures and board control (territory and liberties).  
- **Result:** Strong challenge, mimics strategic thinking without full minimax search.

---

## Technologies

- **HTML5** — Structure of the board and UI.
- **CSS3** — Styling and responsive design.
- **JavaScript** — Game logic, AI, stone placement, captures, scoring.
- **Canvas API** — Drawing the board and stones.

---

## Controls

| Button          | Description                            |
|-----------------|----------------------------------------|
| New Game        | Starts a new game                       |
| Pass            | Pass your turn                          |
| Show Score      | Displays the current score             |
| How to Play     | Opens a modal with Go rules            |

---

## AI Difficulty Levels

The AI has three difficulty levels, each using increasingly complex logic to choose its moves:

### **Easy**
- **Behavior:** Chooses **random legal moves** from all available intersections.
- **Strategy:** No evaluation of captures, liberties, or board position.  
- **Result:** Unpredictable but weak; good for beginners.

### **Medium**
- **Behavior:** Evaluates moves based on **potential captures**.  
- **Algorithm:**
  1. For each legal move, calculate how many opponent stones would be captured.
  2. Keep a list of moves with the **maximum captures**.
  3. Randomly select one move from the best candidates.
- **Strategy:** Prioritizes immediate captures, but does not plan multiple turns ahead.  
- **Result:** Moderate challenge for casual players.

### **Hard**
- **Behavior:** Uses a **heuristic board evaluation** to maximize long-term advantage.
- **Algorithm:**
  1. Generate a set of legal moves (limited for larger boards to avoid slow computation).
  2. For each move:
     - Simulate the move temporarily.
     - Capture opponent stones.
     - Evaluate board score using a heuristic:
       - Stones owned by AI: +1 point each.
       - Stones owned by opponent: -1 point each.
       - Liberties (empty adjacent points) of AI groups: +0.5 points per liberty.
       - Liberties of opponent groups: -0.5 points per liberty.
  3. Restore the board and select the move with the **highest evaluated score**.  
  4. If multiple moves tie, pick one randomly.
- **Strategy:** Considers both immediate captures and board control (territory and liberties).  
- **Result:** Strong challenge, mimics strategic thinking without full minimax search.

---

## Technologies

- **HTML5** — Structure of the board and UI.
- **CSS3** — Styling and responsive design.
- **JavaScript** — Game logic, AI, stone placement, captures, scoring.
- **Canvas API** — Drawing the board and stones.

---

## Installation

1. Clone the repository:

```bash
git clone https://github.com/yourusername/go-game-ai.git
````

2. Open `index.html` in your browser.
3. Start playing!

---



## License

This project is **open-source** and free to use.

---

```
