# Multi-Objective Optimization of Building Energy Performance & Indoor Comfort

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![License](https://img.shields.io/badge/License-MIT-green.svg)
![Contributions](https://img.shields.io/badge/Contributions-Welcome-brightgreen.svg)

## 📌 Project Overview
This repository provides a data-driven optimization framework designed to mitigate the trade-offs between **Building Energy Consumption**, **Indoor Thermal Comfort**, and **CO2 Emissions**. By leveraging machine learning models and the **NSGA-II** (Non-dominated Sorting Genetic Algorithm II), this tool explores optimal building configurations under both historical and future climate scenarios.

## 🛠 Methodology
The workflow integrates predictive modeling with evolutionary optimization:
1. **Surrogate Modeling:** Training regression models to predict energy and comfort metrics.
2. **Optimization:** Implementing NSGA-II to find the Pareto-optimal front for:
    * **Objective 1:** Total Energy Demand (Heating/Cooling).
    * **Objective 2:** Indoor Discomfort (Predictive Mean Vote - PMV).
    * **Objective 3:** Environmental Impact (CO2 Footprint).

## 📊 Key Results
*(Tip: Place your output graph in a folder named 'results' and it will show up here)*
![Pareto Front](results/pareto_plot.png)

The optimization successfully identifies a set of solutions that balance occupant comfort with energy efficiency, providing a decision-support tool for sustainable building design.

## 📁 Repository Structure
* `notebooks/`: Contains the main Jupyter Notebook (`building_energy_optimization.ipynb`) with the full pipeline.
* `data/`: Cleaned historical and future climate datasets used for training and testing.
* `requirements.txt`: List of necessary Python libraries to reproduce the environment.

## 🚀 Getting Started

### Prerequisites
Ensure you have Python 3.8+ installed.

### Installation
1. Clone the repository:
   ```bash
   git clone [https://github.com/Alirezza18/multiobjective-building-energy.git](https://github.com/Alirezza18/multiobjective-building-energy.git)
