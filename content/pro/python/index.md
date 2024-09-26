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

## Mathematical Background

The **Finite Difference Method (FDM)** is a numerical technique used to approximate solutions to partial differential equations (PDEs), such as the **heat equation**. The general form of the heat equation in one dimension is:

{{< math >}}
$$
\frac{\partial u}{\partial t} = \alpha \frac{\partial^2 u}{\partial x^2}
$$
{{< /math >}}

Where:
- \( u(x, t) \) represents the temperature at a given point \( x \) and time \( t \).
- \( \alpha \) is the thermal diffusivity of the material.

### Discretization Using FDM

To numerically solve the equation, we discretize both the time and space domains. Let the space domain be divided into \( n \) points, \( x_1, x_2, \ldots, x_n \), and the time domain into \( m \) steps, \( t_1, t_2, \ldots, t_m \).

Using the **forward difference** for the time derivative and the **central difference** for the second spatial derivative, the heat equation can be approximated as:

{{< math >}}
$$
\frac{u_i^{n+1} - u_i^n}{\Delta t} = \alpha \frac{u_{i+1}^n - 2u_i^n + u_{i-1}^n}{\Delta x^2}
$$
{{< /math >}}

Where:
- \( u_i^n \) is the temperature at position \( x_i \) and time \( t_n \).
- \( \Delta t \) is the time step.
- \( \Delta x \) is the space step.

### Rearranging for the Next Time Step

The above equation can be rearranged to compute the temperature at the next time step, \( u_i^{n+1} \):

{{< math >}}
$$
u_i^{n+1} = u_i^n + \alpha \frac{\Delta t}{\Delta x^2} \left( u_{i+1}^n - 2u_i^n + u_{i-1}^n \right)
$$
{{< /math >}}

This formula allows us to iteratively compute the temperature at each point for the next time step based on the current time step.

### Boundary and Initial Conditions

For the problem to be well-posed, we need boundary and initial conditions. For example:
- **Initial condition**: We assume the temperature distribution at \( t = 0 \) is known, such as \( u(x, 0) = f(x) \).
- **Boundary conditions**: These can be fixed (Dirichlet), like \( u(0, t) = u(L, t) = 0 \), or more complex types, depending on the problem setup.

### Stability Condition

To ensure numerical stability, the following condition must be met:

{{< math >}}
$$
\frac{\alpha \Delta t}{\Delta x^2} \leq \frac{1}{2}
$$
{{< /math >}}

If this condition is not satisfied, the solution may become unstable, leading to large errors or divergence.

### Algorithm Outline

1. Discretize the spatial domain into \( n \) points and the time domain into \( m \) steps.
2. Initialize the temperature distribution \( u(x, 0) \) according to the initial condition.
3. Apply boundary conditions at each time step.
4. Use the finite difference formula to compute the temperature at the next time step \( t_{n+1} \) based on the previous step \( t_n \).
5. Repeat until the desired final time \( T \) is reached.

### Summary

The **Finite Difference Method (FDM)** provides a simple yet powerful way to solve heat transfer problems by approximating derivatives using differences. While easy to implement, care must be taken with stability conditions and boundary values to ensure accurate results.


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
