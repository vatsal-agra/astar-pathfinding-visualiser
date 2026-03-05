# A* Pathfinding Visualiser

An interactive real-time visualisation of the A* search algorithm — place a start, an end, and barriers on a grid, then watch A* find the shortest path step by step.

## What It Does

You build a grid scenario by placing a start node, an end node, and barrier nodes. Once triggered, the A* algorithm runs visually — showing open nodes (green), closed/explored nodes (red), and the final shortest path (purple) once found.

## How A* Works

A* is a best-first search algorithm that finds the shortest path using both actual cost and a heuristic estimate:

```
f(n) = g(n) + h(n)
```

Where:
- `g(n)` = actual cost from start to current node
- `h(n)` = estimated cost from current node to goal (Manhattan distance heuristic)
- `f(n)` = total estimated path cost

This implementation uses a **PriorityQueue** to always expand the lowest f-score node first, guaranteeing the optimal shortest path.

## Tech Stack

- **Python**
- **Pygame** — grid rendering and real-time visualisation
- **PriorityQueue (heapq)** — efficient node ordering for A*

## Key Concepts Demonstrated

- A* search algorithm with Manhattan distance heuristic
- Priority queue for optimal node selection
- Real-time algorithm step visualisation
- Barrier placement for custom maze scenarios
- Path reconstruction via came_from tracking

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
| Place start node | Left click (1st click) |
| Place end node | Left click (2nd click) |
| Place barrier | Left click (subsequent clicks) |
| Remove node/barrier | Right click |
| Run A* algorithm | Press SPACE |
| Reset grid | Press C |

## Color Guide

| Color | Meaning |
|-------|---------|
| 🟠 Orange | Start node |
| 🩵 Turquoise | End node |
| ⬛ Black | Barrier |
| 🟢 Green | Open (to be explored) |
| 🔴 Red | Closed (already explored) |
| 🟣 Purple | Final shortest path |

---

**Author:** Vatsal Agrawal  
**GitHub:** [github.com/vatsal-agra](https://github.com/vatsal-agra)  
**LinkedIn:** [linkedin.com/in/vatsal-agrawal-a7a9641b0](https://linkedin.com/in/vatsal-agrawal-a7a9641b0)
