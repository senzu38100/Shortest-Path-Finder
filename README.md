# Shortest path finder
--------------- Approach ---------------

The shortest path finder is implemented using the Breadth-First Search (BFS) algorithm, a fundamental graph traversal technique. The problem is modeled as a graph,
 where each cell in a maze is treated as a node, and edges exist between adjacent walkable cells.

The BFS algorithm works by expanding outward from the starting position, checking all reachable neighbors before moving further. This ensures that when the end 
node is reached, the discovered path is guaranteed to be the shortest.
Key Steps:

    Graph Representation: The maze is represented as a grid, where each cell is a node identified by its row and column coordinates.
    Queue-based Exploration: A First-In-First-Out (FIFO) queue is used to manage nodes that need to be explored.
    Expansion Process:
        The algorithm starts at the initial node and enqueues it.
        At each step, the front node in the queue is dequeued and its neighbors (up, down, left, right) are checked.
        If a neighbor is walkable and not yet visited, it is added to the queue.
        This process continues until the end node is found.
    Shortest Path Guarantee: Since BFS expands level by level, the first time the end node is reached, the path taken is the shortest one.
    Tracking the Path: To reconstruct the shortest path, a parent-tracking mechanism is used, linking each node to the node from which it was discovered.

By leveraging BFS and a queue structure, the algorithm efficiently finds the shortest path in an unweighted grid-based environment. The implementation ensures 
that all reachable nodes are processed in the order they are discovered, preventing redundant computations.
