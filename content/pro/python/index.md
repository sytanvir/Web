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

## Finite Difference Method (FDM)

The Finite Difference Method (FDM) is a numerical technique used to solve differential equations by approximating them with difference equations. It is particularly useful in heat transfer analysis, where the heat equation governs the temperature distribution over time and space.

### Heat Equation

The one-dimensional heat equation is given by:

{{< math >}}
$$
\frac{\partial u}{\partial t} = \alpha \frac{\partial^2 u}{\partial x^2}
$$
{{< /math >}}

Where:
- \( u \) is the temperature at a given point in space and time.
- \( \alpha \) is the thermal diffusivity of the material.
- \( \frac{\partial u}{\partial t} \) is the rate of change of temperature over time.
- \( \frac{\partial^2 u}{\partial x^2} \) is the second spatial derivative of temperature.

### Discretization Using FDM

To solve this equation numerically, we discretize the domain into a grid of points. The time derivative can be approximated using a forward difference, and the spatial derivative using a central difference:

{{< math >}}
$$
\frac{u_i^{n+1} - u_i^n}{\Delta t} = \alpha \frac{u_{i+1}^n - 2u_i^n + u_{i-1}^n}{\Delta x^2}
$$
{{< /math >}}

Rearranging gives us the iterative update formula:

{{< math >}}
$$
u_i^{n+1} = u_i^n + \frac{\alpha \Delta t}{\Delta x^2} (u_{i+1}^n - 2u_i^n + u_{i-1}^n)
$$
{{< /math >}}

### Algorithm for Heat Transfer Analysis

1. **Initialization:** 
   - Print a welcome message and define thermal properties: \( h_a \), \( T_a \), \( k \), \( g \).

2. **User Input:** 
   - Prompt the user for:
     - Convective Heat Transfer Coefficient \((h_a)\)
     - Ambient Temperature \((T_a)\)
     - Thermal Conductivity \((k)\)
     - Heat Generation \((g)\)
     - Domain type (cylindrical/spherical)
     - Domain length \((L)\)
     - Number of divisions \((n)\)

3. **Discretization:** 
   - Calculate step size: 
   {{< math >}}
   $$
   h = \frac{L}{n}
   $$
   {{< /math >}}
   - Set \( s \) based on domain type:
     - **Cylindrical:** 
     {{< math >}}
     $$
     s = -\frac{g \cdot h^2}{4k}
     $$
     {{< /math >}}
     - **Spherical:** 
     {{< math >}}
     $$
     s = -\frac{g \cdot h^2}{6k}
     $$
     {{< /math >}}

4. **Matrix Setup:** 
   - Construct a length vector from \( 0 \) to \( L \).
   - Initialize coefficient matrix \(\text{matA}\) and append boundary conditions.

5. **Coefficient Matrix Construction:** 
   - Iterate through internal nodes to calculate and append coefficients \( a, b, c \) to \(\text{matA}\).
   - Append boundary condition for \( r = L \).

6. **Constant Vector Construction:** 
   - Create constant vector \(\text{matB}\) with initial value \( s \) and append values for internal nodes and boundary conditions.

7. **Matrix Calculations:** 
   - Compute the inverse of \(\text{matA}\) and solve for \( u \) using:
   {{< math >}}
   $$
   u = \text{inmatA} \cdot \text{matB}
   $$
   {{< /math >}}

8. **Visualization:** 
   - Convert solution \( u \) to a NumPy array and plot the temperature distribution using Matplotlib.

9. **Execution:** 
   - Run the main function to execute the algorithm.

---

### Conclusion

Through this project, I successfully implemented the FDM to simulate heat transfer in solid bars while considering structural deflections. The mathematical framework and algorithmic approach not only provide a solution to the heat equation but also demonstrate the interplay between thermal and structural analysis in engineering applications.

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
