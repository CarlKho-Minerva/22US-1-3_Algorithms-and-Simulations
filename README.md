# CarlKho-Minerva--22US-1-3_Algorithms-and-Simulations

# Randomized Nearest Neighbor Algorithm + 2-Opt Swap

This is a Python module that contains several functions for solving the traveling salesman problem (TSP) using a randomized nearest neighbor algorithm followed by a 2-opt optimization algorithm. Here's a brief description of each function:

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
