# Optimization Algorithm Experiments (Summer 2025)

This repository contains the implementation and analysis of optimization algorithms applied to convex and variational inequality (VI) problems. The experiments focus on comparing classical and advanced methods such as Gradient Descent (GD), Stochastic Gradient Descent (SGD), Stochastic Variance Reduced Gradient (SVRG), Halpern iteration (including stochastic and inexact variants), and the adaptive GRAAL (aGRAAL) method.

---

## Project Structure

- `notebooks/`: Jupyter notebooks for each experiment
- `reports/`: Final PDF reports summarizing results
- `figs/`: Figures and plots from experiments
- `data/`: Datasets used in experiments
- `beyond_golden_ratio/`: Reference code for VI algorithms from the BGR paper (see Acknowledgements)

---

## Experiments

### 1. SVRG vs SGD on Convex Problems
- **Problems:** L2-regularized least squares and logistic regression  
- **Methods:** GD, SGD (with decaying steps), SVRG (with fixed step)  
- **Metrics:** Loss curves, convergence speed, and gradient variance  

### 2. SVRG on Synthetic Dataset
- **Data:** 100×100 synthetic logistic regression  
- **Focus:** Stability of SVRG compared to SGD instability  
- **Insight:** SVRG provides smoother and more stable convergence  

### 3. VI Solver Visualization
- **Methods:** Extragradient (EG), Halpern, OGDA, GRAAL (ϕ = 2, ϕ = φ)  
- **Problem:** Bilinear saddle-point problem (Polar Game)  
- **Visualization:** Julia streamplots using CairoMakie  
- **Result:** Demonstrates convergence and divergence regimes, verifying theoretical predictions  

### 4. aGRAAL Implementation & Reproduction
- **Goal:** Reproduce Figures 2–6 from BGR paper  
- **Tools:** Custom Julia implementation with adaptive step size  
- **Examples:** Polar Game, Forsaken benchmark  
- **Result:** Shows sensitivity to parameter ϕ and validates convergence behavior  

### 5. Halpern Iteration and Variants
- **Goal:** Implement deterministic, stochastic, and inexact Halpern methods  
- **Benchmarks:** Forsaken, Polar Game, and Lower Bound problems  
- **Result:** Verified divergence of EG (Theorem 4.3, Gorbunov et al. 2022) and compared Halpern’s improved performance  
- **Insight:** Highlighted parameter sensitivity, stability issues, and convergence differences  

---

## Recent Work (Fall 2025)

- **Inexact Halpern Experiments:** Extended analysis to Forsaken, Polar Game, and Lower Bound VI benchmarks with parameter tuning (ρ, η, c).  
- **Counterexample Verification:** Reproduced Theorem 4.3 (Gorbunov et al., 2022), demonstrating divergence of EG and contrasting with Halpern iteration.  
- **Research Integration:** Began preparing experimental framework for *inexact fixed-point iterations in min-max problems* (inspired by Alacaoglu et al., 2024–2025).  
- **Reports:** Drafted technical notes and LaTeX reports summarizing results for Directed Studies (MATH 448) under Prof. Ahmet Alacaoglu.  

---

## Acknowledgements

This repository incorporates reference code from [Axel Böhm’s **beyond_golden_ratio**](https://github.com/AxelBohm/beyond_golden_ratio),  
licensed under the MIT License © 2023 Axel Böhm.  

Related paper:  
Alacaoglu, Ahmet, Axel Böhm, and Yura Malitsky.  
*Beyond the Golden Ratio for Variational Inequality Algorithms.*  
arXiv preprint arXiv:2212.13955 (2022).
