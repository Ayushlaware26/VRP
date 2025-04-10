# Vehicle Routing Problem Solver using Genetic Algorithm

This project implements a solution to the Vehicle Routing Problem (VRP) using a Genetic Algorithm approach. The implementation optimizes routes for multiple vehicles to serve a set of locations while minimizing the total distance traveled and balancing the workload among vehicles.

## Problem Description

The Vehicle Routing Problem (VRP) involves:
- A central depot (located at coordinates (0,0))
- Multiple delivery locations (randomly generated within -100 to 100 coordinate range)
- A fleet of vehicles (4 vehicles in this implementation)
- The goal is to find optimal routes for each vehicle while:
  - Minimizing the total distance traveled
  - Balancing the workload among vehicles
  - Ensuring all locations are visited exactly once

## Features

- Random generation of delivery locations
- Multi-objective optimization:
  - Minimizes total route distance
  - Balances workload across vehicles
- Visualization of routes using matplotlib
- Genetic Algorithm implementation using DEAP library
- Configurable parameters for GA optimization

## Requirements

```
deap
matplotlib
numpy
jupyter
```

## Installation

1. Clone this repository
2. Install the required packages:
```bash
pip install -r requirements.txt
```

## Usage

The solution is implemented in a Jupyter notebook (`vehicleRoutingProblem-Solution.ipynb`). To use:

1. Open the notebook in Jupyter Lab/Notebook
2. Run all cells sequentially
3. The final cell will execute the genetic algorithm and display the optimized routes

## Implementation Details

### Genetic Algorithm Components

1. **Individual Representation**: 
   - Permutation of location indices
   - Each individual represents a complete solution for all vehicles

2. **Fitness Function**:
   - Evaluates total distance traveled
   - Includes penalty for unbalanced vehicle loads
   - Uses Euclidean distance for route calculations

3. **Genetic Operators**:
   - Crossover: Partially Matched Crossover (PMX)
   - Mutation: Shuffle Index Mutation
   - Selection: Tournament Selection

### Parameters

- Number of locations: 20
- Number of vehicles: 4
- Population size: 300
- Number of generations: 300
- Crossover probability: 0.7
- Mutation probability: 0.2

## Visualization

The solution includes visualization of:
- All delivery locations (blue dots)
- Central depot (red square)
- Optimized routes for each vehicle (different colored lines)

## Results

The genetic algorithm optimizes routes by:
1. Minimizing the total distance traveled by all vehicles
2. Balancing the workload among vehicles
3. Ensuring all locations are visited exactly once

## License

This project is open source and available under the MIT License.

## Contributing

Feel free to fork this repository and submit pull requests for any improvements.
