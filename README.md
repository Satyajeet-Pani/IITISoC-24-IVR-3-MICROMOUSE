# IITISoC-24-IVR-3-MICROMOUSE

## GOAL
To develop a maze solving micromouse with hardware integration using simulation

People Involved : 

Mentors:
- [Ampady B R](https://github.com/ampady06)
- [Bhawna Chaudhary](https://github.com/WebWizard104)

Members:
- [Khush Paliwal](https://github.com/KhushPaliwal22)
- [Daksh Chandel](https://github.com/DC-005)
- [Satyajeet Pani](https://github.com/Satyajeet-Pani)

## Initial plan:

1) Algorithm:  To try out and find the best algorithm for our micromouse and simulate it in [mms](https://www.bing.com/ck/a?!&&p=1edceb3b1ea7a884JmltdHM9MTcyMjAzODQwMCZpZ3VpZD0zZmRlMmI3Yi03MDc0LTZlMWMtMzdhNC0zZmIyNzFjNjZmNTgmaW5zaWQ9NTQ0Ng&ptn=3&ver=2&hsh=3&fclid=3fde2b7b-7074-6e1c-37a4-3fb271c66f58&psq=mms+simulator&u=a1aHR0cHM6Ly9naXRodWIuY29tL21hY2tvcm9uZS9tbXM&ntb=1)
2) Hardware: To find the most suitable and optimal hardware for our micromouse according to the requirements and rules.
3) Optimizations: If time allows, to optimize the movement of our mouse.

## Algorithm:

#### Breadth-first search:
It involves visiting all the connected nodes of the maze in a level-by-level manner.

https://github.com/user-attachments/assets/60136948-c322-4cfd-9356-9ca11ac03a63

#### Dijkstra's Algorithm:
It is an algorithm for finding the shortest paths between nodes in a weighted graph, which may represent, for example, road networks.

https://github.com/user-attachments/assets/db69f580-81a4-49ad-94b2-37b5b7e51606

#### A* Algorithm:
It is a graph traversal and pathfinding algorithm. A* achieves better performance by using heuristics to guide its search.

https://github.com/user-attachments/assets/170ab3f5-f571-4c94-829b-5c1b3f4d2726

#### Floodfill:
This algorithm calculates the manhattan distances of each cell from the center and makes the mouse move towards the smallest distance from the cell choices it has.
Our mouse doesn't know about the maze wall placements at the starting, so this algorithm dynamically adapts and calculates new distances as soon as the mouse finds a new/undiscovered wall.

https://github.com/user-attachments/assets/f6ae22c9-d815-4f70-b8fa-f30443e4d3fa

We finalised this algorithm for our micromouse as it dynamically adapts to the maze and ensures the shortest path when run for a couple of times.

Next we added return trips to the algorithm as the rules state that the mouse has to return to the start on it's own. This return trip is again utilised by our mouse to find a better path.

https://github.com/user-attachments/assets/c8d6f2ea-c621-45a4-bb10-a4c585f78ac6

##### Algorithm --- Floodfill

## Hardware:
Once we were done with selection of an algorithm, our next step was to look out for the best hardware that we could put in our micromouse.








