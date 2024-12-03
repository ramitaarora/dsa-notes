# Graph Traversals

To enable searching, we add vertices to a list, visited. This list is pretty important because it keeps the search from visiting the same vertex multiple times! This is particularly vital for cyclical graphs where you might otherwise end up in an infinite loop.

Calculating runtime: In an upper bound scenario, we would be looking at every vertex and every edge. Because of this, the big O runtime for both depth-first search and breadth-first search is O(vertices + edges).

## Depth-First Search
- Simply put, a depth-first graph search continues down a path until it reaches the end. 
- It is helpful for determining if a path exists between two vertices. 
- DFS has many applications, including topological sorting and detecting cycles, but one of the more interesting real-world applications is that it can be used to solve problems that have a singular correct answer (a path between the start state and end state), such as a sudoku exercise.
- In order to accomplish this path-finding feat, DFS implementations use either a <b>stack</b> data structure or, more commonly, <b>recursion</b> to keep track of the path the search is on and the current vertex.
- In a stack implementation, the most recently added vertex is popped off the stack when the search has reached the end of the path. Meanwhile, in a recursive implementation, the DFS function is recursively called for each connected vertex.
- Depth-first search is pretty adept at organizing vertices (or vertex values) with a clear order of visitation from beginning to end.
    - Preorder, in which each vertex is added to the “visited” list and added to the output list BEFORE getting added to the stack
    - Postorder, in which each vertex is added to the “visited” list and added to the output list AFTER it is popped off the stack
    - Reverse Post-Order (also known as Topological Sort), which returns an output list that is exactly the reverse of the post-order list

## Breadth-First Search
- On the other hand, a breadth-first graph search approach checks the values of all neighboring vertices before moving into another level of depth. 
- This is an incredibly inefficient way to find just any path between two vertices, but it’s an excellent way to identify the shortest path between them. 
- Because of this, BFS is helpful for figuring out directions from one place to another.
- Unlike DFS, BFS graph search implementations use a <b>queue</b> data structure to keep track of the current vertex and vertices that still have unvisited neighbors. In BFS graph search a vertex is dequeued when all neighboring vertices have been visited.

## Summary

- You can use a graph search algorithm to traverse the entirety of a graph data structure to locate a specific value
- Vertices in a graph search include a “visited” list to keep track of whether or not each vertex has been checked
- Depth-first search (DFS) and breadth-first search (BFS) are two common approaches to graph search
- The runtime for graph search algorithms is O(vertices + edges)
- DFS, which employs either recursion or a stack data structure, is useful for determining whether a path exists between two points
- BFS, which generally relies on a queue data structure, is helpful in finding the shortest path between two points
- There are three common traversal orders which you can apply with DFS to generate a list of all values in a graph: pre-order, post-order, and reverse post-order