# IITISoC-24-IVR-3-MICROMOUSE

## GOAL
To develop a maze solving micromouse with hardware integration using simulation

People Involved : 

Mentors:
- [Ampady B R](https://github.com/ampady06)
- [Bhawna Chaudhary](https://github.com/WebWizard104)

Members:
<br>
- [Khush Paliwal](https://github.com/KhushPaliwal22)
- [Daksh Chandel](https://github.com/DC-005)
- [Satyajeet Pani](https://github.com/Satyajeet-Pani)

The micromouse competition consists of a 16 x 16 maze which the robot (mouse) has to solve without having any pre-knowledge of the maze, the goal is the center.
We started our work by investigating about different maze solving algorithms - bfs, dfs, A*, dijkstra's and floodfill. The files for these algorithms can be found in the repo.
From the simulation using [mms](https://www.bing.com/ck/a?!&&p=1edceb3b1ea7a884JmltdHM9MTcyMjAzODQwMCZpZ3VpZD0zZmRlMmI3Yi03MDc0LTZlMWMtMzdhNC0zZmIyNzFjNjZmNTgmaW5zaWQ9NTQ0Ng&ptn=3&ver=2&hsh=3&fclid=3fde2b7b-7074-6e1c-37a4-3fb271c66f58&psq=mms+simulator&u=a1aHR0cHM6Ly9naXRodWIuY29tL21hY2tvcm9uZS9tbXM&ntb=1) we found that the best algorithm for a micromouse is floodfill(Works as if water flows from the center to the start) as it dynamically adapts to the maze and finds the shortest path. 
Why we needed dynamic programming in this? 
Since we have no prior knowledge of the maze, the walls are unknown to us and as the mouse explores the maze, we get to know about the walls. Floodfill approach dynamically adapts to the news walls found and calculates the manhattan distances again to find the path. In this competition we have to reach the goal and return to start through the maze, floodfill approach utilizes this to find a new better path(if available) with the data of walls from previous run. You will see the floodfill algorithm with multiple runs in this repo. Also we added some weights to find straighter path where it makes the mouse faster (find the file attached).
Once our algorithm was final, the next step was hardware.
After some research we locked our choices on the following components, 
Microcontroller - STM32F103C8T6
Motor - N20 12mm micro gearmotors
Motor driver - TB6612FNG Dual H-bridge motor driver
IR and Ultrasonic sensors
3.7V Li-ion cell.
After acquiring these hardware, one can start with the implementation of micromouse.
