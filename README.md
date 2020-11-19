# N-Queens-problem-using-Hill-climbing-search-and-it-s-variants
N-Queens problem solution using Hill Climbing search and its variants and compare the results of all the searches.

# Problem Formulation:
The N-queens problem is the problem of placing ‘n’ chess queens on an n * n chessboard so that no two queens are attacking each other. This means no queen can be in the same row, column or diagonal. We can find the solutions for all the natural numbers except for n =2 or 3. Here in this report, we are choosing to solve the 8 queens problem by taking a random state by placing 8 queens in the 8*8 chessboard by placing each queen in a column.

There are different types of hill-climbing search techniques that can be used to solve this problem. 
The general hill-climbing search has less percent of success that is around 14%. 
So, to optimize this search there are a couple of updated searches like Hill Climbing sideways move and Random Restart Hill Climbing.
  • Hill climbing search
  • Hill climbing search with sideways movement allowed
  • Random Restart hill climbing search
  • Random restart hill climbing search with sideways movement allowed
  
# Hill Climbing with a sideways move: 
This is an optimized version of the regular hill-climbing search algorithm. 
When a local minimum is reached, continuing search by non-improving “sideways” moves will lead to a significant improvement in the performance of the algorithm.

# Random Restart Hill Climbing: 
This is built on top of the hill-climbing search algorithm.
It iteratively does hill-climbing, each time with a random initial condition. 
The best state is kept; if a new run of hill-climbing produces a better state than the store state, it replaces the stored state. 
This is the most effective algorithm in most of the cases.

# We are using a heuristic function to determine the steps each queen takes. The heuristic cost function h calculates the number of pairs of queens that are attacking each other, either directly or indirectly.


# Code Structure:

# Class 1: HillClimbing:

    1. cells_at_state will return cells with queens in the given state.
    2. print_Nqueen_matrix will print n queen state as a matrix
    3. Horizontal_cells_right_to_current return the cells to the horizontal right of the current cell
    4. diagonal_cells_right_to_current return the cells to the diagonal right of the current cell
    5. total_cells_to_the_right will return all the horizontal and diagonal cells to the right of current cells
    6. heuristic_value returns heuristic value for a given state (h calculates the number of pairs of queens that are attacking each other, either directly or indirectly)
    7. heuristic_matrix calculates heuristic values of each cell and returns heuristic value matrix, least heuristic and numpy array with row and column with least heuristic
    8. randon_state creates and returns a random state which will be used in random restart function.
    9. hill_climbing_search function is a recursive implementation of the hill climbing search using steepest ascent. this method will return result and step towards the least heuristic value at each recursion and the result would contain flat local maxima, local maxima and success
    10. hill_climbing_random_restart function implements random restart algorithm.

# Class 2: project_analysis:

    1. analysis function will start iterating and performs hill climbing and randon-restart hill climbing with and without sideways movement.
    2. print_results function prints stats of all 4 algorithms.
    3. print_hillclimbing_stats will print report of the hill climbing search with and without sideways movement.
    4. print_random_restart_stats will print report of the random restart hill climbing search with and without sideways movement.

# Get N, Iterations and sideways movement as input from the user and run the above classes.
