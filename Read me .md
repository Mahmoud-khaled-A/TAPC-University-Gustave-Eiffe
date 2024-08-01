# TAPC Transportation Optimization

This repository contains the implementation of a Mixed Integer Linear Programming (MILP) model to optimize the number of vehicles required for a new premium public transportation service in Paradise City. The objective is to determine the minimum number of vehicles needed to handle any demand scenario within a 30% delay of the shortest path travel time.

## Problem Overview

The transportation network is represented as a graph where:
- `V` is the set of all stations.
- `T` is the set of time periods.
- `D` is the total demand.
- `C` is the vehicle capacity.
- `W` is the travel duration for each arc.
- `d` is the shortest path travel time between stations.

The service must satisfy all demands for each time period with a delay no greater than 30% of the direct trip time.

## Model Description

The MILP model aims to minimize the number of vehicles required while satisfying all demand and delay constraints.

### Objective
Minimize the number of vehicles \( N \).

### Constraints
1. **Demand satisfaction**: Ensure each vehicle can transport all passengers within the allowable delay.
2. **Capacity constraints**: Ensure the number of passengers in each vehicle does not exceed its capacity.
3. **Total passenger constraint**: Ensure the sum of passengers across all vehicles does not exceed the total demand.
4. **Delay constraint**: Ensure the travel time for each vehicle is within 1.3 times the shortest path travel time.

## Files in this Repository

-  `TAPC-University-Gustave-Eiffel.py`: The Python script containing the MILP formulation and solution using CPLEX.

- `README.md`: This file.

## Usage Instructions

### Requirements
- IBM ILOG CPLEX Optimization Studio
- docplex Python library
