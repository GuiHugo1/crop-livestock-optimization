# Crop-Livestock Circular Optimization in Alberta

**MGSC 662 – Decision Analytics (Fall 2025)**
**Authors:** Hugo Guideau, Al Cheaito, Vasilis Christopoulos, Tirth Baldia, Rafael Daniel Chantres Garcia
**Instructor:** Prof. Javad Nasiry

---

## 📌 Overview
This project develops a mathematical optimization model to integrate crop rotations and livestock grazing in Alberta, Canada. The goal is to minimize synthetic fertilizer use by leveraging manure nutrients from cattle, while respecting agronomic constraints, field-size distributions, and regional crop demand.

**Key Findings:**
- **3% reduction** in synthetic fertilizer requirements at the provincial scale.
- **CAD 200M/year** in direct cost savings, plus environmental benefits.
- **Dynamic crop rotations** emerge when cattle integration is enabled, improving nutrient cycling.

---

## 📂 Repository Structure

| Folder/File          | Description                                                                 |
|----------------------|-----------------------------------------------------------------------------|
| `/code`              | Python implementation (Gurobi) of the integrated crop-livestock model.      |
| `/data`              | Input datasets: crop nutrient coefficients, field sizes, cattle numbers.   |
| `/results`   | Optimization visualization.         |
| `MGSC_662_Report.pdf`              | Full report (PDF), appendices, and supplementary materials.                 |
| `README.md`          | This file.                                                                  |

---

## 🔍 Problem Statement
Modern agriculture in Western Canada relies heavily on synthetic fertilizers, which are energy-intensive and contribute to greenhouse gas emissions. Alberta’s cattle population produces underutilized manure nutrients. This project optimizes **multi-year crop rotations** and **pasture allocation** to:
- Meet crop demand.
- Minimize synthetic fertilizer use.
- Capture nutrient circularity between crops and livestock.

**Models Developed:**
1. Base crop-rotation model (provincial level).
2. CCS-level model with fixed field identifiers.
3. **Final integrated model**: CCS-level, field-size distributions, grazing capacity, and manure nutrient recycling.

---

## 🛠️ Installation & Usage

### Requirements
- Python 3.8+
- Gurobi Optimizer (academic license available [here](https://www.gurobi.com/academia/academic-program-and-licenses/))
- Libraries: `pandas`, `numpy`, `matplotlib`, `networkx`

## Key Results

### Scenario Comparison
| Scenario          | Synthetic Nutrients (Mt) | Savings vs. Baseline |
|-------------------|-------------------------|----------------------|
| No Integration    | 6.55                    | —                    |
| With Integration  | 6.35                    | 3%                   |

---

## Visualizations
- **Rotation Networks**: Compare crop-only vs. integrated scenarios.
  ![Rotation Network Example](results/Network_Example.png)
- **Field-Size Dynamics**: Radar-style plot of crop transitions over 6 years.

**Insights:**
- Pasture → wheat/barley transitions dominate.
- Grass hay is not selected; all grass fields become pasture.
- Rotation diversity increases with cattle integration.

---

## Data Sources
| Data                  | Source                                                                 |
|-----------------------|------------------------------------------------------------------------|
| Crop areas & cattle   | [2021 Census of Agriculture](https://agriculture.canada.ca/atlas)       |
| Nutrient coefficients | [Government of Manitoba](https://www.gov.mb.ca/sd/eal/registries/5659steinbach/crop_nutrient_removal.pdf) |
| Field-size classes    | [Lesiv et al. (2018)](https://doi.org/10.1111/gcb.14492)                |

---

## Future Work
- Soil fertility decay and mandatory fallow periods.
- Economic optimization (crop prices, fertilizer costs).
- Stochastic yields and weather variability.
- Livestock feed interactions and infrastructure constraints.

---
## License
MIT License – see [LICENSE](LICENSE).
