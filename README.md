# ML Hackathon: “Hackman” (Hangman AI Agent)

**Date:** November 4, 2025
## 1️⃣6️⃣ Team Number- 16
## 👥 Team Members
- **Yash Verma** (PES1UG23AM910)  
- **Vraj Detroja** (PES1UG23AM914)  
- **Shravan Kumar** (PES1UG24AM813)

---

## 🧠 Project Overview

This project is a solution for the **PES University UE23CS352A Machine Learning Hackathon**.  
The challenge: build a **hybrid system** to intelligently solve the game of **Hangman**.

Our solution consists of two mandated components:

### Part 1: The “Oracle” (HMM)
- A **letter-bigram Hidden Markov Model** trained on the provided `corpus.txt`.
- We implemented the **Forward–Backward algorithm** to compute posterior probabilities  
  \( P(\text{letter} \mid \text{pattern}, \text{guessed\_letters}) \) for all blank slots.  
- This gives the agent a powerful **linguistic intuition**.

### Part 2: The “Brain” (RL Agent)
- A complete **Reinforcement Learning** framework.
- A **707-dimension state vector** combining:
  - the current game pattern,
  - guessed letters,
  - remaining lives,
  - and the HMM’s probability outputs.
- The final agent uses the HMM’s probabilities as a **proxy for Q-values** in its exploitation strategy (an intelligent HMM-based heuristic).

---

## ✅ Final Evaluation Results

- **Final Score:** `-50,558.0`  
- **Success Rate:** `36.35%` (**727 Wins**)  
- **Total Wrong Guesses:** `10,257`  
- **Total Repeated Guesses:** `0`

---

## 📁 Files in this Repository

- `ML_Hackathon_Collab_Run.ipynb` — The complete Python notebook.
- `Analysis Report.pdf` — The detailed project report answering all hackathon questions.
- `corpus.txt` — The **50,000-word** training dataset.
- `test.txt` — The **2,000-word** test dataset.
- `Corpus Word Length Distribution.png` — EDA plot used in the report.
- `Final Evaluation Results.png` — Final results plot used in the report.

---

## ▶️ How to Run

1. **Prerequisites**
   - Python 3.9+ recommended
   - Libraries: `numpy`, `pandas`, `matplotlib`

   Install (if needed):
   ```
   bash
   pip install numpy pandas matplotlib
   ```
2. **Project Setup**
   - Place all files (the notebook and the .txt datasets) in the same directory.

3. **Run the Notebook**
    - Open and run f87d51a151f04ede9849b2c63ef3080a.md from top to bottom.

4. **Evaluation Steps**
   - Cell 8 runs the full evaluation on test.txt.
   - Cell 9 generates the final evaluation plot.
---
