# GAP_using_approximation_method
# Generalized Assignment Problem (GAP) - Approximation Method

This project provides an implementation of an **approximation method** (greedy heuristic) for solving instances of the **Generalized Assignment Problem (GAP)** using Python.The objective is to assign users to servers such that:

- Each user is assigned to exactly one server.
- The total utility is maximized.
- Server resource constraints are not violated.

It also includes a comparison of the greedy approach results with the optimal solutions.

## 📁 Project Structure

project/
│
├── approximate_GAP_solver.ipynb        # Main Jupyter notebook (create or move here)
├── gap_dataset_files/              # Folder containing gap1.txt, gap2.txt, ... (already exists)
│   ├── gap1.txt
│   ├── gap2.txt
│   └── ...                         # All GAP dataset files
│
├── greedy_results.csv              # Output from Greedy method
├── optimal_results.csv             # Output from Optimal method
├── gap_comparison_plot.png         # Graph comparing results
├── README.md  

## 🧩 Problem Statement


The problem is adapted from:  
**"An efficient approximation for the generalized assignment problem"**  
_Cohen, Reuven, Liran Katzir, and Danny Raz_ (Information Processing Letters, 2006)

- Each dataset contains multiple instances of user-server assignment problems.
- The utility, VM allocation, and server capacity data are provided in OR-Library format.

The full problem description and datasets are available at:  
[https://people.brunel.ac.uk/~mastjjb/jeb/orlib/gapinfo.html](https://people.brunel.ac.uk/~mastjjb/jeb/orlib/gapinfo.html)

## 🧠 Approximation Method

The approximation method used here is a **greedy heuristic**:
- For each task, the algorithm selects the agent that offers the highest profit-to-cost ratio, considering capacity constraints.
- This results in a near-optimal assignment with significantly reduced computation time.

## 📊 Results

Two CSV files are provided for comparison  which is the output you get, after execution of code:
- `greedy_results.csv`: Contains the results (total profit, time taken, etc.) from the greedy(approximation) method.
- `optimal_results.csv`: Contains the optimal solution results for the same datasets.

## 🧠 How it Works

### Dataset Format

Each `.txt` file contains:
1. Number of instances
2. For each instance:
   - Number of servers and users
   - Utility matrix (servers × users)
   - VM allocation matrix (servers × users)
   - Server capacities (list)

### Output

For each instance:
- Task Assignments (user → server)
- Total Optimal Utility

### Example Output

```
Processing Instance 1 from gap1.txt  
Task Assignments: [1, 2, 0, 3, ...]  
Total Optimal Utility: 562.0
```

## 📦 How to Run

1. Replace the file path same as your directory in the code .
2. Open the notebook `assignment1(approximation_method).ipynb` using Jupyter.
3. Run all cells to execute the approximation method on the dataset.
4. the first cell contains the code for approximation method
5. next cell contains code for optimal method(PULP).
6. last cell plots the graph.
## 🧮 Requirements

- Python 3.x
- Jupyter Notebook
- NumPy
- Pandas

Install dependencies using:
```bash
pip install numpy pandas notebook
```

## 📌 Notes

- The dataset files (`.gap`) follow a standard GAP format and are parsed within the notebook.
- The method is fast and scalable, though it does not always guarantee an optimal solution.
- Useful for large-scale instances where exact methods become computationally expensive.



## 🧾 References

- Cohen, R., Katzir, L., & Raz, D. (2006).  
  [An efficient approximation for the generalized assignment problem](https://www.sciencedirect.com/science/article/abs/pii/S0020019006001931)
- OR-Library GAP datasets:  
  [https://people.brunel.ac.uk/~mastjjb/jeb/orlib/gapinfo.html](https://people.brunel.ac.uk/~mastjjb/jeb/orlib/gapinfo.html)



## ✍️ Author


**Md Kaif
M.Tech (cse)
Nit Jamshedpur**
