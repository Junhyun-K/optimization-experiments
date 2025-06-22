# Optimization Algorithm Experiments (Summer 2025)

This repository contains implementation and analysis of optimization algorithms on convex and variational inequality problems. Experiments include comparisons of GD, SGD, SVRG, and aGRAAL.

## 📂 Project Structure

- `reports/`: Final PDF reports summarizing each experiment.
- `notebooks/`: Jupyter notebooks containing experiment code and analysis.
- `src/`: (Optional) Helper functions in Julia or Python.
- `figs/`: (Optional) Saved plots for reference.

## 📌 Experiments

### 1. SVRG vs SGD (Convex Problems)
- Problem: L2-regularized least squares & logistic regression
- Methods: GD, SGD with decaying steps, SVRG with fixed step size
- Evaluation: Convergence speed, variance reduction, loss residual

### 2. SVRG on Small Data
- Small 100×100 synthetic logistic regression problem
- Focus: SVRG smooth convergence vs. SGD instability

### 3. VI Solver Visualization
- Methods: OGDA, GRAAL (ϕ = 2, φ)
- Problem: Polar Game
- Tools: Julia + CairoMakie streamplots
- Result: Only GRAAL(ϕ = φ) converges as predicted

### 4. aGRAAL Implementation
- Full reproduction of BGR paper figures
- Custom Julia implementation of aGRAAL
- Adaptive step-size behavior across VI problems (Polar, Forsaken)

## 🛠 Requirements

```bash
pip install numpy matplotlib pandas scikit-learn jupyter altair
