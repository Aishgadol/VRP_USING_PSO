# Vehicle Routing with Particle Swarm Optimization

This repository contains a simple implementation of the Vehicle Routing Problem (VRP) solved with Particle Swarm Optimization (PSO). It parses benchmark files containing customer coordinates and travel times, optimizes the assignment and ordering of locations for multiple vehicles, and visualizes the resulting routes.

## Goals and Objectives

- Parse VRP datasets with coordinates and time matrices.
- Use PSO to assign each location to a vehicle and determine the visit order.
- Minimize a combined objective of travel distance and time.
- Visualize routes and print per vehicle and total statistics.

## Architecture

- **`VRP.py`** – Handles dataset parsing, distance/time matrix computation and utility functions for route evaluation and visualization.
- **`pso.py`** – Generic PSO implementation used to optimize discrete assignments.
- **`main.py`** – Example script that loads a dataset (defaults to `Ex3-d33`), sets PSO hyper‑parameters and runs the optimization.
- **`Ex1-d5`, `Ex2-d22`, `Ex3-d33`** – Example VRP files containing coordinates and travel‑time tables.

## Installation

1. Clone the repository.
2. Create a Python environment (recommended Python ≥3.8).
3. Install dependencies:

```bash
pip install -r requirements.txt
```

No other system requirements are needed. A display or notebook environment is required to view matplotlib plots.

## Usage

Run the example optimization:

```bash
python main.py
```

`main.py` contains several tunable parameters at the top of the file such as `SWARM_SIZE`, `MAX_ROUTES`, and `MAX_ITER`. Modify them to experiment with different settings or datasets.

The script outputs the best discrete assignments and prints route statistics. After running, a matplotlib window shows the computed routes.

## Expected Results

Running `main.py` produces console output with each vehicle's route, distance, and time, for example:

```
vehicle 1 route: depot -> 3 -> 7 -> 2 -> depot
Distance for vehicle 1 r_distance=12.3, Time traveled = 15.0
...
Total Distance is: 56.1, Total Time = 70.3
longest route: 20.1, route that takes longest time: 25.7
```

A plot visualizing each route is also displayed. No files are written by default.

## Development and Contribution

The project does not include automated tests yet, but new features or bug fixes are welcome. Standard pull‑requests are recommended. Style is simple PEP‑8 compliant Python. Tests can be added with `pytest`.

## Project Status and Roadmap

This is experimental/alpha code demonstrating PSO for VRP. Possible improvements include:

- Command‑line interface for selecting datasets and hyper‑parameters.
- More advanced initialization and velocity update rules.
- Additional benchmark datasets and unit tests.

## License

No explicit license is provided. We suggest releasing the code under the MIT License or another OSI‑approved license if distributing publicly.

