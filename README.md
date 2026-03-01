# Informed-Searches-Dynamic-Pathfinding-Agent
Dynamic Pathfinding Agent
This project is a real-time, interactive pathfinding visualizer built with Python and Pygame. 
It allows users to observe how different search algorithms navigate a grid, manage obstacles, and adapt to live environment changes.

Core Features
Algorithm Options: Switch between A* (Optimal) and Greedy Best-First Search (Heuristic-focused).

Dual Heuristics: Toggle between Manhattan Distance and Euclidean Distance for path calculation.

Dynamic Obstacles: Enable a mode where random walls appear during the search process to test agent adaptability.

Real-time Metrics: Track nodes visited, total path cost, and execution time in milliseconds.

Maze Generation: Automatically generate a random layout with 30% obstacle density.

Scalable UI: Fully resizable window with a dedicated sidebar for control instructions and statistics.
Installation and Setup
Requirement: Ensure Python 3.x is installed on your system.

Dependency: Install the Pygame library using the following command:
pip install pygame

Execution: Run the script using python filename.py.
User Controls
Left Click (First): Place the Blue Start node.

Left Click (Second): Place the Purple Goal node.

Left Click (Drag): Draw Black walls/obstacles.

A Key: Toggle between A* and GBFS algorithms.

H Key: Toggle between Manhattan and Euclidean heuristics.

D Key: Toggle Dynamic Mode (Obstacles appear during search).

G Key: Generate a random maze.

C Key: Clear the grid and reset all metrics.

SPACE Key: Begin the pathfinding visualization.
Logic and Mathematical OverviewSearch Mechanism: The agent uses a priority queue ($heapq$) to evaluate which node to explore next.Evaluation Function: The cost of a node is calculated using the formula:$$f(n) = g(n) + h(n)$$Cost ($g$): The actual distance from the start node to the current node.Heuristic ($h$): The estimated distance from the current node to the goal.Heuristic Types:Manhattan: $|x_1 - x_2| + |y_1 - y_2|$ (Ideal for 4-direction movement).Euclidean: $\sqrt{(x_1 - x_2)^2 + (y_1 - y_2)^2}$ (Straight-line distance).

Visual Indicators
Blue: Starting position.

Purple: Target destination.

Black: Non-traversable walls.

Red: Nodes that have been fully evaluated (Closed Set).

Yellow: Nodes currently being considered (Open Set/Frontier).

Green: The final calculated shortest path.
