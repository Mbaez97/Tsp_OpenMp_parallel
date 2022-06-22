# TSP - Traveling Salesman Problem

In this proyect we will implement the TSP algorithm using the [Genetic Algorithm](https://en.wikipedia.org/wiki/Genetic_algorithm) and the [Simulated Annealing](https://en.wikipedia.org/wiki/Simulated_annealing).

## Genetic Algorithm

Is a search-based optimization technique used to find the optimal solution to a problem.
Initially, the algorithm builds a candidate solution and then iteratively improves it.  
The algorithm is said to be **generational**, because each generation is a new generation of solutions.
It is stopped when we reach a stopping criteria. For problems such as The Traveling Salesman Problem, which are considered NP-Hard in nature, the Genetic Algorithm is an efficient tool, and provides a good-enough near-optimal solution (or a set of such solutions), although it doesn’t guarantee the optimal solution.

## Parallel Algorithm

The Genetic Algorithm code for the travelling salesman problem is written in C, which supports OpenMP. At various for loops during one iteration, we can use pragma omp to parallelise the logic. Although we cant parallelise the overall algorithm, since each generation needs the output of the previous generation we can parallelise the various functions inside one generation.
