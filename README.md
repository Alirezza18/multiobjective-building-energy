# Multi-Objective Optimization of Building Energy Performance & Indoor Comfort

## 📌 Project Overview

This repository provides a data-driven optimization framework designed to mitigate the trade-offs between **Building Energy Consumption**, **Indoor Thermal Comfort**, and **CO2 Emissions**. By leveraging machine learning models and the **NSGA-II (Non-dominated Sorting Genetic Algorithm II)**, this tool explores optimal building configurations under both historical and future climate scenarios.

## 🛠 Methodology

The workflow integrates predictive modeling with evolutionary optimization:

1. **Surrogate Modeling:** Training regression models to predict energy and comfort metrics.
2. **Optimization:** Implementing NSGA-II to find the Pareto-optimal front for:
* **Objective 1:** Total Energy Demand (Heating/Cooling).
* **Objective 2:** Indoor Discomfort (Predictive Mean Vote - PMV).
* **Objective 3:** Environmental Impact (CO_2 Footprint).

## 📂 Repository Structure

* `building_energy_optimization.ipynb`: The primary pipeline for data preprocessing, model training, and optimization.
* `extended_complete_Historical_5000_clean.csv`: Cleaned historical dataset for baseline modeling.
* `mid_future_with_preds_clean.csv`: Predictive dataset incorporating climate change projections.

## 🚀 Technical Requirements

To replicate this study, ensure the following Python libraries are installed:

```bash
pip install pandas numpy matplotlib seaborn pymoo scikit-learn

```

## 📊 Key Features

* **Climate Change Adaptation:** Evaluates building performance under future weather shifts.
* **Pareto Analysis:** Generates visualization of trade-offs between conflicting objectives.
* **Scalability:** The framework can be adapted to various building types and climatic zones.

## 📧 Contact

**Alireza** - [GitHub Profile](https://www.google.com/search?q=https://github.com/Alirezza18)
