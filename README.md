# TnP\_Lab11



Questions:

How does each pathfinding algorithms calculate and prioritize paths?



A\* pathfinding calculates costs for each node within a navigable area and then assesses the total cost of possible paths to a goal to find the lowest cost, or shortest, path. Dijkstra's algorithm does a breadth-first search on a weighted graph, while a typical Breadth-First-Search checks all possible paths from the start to find a path to the goal. A\* and Dijkstra guarantee the shortest path to the goal, while BFS only can do so on an unweighted graph.



What challenges arise when dynamically updating obstacles in real-time?



When dynamically updating obstacles in real-time, it seems that the algorithms, at least BFS, will dead-end if a new obstacle is placed along the already-found path, even if there are other potential options to get to the end.



Which algorithm should you choose and how should you adapt it for larger grids or open-world settings?



A\* is the best and fastest algorithm as it combines the heuristics of both BFS and Dijkstra. It is also much faster than both of these algorithms. In larger grids or open-world settings, you could break down the navigable area into smaller sub-areas so that pathfinding agents do not have to do pathfinding searches over a massive area. You could simply enable or disable their pathfinding when the goal enters and leaves their subarea.



What would your approach be if you were to add weighted cells (e.g., "difficult terrain" areas)?



You could add weighted cells to A\* pathfinding by taking the standard 1 cost for each movable cell and add in a custom weight for all non-obstacle cells. You could then set the cost for certain "difficult terrain" cells to a higher value, such as 2, as this would make them increase the cost of the overall evaluated path and make those routes more costly to be shortest.

