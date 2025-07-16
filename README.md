# 🧩 Sudoku Solver using Dancing Links (DLX) in C++

🚀 A fast and efficient console-based Sudoku solver built in C++, leveraging **Donald Knuth's Dancing Links (DLX)** algorithm to model and solve the puzzle as an **Exact Cover Problem**.
## 🔧 Tech Stack
- **Language**: C++
- **Algorithm**: DLX (Dancing Links)
- **Approach**: Backtracking + Exact Cover Mapping
- **Memory Model**: Pointer-based linked list (no STL used)

## 📌 Features
- Converts any standard 9×9 Sudoku puzzle into an **Exact Cover Problem** using concepts from **Combinatorics** and **Boolean Algebra**.
- Implements the **Dancing Links (DLX)** algorithm with a custom-built **toroidal doubly linked list** for ultra-fast row and column manipulation.
- Efficiently solves puzzles across all difficulty levels — from easy to diabolical.
- Completely **STL-free** — low-level implementation with manual memory management and performance-focused design.
- Clean console output of the solved **Sudoku** grid.

## 🧠 Algorithm Overview

The **Dancing Links (DLX)** algorithm is employed to solve **Exact Cover** problems with high efficiency. In this project:

- The 9×9 Sudoku puzzle is converted into a **Boolean constraint matrix** with 729 rows (9×9×9 possible cell-number combinations) and 324 columns (representing constraints for rows, columns, boxes, and cells).
- Each row in the matrix corresponds to a valid assignment of a number to a specific cell.
- This matrix is transformed into a **toroidal doubly linked list**, enabling constant-time removal and restoration of rows and columns during the backtracking process.
- A recursive search algorithm navigates through possible number placements and backtracks effectively using the **DLX** technique.

## 🖥️ How to Run

1. **Compile the code:**
   ```bash
   g++ -o sudoku_solver sudoku_solver.cpp
   ```

2. **Run the executable:**
   ```bash
   ./sudoku_solver
   ```

3. **Input:**
   * Enter the 9×9 Sudoku puzzle row-wise, using `0` to represent empty cells.

4. **Output:**
   * Displays the completed Sudoku grid if a solution exists.
   * Otherwise, shows `"No Solution Exists"`.

## 📂 Sample Input
5 3 0 0 7 0 0 0 0  
6 0 0 1 9 5 0 0 0  
0 9 8 0 0 0 0 6 0  
8 0 0 0 6 0 0 0 3  
4 0 0 8 0 3 0 0 1  
7 0 0 0 2 0 0 0 6  
0 6 0 0 0 0 2 8 0  
0 0 0 4 1 9 0 0 5  
0 0 0 0 8 0 0 7 9  

## ✅ Sample Output

5 3 4 6 7 8 9 1 2  
6 7 2 1 9 5 3 4 8  
1 9 8 3 4 2 5 6 7  
8 5 9 7 6 1 4 2 3  
4 2 6 8 5 3 7 9 1  
7 1 3 9 2 4 8 5 6  
9 6 1 5 3 7 2 8 4  
2 8 7 4 1 9 6 3 5  
3 4 5 2 8 6 1 7 9


## 🏗️ Project Structure
sudoku_solver.cpp      // Main source file
README.md              // Project documentation

## 📘 References

* [Donald Knuth - Dancing Links (DLX)](https://arxiv.org/pdf/cs/0011047.pdf)
* [Exact Cover Problem – Wikipedia](https://en.wikipedia.org/wiki/Exact_cover)

## 🙋‍♂️ Author

**Aditya Sharma**
