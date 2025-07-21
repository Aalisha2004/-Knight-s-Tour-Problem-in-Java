
# Knight's Tour Problem in Java

This project is a Java implementation of the **Knight's Tour** problem using **Backtracking**.

## 📌 What is the Knight's Tour?

The Knight's Tour is a classic problem in computer science and chess mathematics. The objective is to move a knight on an empty 8x8 chessboard such that it visits every square exactly once.

The knight can move in an "L" shape: two squares in one direction and then one square perpendicular to that direction.

## 🧠 Approach

This implementation uses **recursive backtracking** to explore all possible moves and backtrack if a move leads to a dead end.

- The knight starts at position **(0,0)**.
- It recursively tries all 8 possible knight moves at each step.
- If a full tour (64 moves) is completed, the solution is printed.
- If no solution is found, it reports that the solution doesn't exist.

## 📁 File Structure

```

tourSolution.java
README.md

````

## 🚀 How to Run

1. **Compile the Program**
   ```bash
   javac tourSolution.java
````

2. **Run the Program**

   ```bash
   java tourSolution
   ```

## 🧾 Output

* If a solution exists, it prints the board with numbers indicating the order in which the knight visits the squares.
* If no solution exists, it prints:

  ```
  Solution does not exist
  ```

### Example Output

```
0 59 38 33 30 17 8 63
37 34 31 60 9 62 29 16
58 1 36 39 32 27 18 7
35 48 41 26 61 10 15 28
42 57 2 49 40 23 6 19
47 50 45 54 25 20 11 12
56 43 52 3 22 13 24 5
51 46 55 44 53 4 21 14
```

## 🛠️ Key Functions

* `isSafe(x, y, sol)` — Checks if the knight can move to (x, y).
* `solveKT()` — Initializes the board and starts solving.
* `solveKTUtil(x, y, movei, sol, xMove, yMove)` — Recursive function that performs the backtracking logic.
* `printSolution(sol)` — Prints the chessboard with the knight’s tour path.

## 🧩 Algorithm Details

* **Board Size:** 8x8 (`N = 8`)
* **Moves Checked:** All 8 possible knight moves in clockwise order.
* **Backtracking:** If a move does not lead to a solution, it undoes the move (`sol[x][y] = -1`) and tries the next.
