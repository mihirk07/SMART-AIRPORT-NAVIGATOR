SMART-AIRPORT-NAVIGATOR

Smart Airport Navigator (A* Pathfinding)
An intelligent, graph-based navigation system designed for large airports. This project uses the A* Search Algorithm to compute the most efficient walking routes between airport locations, considering real-world factors like stairs, distance, and accessibility.



OVERVIEW:

Navigating large airports can be confusing and time-consuming. Traditional maps do not always provide optimized walking routes or consider accessibility needs.
Smart Airport Navigator converts an airport layout into a state-space graph, where:
Locations (like gates, lounges, counters) are nodes
Paths between them are weighted edges
Using a cost-sensitive approach, the system calculates the shortest and most efficient route between any two points (e.g., from entrance to boarding gate), while adjusting for real-world conditions such as stairs.



AI CONCEPTS APPLIED:

Graph Theory

Airport locations are represented as nodes, and walkways are edges with weights.
Informed Search (A*) Algorithm

Uses the evaluation function:
f(n) = g(n) + h(n)
where:
g(n): actual path cost
h(n): heuristic estimate to goal
Heuristic Function
Uses Euclidean Distance to ensure optimal pathfinding.
Cost Function Optimization
Edge weights are dynamically adjusted:
Flat paths → normal cost
Stairs → 1.5× cost multiplier



TECH STACK:

Language: Python 3.x

Graph Library: NetworkX (for graph creation & A* algorithm)

Visualization: Matplotlib (for map rendering)

Math: Python math module (distance calculation)



AIRPORT MAP NODES:

The system maps key airport locations including:

-Entry/Exit

-Main Entrance

-Exit Terminal

-Processing Area

-Ticketing Office

-Check-In Counter

-Security Check

-Immigration

-Facilities

-Food Court

-Duty Free Shop

-Medical Room

-Information Desk

-Lounge

-Boarding Gates

-Boarding Gate A

-Gate B, C, D, E



RESULTS:

The system generates a visual airport map where:

-Gray Nodes: Airport locations

-Black Lines: Flat walking paths

-Red Dashed Lines: Stairs (higher cost paths)

-Red Nodes: Selected path locations

-Blue Path: Optimal route calculated by A*

-Distance Calculation:

-Total weighted distance (in meters) is displayed in the window title.



HOW TO RUN THE PROJECT:

Follow these steps to execute the navigator on your system:

1. Prerequisites
Ensure Python 3.7 or higher is installed:
Bash
python --version

2. Install Required Libraries
Bash
pip install networkx matplotlib

3. Run the Script
Bash
python your_file_name.py

4. Provide Input
Enter the start and destination points:

Start_point: Main_Entrance

End_point: Boarding_Gate_A

5. Output Window
A visualization window will appear showing:
The airport layout
Highlighted optimal path
Total distance



VISUALIZATION DETAILS:

-Light Grey Nodes: All airport landmarks

-Red Nodes: Nodes in the selected path

-Black Edges: Standard flat paths

-Red Dashed Edges: Stairs (higher cost)

-Blue Line: Optimal route



KEY FEATURES:

-Realistic airport navigation model

-Supports accessibility-aware routing

-Visual path representation

-Dynamic cost adjustment (stairs vs flat)

-Efficient A* pathfinding
