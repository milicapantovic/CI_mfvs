Minimum Feedback Vertex Set project
=======
# Minimum Feedback Vertex Set in Directed Graphs

## Problem Statement

The **Minimum Feedback Vertex Set (MFVS)** problem is a well-known **NP-complete** problem. Formally, given an directed graph G = (V, E) the objective is to identify the smallest subset of vertices S ⊆ V such that the removal of S results in an acyclic graph (a forest). This project implements and compares several algorithms for this problem in directed graphs.

The MFVS problem arises in numerous theoretical and practical contexts, including:

* **Deadlock detection and resolution** in operating systems and distributed systems
* **Circuit design and testing**
* **Program optimization**
* **Constraint satisfaction problems**


## Implemented Methods

1. **Naive Exact Algorithm:** enumerates all vertex subsets and checks for acyclicity. Guarantees optimality but feasible only for very small graphs (n ≤ 10).

2. **Greedy Cycle-Frequency Heuristic:** removes the vertex most frequently appearing in cycles.

3. **Greedy-Degree-Product Heuristic:** removes the vertex with the highest in-degree × out-degree.

4. **WLS D-Sequence Heuristic:** based on the method by Wang, Lloyd, and Soffa (1985, 1988). Constructs a D-sequence of vertices using associated graphs. Provides optimal results on cyclically reducible graphs.

5. **Local-Ratio Inspired Heuristic:** adapted from approximation algorithms for the undirected variant. Balances solution quality and runtime, though without proven guarantees for DFVS. 

6. **Iterative Compression (Sketch):** Based on Reed–Smith–Vetta (2004). Demonstrates exact methods for small k.

## Requirements:

 * Python 3.11, 
 * networkX 
 * matplotlib

## Results:

 * Naive Exact: optimal but impractical for larger graphs.

 * Degree-Product: fastest, scales well.

 * Frequency: more accurate but slower.

 * WLS D-Sequence: best overall, often close to optimal.

 * Local-Ratio: competitive, moderate speed and quality.

## Each run will:

* Print the DFVS size, runtime, and validity.
* Show the original graph with DFVS highlighted.
* Show the resulting DAG after vertex removal.

## Visualization

The Jupyter Notebook provides visualizations of graphs with the identified feedback vertex sets, as well as comparative charts illustrating algorithmic runtime and solution quality.

## Requirements

* Python 3.10+
* NetworkX
* pandas
* matplotlib
* Jupyter Notebook for interactive exploration

## References

 * Wang, Lloyd, Soffa (1985, 1988). Feedback Vertex Sets and Cyclically Reducible Graphs.

 * Bafna, Berman, Fujito (1999). A 2-approximation algorithm for the undirected feedback vertex set problem.

 * Chudak, Goemans, Hochbaum, Williamson (1998). Primal-dual approximation algorithms for feedback problems.

 * Cao (2018). Naive Algorithms for Feedback Vertex Set.

 * Reed, Smith, Vetta (2004). Iterative Compression and Odd Cycle Transversal.

 * Guo, Moser, Niedermeier (2006). Iterative Compression for Feedback Vertex Set.

 * Fomin, Gaspers, Pyatkin (2006). On exact algorithms for feedback vertex set.

## Authors

* Isidora Dukić 146/2020
* Milica Pantović 46/2019

>>>>>>> bef5c3f (feat: project notebook added)
