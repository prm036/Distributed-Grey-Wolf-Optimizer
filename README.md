# Workflow Scheduling in Cloud Using DGWO

This project addresses the task scheduling problem in cloud environments using the Discrete Grey Wolf Optimizer (DGWO) algorithm.  It focuses on efficiently assigning dependent workflow tasks to virtual machines (VMs) in order to minimize computation and data transmission costs.

## Objective

The main goal is to optimize the execution of workflows on the cloud by:
- Minimizing the total execution time(makespan).
- Reducing data transfer costs between VMs
- Improving overall resource utilization

## Why DGWO?

Workflow scheduling in cloud is an NP-hard problem, meaning it's computationally hard to find optimal solutions, especially at scale. Traditional algorithms like:
- Particle Swarm Optimization (PSO)
- Simulated Annealing (SA)
- Genetic Algorithms (GA)

often struggle with medium to large-sized problems.

The DGWO algorithm, inspired by the hunting behavior of grey wolves, addresses these challenges by:
- Efficiently exploring the search space
- Dynamically adjusting search parameters
- Handling both balanced and imbalanced workflow types

## How It Works

1. **Initialization**: A population of "wolves" (candidate solutions) is created.
2. **Fitness Evaluation**: Each solution is scored based on  and communication costs.
3. **Search Strategy**:
   - Alpha, beta, and delta wolves guide the search (best solutions).
   - Omega wolves explore new possibilities.
4. **Migration**: Use an island model to distribute solutions and periodically exchange the best ones.
5. **Termination**: After several iterations, return the best solution.

## Tools & Technologies

- **Language**: Java
- **Platform**: Cloud-simulated environment using random task/VM configurations

## Results

The DGWO algorithm was compared against GWO and PSO on both balanced and imbalanced workflows. DGWO consistently outperformed the others in terms of:
- Makespan reduction
- Adaptability
- Scalability

## Future Improvements

- Extend to multi-objective optimization
- Improve convergence speed with adaptive parameters
