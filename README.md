Surrogate-Accelerated Multi-Objective Optimization for Energy Scenario Analysis
A Python framework for large-scale energy performance optimization under climate scenario uncertainty, combining high-fidelity surrogate modelling with evolutionary multi-objective search across high-dimensional parameter spaces.
Overview
This framework addresses a core computational bottleneck in scenario-based energy analysis: physics-based simulation models are too expensive to evaluate at the population scales required for robust Pareto-front exploration. The solution implemented here replaces direct simulation calls with a Bayesian-optimized CatBoost surrogate model, enabling efficient sampling across high-dimensional design and policy spaces under both historical and future climate forcing.
The optimization targets three coupled performance objectives — energy demand intensity, thermal discomfort risk, and operational carbon emissions — and resolves trade-offs between them using NSGA-II evolutionary search. Results are analyzed under two climate scenarios derived from regional climate projections, demonstrating non-linear performance divergence across scenario space under changing forcing conditions.
This methodology is domain-agnostic: the surrogate-optimization pipeline is structurally applicable to any setting where expensive simulation models constrain scenario ensemble size — including power system models, integrated assessment models, and industrial process optimization.
Methods
Surrogate modelling: CatBoost gradient boosting with Bayesian hyperparameter optimization (Optuna). Model selection benchmarked against Random Forest, XGBoost, and neural baselines. Evaluated on RMSE, R², and out-of-sample generalization across scenario conditions.
Interpretability: SHAP-based global sensitivity analysis to identify which input parameters drive performance divergence between climate scenarios — analogous to variance-based sensitivity analysis in uncertainty quantification.
Optimization: NSGA-II multi-objective evolutionary algorithm for Pareto-front resolution across three objectives simultaneously. Non-dominated solution sets analyzed via parallel coordinates and density distributions.
Climate scenario integration: Baseline and mid-future climate forcing derived from regional climate projections. Scenario-specific boundary conditions propagated through the surrogate to quantify performance uncertainty under non-stationary climate conditions.
Repository Structure
surrogate-accelerated-multiobjective-optimization/
├── data/
│   ├── raw/
│   ├── processed/
├── src/
│   ├── surrogate/
│   ├── optimization/
│   └── analysis/
├── notebooks/
├── results/
│   ├── plots/
│   └── metrics/
├── requirements.txt
└── README.md
Requirements
pip install -r requirements.txt
Core dependencies: pandas, numpy, scikit-learn, catboost, optuna, pymoo, shap, matplotlib
Usage
python# Train surrogate model
python src/surrogate/train.py --scenario baseline --config configs/default.yaml

# Run multi-objective optimization
python src/optimization/nsga2_run.py --surrogate models/catboost_baseline.pkl
Key Results
Surrogate model achieves R² > 0.97 across all objectives with RMSE well within acceptable bounds for optimization use. NSGA-II identifies non-dominated solution sets demonstrating significant trade-offs between energy demand reduction and thermal resilience under future climate forcing. Climate scenario comparison reveals non-linear performance divergence that coarse statistical approaches fail to capture.
