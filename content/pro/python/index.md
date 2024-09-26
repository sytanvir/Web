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

## Pendulum-Projectile Simulation on Solar Planets
- **Description:** A sophisticated simulation that combines the dynamics of pendulum motion with projectile motion in a solar system context.
- **Course:** Stanford University CS106A (2023)
- **Technologies Used:** Python 3, Pygame
- **Key Features:**
  - Realistic simulation of pendulum and projectile dynamics.
  - Visualization of gravitational interactions with different planetary bodies.
- **Visuals:**
  ![Pendulum-Projectile Simulation](pendulum_projectile_simulation.png)
- **Project Repository:** [View Project](https://github.com/sytanvir/Pendulum-Projectile-Simulation-on-Solar-Planets.git)

## Finite Difference Method (FDM) for Heat Transfer
- **Project Repository:** [View Project](https://github.com/sytanvir/FDM-Heat-Transfer.git)
- **Description:** A sophisticated implementation of the Finite Difference Method (FDM) that numerically solves heat transfer problems by approximating differential equations with difference equations.
- **Course:** Academic Project
- **Technologies Used:** Python 3, NumPy, Matplotlib
- **Key Features:**
  - Accurate simulation of heat distribution over time in solid materials.
  - Flexibility to analyze both cylindrical and spherical coordinate systems.
- **Visuals:**
  ![FDM Heat Transfer Simulation](fdm_heat_transfer_simulation.png)

### Heat Equation

The one-dimensional heat equation is:

{{< math >}}
$$
\frac{\partial u}{\partial t} = \alpha \frac{\partial^2 u}{\partial x^2}
$$
{{< /math >}}

Where:
- \( u \): temperature
- \( \alpha \): thermal diffusivity

### Discretization Using FDM

The equation can be discretized as:

{{< math >}}
$$
\frac{u_i^{n+1} - u_i^n}{\Delta t} = \alpha \frac{u_{i+1}^n - 2u_i^n + u_{i-1}^n}{\Delta x^2}
$$
{{< /math >}}

Rearranged to:

{{< math >}}
$$
u_i^{n+1} = u_i^n + \frac{\alpha \Delta t}{\Delta x^2} (u_{i+1}^n - 2u_i^n + u_{i-1}^n)
$$
{{< /math >}}

### Simplified Algorithm

1. **Initialization:** Define thermal properties \( h_a, T_a, k, g \).
2. **User Input:** Gather inputs like \( h_a, T_a, k, g, L, n \).
3. **Discretization:** 
   {{< math >}} 
   $$ h = \frac{L}{n}, \quad s = -\frac{g \cdot h^2}{4k} \text{ (cylindrical)}, \quad s = -\frac{g \cdot h^2}{6k} \text{ (spherical)} $$ 
   {{< /math >}}
4. **Matrix Setup:** Construct \( \text{matA} \) with boundary conditions.
5. **Matrix Construction:** Append internal node coefficients \( a, b, c \) to \( \text{matA} \).
6. **Constant Vector:** Create \( \text{matB} \) with boundary values.
7. **Matrix Calculations:** Solve using:
   {{< math >}}
   $$ u = \text{inmatA} \cdot \text{matB} $$
   {{< /math >}}
8. **Visualization:** Plot temperature distribution.
9. **Execution:** Run the algorithm.

## Karel Robot (7 Mini Projects)
- **Project Repository:** [View Projects](your_project_link_here)
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
## Baby Snake
- **Project Repository:** [View Project](your_project_link_here)
- **Description:** A collection of engaging mini-games developed using Python, showcasing programming logic and design principles.
- **Course:** Stanford University CS106A (2023)
- **Technologies Used:** Python 3, Pygame
- **Key Features:**
  - Includes various game genres: puzzles, arcade, and strategy.
  - Focus on user experience and gameplay mechanics.
- **Visuals:**
  ![Baby Snake](graph.jpg)

