---
title: 'Investigation of Optical Efficiency of the Concentrated Solar Power System Located on the Inclined Hillside Areas'

# Authors
# If you created a profile for a user (e.g. the default `admin` user), write the username (folder name) here
# and it will be replaced with their full name and linked to their profile.
authors:
  - Anwoy Talukder Ranjak
  - admin
  - A. K. M. Ashikuzzaman
  - Tahmidul Haque Ruvo

# Author notes (optional)
author_notes:
  - 'Equal contribution'
  - 'Equal contribution'

date: '2024'
doi: 'https://dx.doi.org/10.2139/ssrn.4862794'

# Schedule page publish date (NOT publication's date).
publishDate: '2024'

# Publication type.
# Accepts a single type but formatted as a YAML list (for Hugo requirements).
# Enter a publication type from the CSL standard.
publication_types: ['Conference']

# Publication name and optional abbreviated publication name.
publication: SSRN 14th International Conference on Mechanical Engineering (ICME 2023)
publication_short: SSRN

abstract: Renewable energy in the industrial sector is a key step in achieving low-carbon production systems. Concentrated Solar Power (CSP) technologies can be used to generate electricity by converting sunlight energy to power a turbine. Solar Power Tower (SPT) has become more developed and well-liked in recent years on a commercial scale, despite the fact that parabolic trough is still the most well-known and widely used CSP technology. In this study, the inclined barren surfaces of hillside areas are taken as solar fields which are named as Hillside Concentrated Solar Powerplant (HCSP) system. For this, three different barren hilly areas located at United States have been selected where the solar irradiation is moderately higher. A simple inclined plane V-shape layout with 5100 heliostats is simulated for optical efficiency in each of the locations for four days of a year and three times of a day. These simulation results show that the inclined rectangular array type layout provides greater optical efficiency at any of the three locations investigated than the optical efficiencies of the traditional horizontal plane functional layouts.

# Summary. An optional shortened abstract.
summary: The study finds that an inclined V-shape heliostat layout in hillside CSP systems yields higher optical efficiency than traditional layouts across various U.S. locations.

tags:
  - CSP
  - Solar Energy
  - Renewable Energy

# Display this page in the Featured widget?
featured: true

# Custom links (uncomment lines below)
# links:
# - name: Custom Link
#   url: http://example.org

url_pdf: ''
#url_code: 'https://github.com/HugoBlox/hugo-blox-builder'
#url_dataset: 'https://github.com/HugoBlox/hugo-blox-builder'
#url_poster: ''
#url_project: ''
#url_slides: ''
#url_source: 'https://github.com/HugoBlox/hugo-blox-builder'
#url_video: 'https://youtube.com'

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
image:
  caption: 'Image credit: [**Unsplash**](https://unsplash.com/photos/pLCdAaMFLTE)'
  focal_point: ''
  preview_only: false

# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `internal-project` references `content/project/internal-project/index.md`.
#   Otherwise, set `projects: []`.
projects:
  - example

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
slides: csp
---

{{% callout note %}}  
Click the **Cite** button above to easily import this publication's metadata into your reference manager.  
{{% /callout %}}

{{% callout note %}}  
Click the **Slides** button to view the presentation, formatted with Markdown.  
{{% /callout %}}

# Investigation of Optical Efficiency of the Hillside Concentrated Solar Power System

This document presents the simulation and analysis of a **Hillside Concentrated Solar Power (HCSP)** system, utilizing a **V-shape heliostat layout** for improved optical efficiency.

---

## Mathematical Model

The **solar flux** intensity, which is a key factor in evaluating the performance of heliostat fields, is modeled using the **Hermite analytical method**. The formula for solar flux at any given point is:

\[
F(x, y) = \frac{1}{2 \alpha_x \alpha_y} \exp\left( -\frac{1}{2} \left( \frac{x}{\alpha_x} \right)^2 - \frac{1}{2} \left( \frac{y}{\alpha_y} \right)^2 \right) \sum_{i=0}^{\infty} \sum_{j=0}^{\infty} A_{ij} H_i\left( \frac{x}{\alpha_x} \right) H_j\left( \frac{y}{\alpha_y} \right)
\]

Where:
- \( \alpha_x, \alpha_y \) are the standard deviations of the flux distribution.
- \( H_i, H_j \) are Hermite polynomials.
- \( A_{ij} \) are the coefficients for the flux intensity.

---

## Code Implementation

To calculate the solar flux, we use the following Python code:

```python
import numpy as np
import math

# Function to calculate solar flux
def solar_flux(x, y, alpha_x, alpha_y, A_ij):
    flux = (1 / (2 * alpha_x * alpha_y)) * np.exp(-0.5 * (x / alpha_x) ** 2 - 0.5 * (y / alpha_y) ** 2)
    hermite_sum = 0
    for i in range(len(A_ij)):
        hermite_sum += A_ij[i] * math.hermite(i, x / alpha_x) * math.hermite(i, y / alpha_y)
    return flux * hermite_sum

# Sample values
alpha_x = 0.5  # Standard deviation in x direction
alpha_y = 0.5  # Standard deviation in y direction
x = np.linspace(-5, 5, 100)  # x values
y = np.linspace(-5, 5, 100)  # y values
A_ij = np.random.rand(10)  # Example random values for A_ij coefficients

# Calculate solar flux for given values
flux_values = np.array([[solar_flux(xi, yi, alpha_x, alpha_y, A_ij) for xi in x] for yi in y])

# Display results (You could use Matplotlib to plot if needed)
print(flux_values)

