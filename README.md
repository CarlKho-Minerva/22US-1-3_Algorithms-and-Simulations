# Algorithms and Simulations

### Note from Carl

This assignment and class gave me a sense of accomplishment. The optional TSP algorithm implementation challenged me to convert my deceptively-simple flowchart into code. However, seeing the Randomized Nearest Algorithm together with the 2-opt swap optimize my solution was worthwhile. It taught me to read documentation and forums diligently. Explaining Euler's method in the context of the SIR model also demystified the daunting world of calculus while helping me develop a more solid understanding of differential equations. I am so excited to apply this understanding to other areas of life.

## Randomized Nearest Neighbor Algorithm + 2-Opt Swap

This is a Python code that contains several functions for solving the traveling salesman problem (TSP) using a randomized nearest neighbor algorithm followed by a 2-opt optimization algorithm. Here's a brief description of each function:

calculate_distance(city1, city2): Calculates the Euclidean distance between two cities given their coordinates.

calculate_distance_matrix(cities): Generates a distance matrix from a list of cities and their coordinates.

randomized_nearest_neighbor(cities, distance_matrix): Generates an initial route using the randomized nearest neighbor algorithm.

calculate_total_distance(route, distance_matrix): Calculates the total distance of a route given its distance matrix.

swap_cities(route, i, j): Swaps two cities in a route.

apply_2opt_swap(route, i, j): Applies the 2-opt swap to a route.

run_tsp(cities, num_iterations): Runs the TSP algorithm on a list of cities for a given number of iterations. This function prints out the initial route and distance, the randomized nearest neighbor route and distance, and the optimized route and distance, as well as the improvements achieved by the randomized nearest neighbor algorithm and the 2-opt optimization algorithm.

To use this module, you need to provide a list of cities and their coordinates. You also need to specify the number of iterations for the 2-opt optimization algorithm in the run_tsp function. Here's an example of how to use this module:

```
cities = [(0, 0), (1, 1), (2, 2), (3, 3), (4, 4)]
num_iterations = 1000
run_tsp(cities, num_iterations)

>>> Initial Route:  [12, 7, 10, 3, 6, 5, 0, 4, 13, 11, 2, 1, 8, 9, 14]
    Initial Distance:  1999.0005498593391 km

    Randomized Nearest Neighbor Route:  [0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 11, 10, 12, 13, 14]
    Randomized Nearest Neighbor Distance:  1042.1970100478286 km
    Improved by RNNA: - 956.8035398115105 km | In percentage:  47.86409587925509 %

    Optimized Route:  [0, 1, 2, 3, 10, 12, 13, 14, 11, 9, 8, 7, 6, 5, 4]
    Optimized Distance:  963.5770192510071 km
    Improved by 2-Opt Swap: - 78.61999079682153 km | In percentage:  7.543678406179029 %

```

This will run the TSP algorithm on a list of 5 cities with their coordinates (0,0), (1,1), (2,2), (3,3), and (4,4), for 1000 iterations of the 2-opt optimization algorithm.

## Euler's Method

This is a Python code for simulating the spread of an infectious disease using the SIR model and Euler's method. The code starts with importing the required libraries numpy and matplotlib. The code then sets font size and figure size for visualizations using matplotlib.

Next, the code defines a function named "SIR_Euler" that simulates the spread of a disease using the SIR model and Euler's method. The function takes four parameters: transmission rate, recovery rate, a list of initial values for S, I, and R, and the end time of the simulation. The function calculates the number of time steps and creates arrays to store the values of S, I, and R for each time step. The initial values for S, I, and R are set, and the total population size is calculated.

The function then iterates over each time step and calculates the new values for S, I, and R based on the SIR model equations. The function then generates a plot of S, I, and R over time using the matplotlib library.

The main code sets the parameters for Quezon City's outbreak using national statistics data, calls the "SIR_Euler" function to run, and generates a plot of S, I, and R over time. The x-axis represents time in days, and the y-axis represents the size of the population in each compartment (S, I, or R).
