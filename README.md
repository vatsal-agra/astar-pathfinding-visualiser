# A* Pathfinding Visualiser

An interactive visualisation of the A* search algorithm — watch the algorithm find the shortest path in real time, step by step.

## What It Does

The visualiser renders a grid where you can place a start point, an end point, and barriers. Once triggered, the A* algorithm runs and visually traces its exploration process — showing open nodes, closed nodes, and the final shortest path once found.

## How A* Works

A* is a best-first search algorithm that finds the shortest path between two points using a heuristic function. At each step it evaluates nodes using:

```
f(n) = g(n) + h(n)
```

Where:
- `g(n)` = cost from the start node to the current node
- `h(n)` = estimated cost from the current node to the goal (heuristic)
- `f(n)` = total estimated cost

This implementation uses a **priority queue (min-heap)** to always expand the lowest-cost node first, ensuring optimal pathfinding efficiency.

## Tech Stack

- **Python**
- **Pygame** — grid rendering and real-time visualisation
- **heapq** — priority queue implementation

## Key Concepts Demonstrated

- A* search algorithm
- Priority queues and min-heap data structures
- Heuristic design (Manhattan distance)
- Real-time algorithm visualisation

## How to Run

```bash
# Install dependencies
pip install pygame

# Run the visualiser
python astar_visualiser.py
```

## Controls

| Action | Input |
|--------|-------|
| Set start node | Left click (first click) |
| Set end node | Left click (second click) |
| Place barrier | Left click (subsequent clicks) |
| Remove node | Right click |
| Start algorithm | Press SPACE |
| Reset grid | Press C |

---

**Author:** Vatsal Agrawal  
**GitHub:** [github.com/vatsal-agra](https://github.com/vatsal-agra)  
**LinkedIn:** [linkedin.com/in/vatsal-agrawal-a7a9641b0](https://linkedin.com/in/vatsal-agrawal-a7a9641b0)
