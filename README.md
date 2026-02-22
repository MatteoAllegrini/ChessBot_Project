# ChessBot_Project

# ♟️ ChessBot – Thinking in Moves  

A fully functional chess engine built from scratch in Python, featuring a complete board implementation and an AI powered by **Minimax with Alpha-Beta Pruning**.

This project explores the core principles behind chess engines, focusing on algorithmic reasoning, clean design, and practical implementation.

---

## 🚀 Features

- ✅ Complete chess rules implementation  
  - Legal move generation  
  - Castling  
  - En passant  
  - Promotion  
  - Check and checkmate detection  
  - Stalemate detection  

- 🧠 AI Opponent  
  - Minimax search algorithm  
  - Alpha-Beta pruning optimization  
  - Move ordering heuristics  
  - Adjustable difficulty (search depth)

- 📊 Position Evaluation  
  - Hand-crafted evaluation function  
  - Material balance  
  - Piece-square tables (positional heatmaps)

- 🖥️ Text-based Interface  
  - Playable in terminal / Google Colab  
  - ASCII board rendering  
  - PvP and Player vs AI modes  

---

## 🏗️ Project Structure

The engine follows an object-oriented design:

- `Square` – represents a board square  
- `Piece` (+ subclasses: Pawn, Knight, Bishop, Rook, Queen, King)  
- `Move` – encodes move information  
- `Board` – manages game state and rules  
- `minmax_alphabeta()` – core AI search function  

---

## ⚙️ How It Works

### 1️⃣ Move Generation  
Pseudo-legal moves are generated and then filtered to ensure the king is not left in check.

### 2️⃣ Evaluation Function  
Board positions are evaluated using:
- Material values (P=1, N=3, B=3, R=5, Q=9)
- Positional bonuses via piece-square tables
- Checkmate and stalemate detection

### 3️⃣ Search Algorithm  
The AI uses:
- **Minimax** for adversarial decision-making  
- **Alpha-Beta pruning** to reduce explored nodes  
- Heuristic **move ordering** to improve pruning efficiency  

Time complexity:
- Worst case: `O(b^d)`  
- Best case: `O(b^(d/2))`  

Where:
- `b` = branching factor (~35 in chess)  
- `d` = search depth  

---

## 🎮 Game Modes

- **PvP (Player vs Player)**
- **Player vs AI**
  - Easy → depth 2  
  - Medium → depth 3  
  - Hard → depth 4  

---

## 📈 Performance

- Depth 4: plays at an intermediate level  
- Depth 5: significantly stronger but computationally expensive  
- Alpha-Beta pruning substantially reduces evaluated positions  

---

## 🔮 Future Improvements

- Bitboard representation for higher efficiency  
- Transposition tables  
- Quiescence search  
- Improved check detection  
- More advanced evaluation heuristics  

---

## 📚 Educational Purpose

This project is a practical exploration of:

- Game tree search  
- Adversarial AI  
- Algorithm optimization  
- Chess engine architecture  

The implementation prioritizes **clarity and structure** over extreme performance.
