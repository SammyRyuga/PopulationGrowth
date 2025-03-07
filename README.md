# Population Growth Simulation

## Overview
This C program simulates population growth over a specified number of days using a logistic growth model. It allows users to input parameters such as initial population, growth rate, carrying capacity, time step, and duration. Additionally, the user can specify a day on which the population is halved due to an external event.

## Features
- Uses the logistic growth equation:  
  \[ P(t + dt) = P(t) + dt \times k \times P(t) \times (1 - P(t) / K) \]
- Allows user input for various parameters.
- Prints a step-by-step simulation of the population over time.
- Implements an event where the population is halved on a user-specified day.
- Prevents invalid inputs through input validation.

## How It Works
1. The user is prompted to enter:
   - Initial population (must be positive).
   - Growth rate (must be positive).
   - Carrying capacity (must be greater than initial population).
   - Time step (dt, must be positive).
   - Duration (number of days to simulate, must be positive).
   - Event day when the population is halved (must be within the duration range).
2. The program then simulates population growth using the logistic equation.
3. It displays the population for each day.
4. If the specified event day occurs, the population is halved.
5. The simulation continues until the specified duration ends.

## Compilation and Execution
To compile and run the program, use the following commands:

```sh
gcc population_simulation.c -o population_simulation
./population_simulation
```

## Example Output
```
============================================
  Population Growth Simulation Setup
============================================
Enter initial population (positive): 100
Enter growth rate (positive): 0.1
Enter carrying capacity (must be > initial population): 1000
Enter time step (dt, positive): 1
Enter duration (days, positive): 10
Enter when population halves (between 1 and 10): 5

============================================
  Population Growth Simulation
============================================

 Day | Population
----------------------
  0  | 100.00
  1  | 109.00
  2  | 118.71
  3  | 129.18
  4  | 140.50
----------------------
 ** Event on Day 5: Population halved! **
----------------------
  5  | 70.25
  6  | 76.86
  7  | 84.02
  8  | 91.75
  9  | 100.08
 10  | 109.04

============================================
  Simulation Complete!
============================================
```

## Notes
- The logistic growth model is used to represent population growth with environmental constraints.
- The time step (dt) influences the accuracy of the simulation.
- The event feature allows simulation of sudden population reductions.
- Negative population values are prevented by setting the minimum population to zero.

## License
This project is open-source and free to use under the MIT License.

## Author
Developed by Samanyu Pattanayak
