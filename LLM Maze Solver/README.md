# 🧩 ASCII Maze Solver – Tree-of-Thought LLM Prompting

This project implements an **ASCII-based maze solver** using **Tree-of-Thought (ToT) prompting** with an **LLM (GPT-4o-mini)**.  
The goal was to design prompts and minimal supporting code to guide the model through reasoning-based maze navigation — effectively letting the model "think" through possible paths before deciding.

---

## **Overview**
The system:
- Flattens an `N×M` ASCII maze into a 1-D string (rows delimited by `|`).
- Flattens a 3×3 local grid to describe the LLM’s current surroundings.
- Uses prompt-based reasoning to choose valid next moves (`U`, `D`, `L`, `R`).
- Applies a **Tree-of-Thought** approach: exploring move sequences using a depth-first style search and backtracking to refine reasoning.

Each maze was solved through repeated LLM interactions, showing that careful prompt engineering can make reasoning-driven control tasks feasible — though not efficient.

---

## **Results Summary**
- **All three mazes solved successfully**, often with *optimal* paths.  
- **Token usage per maze:** 2.3k–5.6k total (input + output).  
- **Estimated cost per run:** \$0.0007–\$0.0017 (based on GPT-4o-mini pricing).  
- Demonstrated reliable local reasoning, but inconsistent global planning and slow runtime due to API latency.

---

## **Limitations**
While effective for demonstration, this method:
- Is **slow**, **stochastic**, and **costly** compared to classical solvers (BFS/DFS/A*).  
- Relies heavily on precise prompt scaffolding.  
- Shows that LLMs still struggle with **spatial reasoning** and **deterministic pathfinding**.

**Verdict:** Great as a research and teaching tool — not as a production maze solver.

---

## **Setup**
1. Clone or download this project.  
2. Install dependencies:
   ```bash
   pip install openai
3. You'll need your own API key.


## **Acknowledgements**
Credit to Professor Scott Dick and ECE 449 course material (University of Alberta) for providing the foundational lab framework
and conceptual design of this experiment.
