# A* Pathfinding Visualization

This project provides an interactive web-based visualization of the A* pathfinding algorithm implemented using HTML, CSS, and vanilla JavaScript. Users can create a grid environment with obstacles, define start and end points, and watch the A* algorithm find the shortest path between them.

Check out my [Visusal Implementation](https://fnxdoom.github.io/A-star/)
<!-- ![A* Visualization Screenshot](path/to/your/screenshot.png) -->

## Features

*   **Interactive Grid:** A 15x10 grid where users can visualize the pathfinding process.
*   **Obstacle Placement:** Click on cells to add or remove obstacles (represented by black blocks).
*   **Custom Start/End Points:** Use dedicated buttons ("Set Start Point", "Set End Point") to designate the start ('S') and end ('E') points by clicking on the grid.
*   **A* Algorithm Implementation:** Finds the shortest path using the A* search algorithm, considering 8-directional movement (including diagonals).
*   **Step-by-Step Visualization:**
    *   Animates the algorithm's exploration process, highlighting visited nodes (yellow).
    *   Draws the final shortest path found (blue).
*   **Control Options:**
    *   `Find Path`: Runs the A* algorithm from the current start to the end point.
    *   `Reset Grid`: Clears all obstacles, path visualization, and resets start/end points to their default positions.
    *   `Clear Path`: Removes only the visualized path and visited nodes, keeping obstacles and start/end points intact.
    *   `Random Obstacles`: Populates the grid with a random selection of obstacles (approximately 30% density).
*   **Informative Feedback:** An information bar provides user guidance and status updates (e.g., "Finding path...", "Path found!", "No path found!").
*   **Visual Legend:** Clearly explains the meaning of different cell colors (Empty, Obstacle, Start, End, Visited, Path).

## How to Use

1.  **Save the Code:** Save the provided HTML code (which includes the CSS and JavaScript) as an `.html` file (e.g., `astar_visualization.html`).
2.  **Open in Browser:** Open the saved HTML file in your preferred web browser (like Chrome, Firefox, Safari, Edge).
3.  **Interact with the Grid:**
    *   The grid will initialize with default start (S) and end (E) points.
    *   Click on any empty cell to toggle it as an obstacle (black). Clicking an obstacle removes it. You cannot place obstacles on the start or end points.
    *   To change the start point: Click the "Set Start Point" button, then click on the desired cell in the grid.
    *   To change the end point: Click the "Set End Point" button, then click on the desired cell in the grid.
4.  **Generate Obstacles (Optional):** Click the "Random Obstacles" button to quickly create a maze-like environment.
5.  **Find the Path:** Click the "Find Path" button.
6.  **Observe:** Watch as the algorithm explores potential paths (yellow cells) and then highlights the shortest path found (blue cells). The info bar will indicate if a path was found and its length.
7.  **Reset or Clear:**
    *   Use "Clear Path" if you want to run the algorithm again with the same obstacles but perhaps different start/end points or just clear the visualization.
    *   Use "Reset Grid" to start completely fresh with the default setup.

## Technical Details

*   **Algorithm:** A* Search Algorithm
*   **Heuristic:** Manhattan distance (`h = |x1 - x2| + |y1 - y2|`)
*   **Movement:** Allows 8-directional movement (horizontal, vertical, and diagonal).
    *   Cost for horizontal/vertical movement: 1
    *   Cost for diagonal movement: `sqrt(2)` (approximated as 1.4)
*   **Implementation:** Pure HTML, CSS, and JavaScript. No external libraries or frameworks are required.
*   **Grid Representation:** A 2D JavaScript array (`grid`) stores the state of each cell (0 for walkable, 1 for obstacle).
*   **Visualization:** DOM manipulation is used to update the `className` of grid cells, applying CSS styles for different states (obstacle, start, end, visited, path). `setTimeout` is used for animation delays.

## Possible Future Improvements

*   Adjustable grid size.
*   Different heuristic options (e.g., Euclidean, Diagonal Distance).
*   Control over animation speed.
*   Support for weighted nodes (e.g., different terrain costs like 'mud' or 'water').
*   Visual display of g, h, and f costs on cells during visualization (optional toggle).
