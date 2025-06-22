# Optimization Algorithm Experiments (Summer 2025)

This repository contains the implementation and analysis of optimization algorithms applied to convex and variational inequality (VI) problems. The experiments compare classical and advanced methods such as Gradient Descent (GD), Stochastic Gradient Descent (SGD), Stochastic Variance Reduced Gradient (SVRG), and the adaptive GRAAL (aGRAAL) method.

---

## 📁 Project Structure

- `notebooks/`: Jupyter notebooks for each experiment
- `reports/`: Final PDF reports summarizing results
- `figs/`: Figures and plots from experiments
- `data/`: Datasets used in experiments
- `beyond_golden_ratio/`: Included reference code for VI algorithms from the BGR paper

---

## Experiments

### 1. SVRG vs SGD on Convex Problems
- **Problems:** L2-regularized least squares and logistic regression
- **Methods:** GD, SGD (with decaying steps), SVRG (with fixed step)
- **Metrics:** Loss curves, convergence speed, and gradient variance

### 2. SVRG on Synthetic Small Dataset
- **Data:** 100×100 synthetic logistic regression
- **Focus:** SVRG variance reduction vs. SGD instability
- **Insight:** SVRG offers smoother and more stable convergence

### 3. VI Solver Visualization
- **Methods:** OGDA, GRAAL (ϕ = 2), GRAAL (ϕ = φ)
- **Problem:** Bilinear saddle-point problem (Polar Game)
- **Visualization:** Julia streamplots using CairoMakie
- **Result:** GRAAL (ϕ = φ) converges as predicted in theory

### 4. aGRAAL Implementation & Reproduction
- **Goal:** Reproduce Figures 2–6 from BGR paper
- **Tools:** Custom Julia implementation with adaptive step size
- **Examples:** Polar Game, Forsaken example
- **Result:** Shows sensitivity to ϕ and validates convergence behavior

---

## Requirements

To run the Python notebooks:

```bash
pip install numpy pandas matplotlib scikit-learn jupyter altair
