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

---
## Finite Difference Method (FDM) for Heat Transfer
summary: Numerical solution of heat transfer problems using the Finite Difference Method.
date: 2023-10-24
type: docs
math: true
tags:
  - Python
  - Projects
  - Programming
  - Heat Transfer
image:
  caption: 'Finite Difference Method for Heat Transfer'

## Finite Difference Method (FDM) for Heat Transfer

### Overview

The Finite Difference Method (FDM) is a powerful numerical technique for solving partial differential equations, particularly useful for analyzing heat transfer problems. This project demonstrates the application of FDM to model the heat distribution in solid bars, integrating both heat transfer and structural deflection analysis.

---

### Algorithm

1. **Define the Problem:**
   - Consider the heat equation:
   {{< math >}}
   $$ 
   \frac{\partial u}{\partial t} = \alpha \frac{\partial^2 u}{\partial x^2} 
   $$
   {{< /math >}}
   - \( u \): Temperature at a point in space and time.
   - \( \alpha \): Thermal diffusivity.

2. **Discretization:**
   - Divide the spatial domain into \( n \) points \( x_1, x_2, \ldots, x_n \).
   - Divide the time domain into \( m \) steps \( t_1, t_2, \ldots, t_m \).

3. **Finite Difference Approximations:**
   - Use the forward difference for the time derivative and the central difference for the spatial derivative:
   {{< math >}}
   $$ 
   \frac{u_{i}^{n+1} - u_{i}^{n}}{\Delta t} = \alpha \frac{u_{i+1}^{n} - 2u_{i}^{n} + u_{i-1}^{n}}{\Delta x^2} 
   $$
   {{< /math >}}

4. **Update Temperature Iteratively:**
   - Rearrange the equation to compute the temperature at each point:
   {{< math >}}
   $$ 
   u_{i}^{n+1} = u_{i}^{n} + \frac{\alpha \Delta t}{\Delta x^2} (u_{i+1}^{n} - 2u_{i}^{n} + u_{i-1}^{n}) 
   $$
   {{< /math >}}

5. **Boundary and Initial Conditions:**
   - Set initial temperature distribution and define boundary conditions (e.g., fixed temperature or insulated ends).

6. **Stiffness Matrix (for Structural Analysis):**
   - The stiffness matrix \( \mathbf{K} \) relates forces and displacements in the system:
   {{< math >}}
   $$ 
   \mathbf{F} = \mathbf{K} \mathbf{u} 
   $$
   {{< /math >}}
   - For a 1D bar element:
   {{< math >}}
   $$ 
   \mathbf{K} = \frac{EA}{L} \begin{bmatrix} 1 & -1 \\ -1 & 1 \end{bmatrix} 
   $$
   {{< /math >}}
   - Where \( E \) is Young's modulus, \( A \) is the cross-sectional area, and \( L \) is the length.

---

### Conclusion

Through this project, I successfully implemented the FDM to simulate heat transfer in solid bars while considering structural deflections. The mathematical framework and algorithmic approach not only provide a solution to the heat equation but also demonstrate the interplay between thermal and structural analysis in engineering applications.

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
    ### Beyond Fill Karel
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
