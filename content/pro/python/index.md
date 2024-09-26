---
title: Python 
summary: A curated collection of my Python projects demonstrating technical skills and practical applications.
date: 2023-10-24
type: docs
math: false
tags:
  - Python 3
  - Karel 
  - Programming
image:
  caption: 'Python'
---

# Python Projects Showcase

Welcome to my **Python Projects Showcase**! This portfolio features a selection of my projects developed using Python at Stanford University, illustrating my capabilities in software design, algorithm development, and simulation.

---

## 1: Pendulum-Projectile Simulation on Solar Planets
- **Description:** A sophisticated simulation that combines the dynamics of pendulum motion with projectile motion in a solar system context.
- **Course:** Stanford University CS106A (2023)
- **Technologies Used:** Python 3, Pygame
- **Key Features:**
  - Realistic simulation of pendulum and projectile dynamics.
  - Visualization of gravitational interactions with different planetary bodies.
- **Visuals:**
  ![Pendulum-Projectile Simulation](pendulum_projectile_simulation.png)
- **Project Repository:** [View Project](your_project_link_here)

---

## 2: Finite Difference Method (FDM) for Heat Transfer
- **Description:** Developed a simulation tool implementing the Finite Difference Method to solve heat transfer problems.
- **Course:** Stanford University CS106A (2023)
- **Technologies Used:** Python 3, NumPy
- **Key Features:**
  - Accurate numerical solutions for heat distribution over time.
  - Graphical representation of simulation results for analysis.
- **Visuals:**
  ![FDM Heat Transfer](fdm_heat_transfer.png)
- **Project Repository:** [View Project](your_project_link_here)

---

## 3: Karel Robot (7 Mini Projects)
- **Description:** A series of seven mini-projects utilizing the Karel Robot programming environment to introduce fundamental programming concepts.
- **Course:** Stanford University CS106A (2023)
- **Key Features:**
  - Hands-on programming exercises including maze navigation and object manipulation.
  - Emphasis on logical thinking and problem-solving skills.
- **Projects:**
  - Beyond Fill Karel
  - Checkerboard Karel
  - Fill Karel
  - Jigsaw Karel
  - Piles
  - Spread Beepers
  - Stone Mason Karel
- **Visuals:**
  ![Karel Robot Projects](karel_robot_projects.png)
- **Project Repository:** [View Projects](your_project_link_here)

```python
    ### Example Code:
from karel.stanfordkarel import *

def main():
    """
    Karel moves along a row, painting each corner randomly with blue or red.
    Then, Karel returns to the starting position.
    """
    while front_is_clear():
        paint_random_corner()
        move()
    paint_random_corner()
    return_to_start()

def paint_random_corner():
    if random():
        paint_corner("blue")
    else:
        paint_corner("red")

def return_to_start():
    turn_around()
    while front_is_clear():
        move()
    turn_around()

def turn_around():
    for _ in range(2):
        turn_left()

if __name__ == '__main__':
    main()
    ```

---

## 4: Graph Simulator
- **Description:** A versatile graph simulation tool that allows users to visualize and manipulate graph structures interactively.
- **Course:** Stanford University CS106A (2023)
- **Technologies Used:** Python 3, Matplotlib
- **Key Features:**
  - Interactive UI for adding and removing nodes and edges.
  - Visualization of graph algorithms in real-time.
- **Visuals:**
  ![Graph Simulator](graph_simulator.png)
- **Project Repository:** [View Project](your_project_link_here)

---

## 5: Games
- **Description:** A collection of engaging mini-games developed using Python, showcasing programming logic and design principles.
- **Course:** Stanford University CS106A (2023)
- **Technologies Used:** Python 3, Pygame
- **Key Features:**
  - Includes various game genres: puzzles, arcade, and strategy.
  - Focus on user experience and gameplay mechanics.
- **Visuals:**
  ![Games Collection](games_collection.png)
- **Project Repository:** [View Projects](your_project_link_here)

---

## Conclusion

Thank you for exploring my Python Projects Showcase! I am dedicated to continuous learning and improvement in software development. If you have any questions or feedback, please feel free to reach out.
