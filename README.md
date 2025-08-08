# 🔥 Advanced Physics-Informed Neural Network (PINN) for 2D Heat Equation

This repository contains a **research-grade implementation** of a Physics-Informed Neural Network (PINN) that solves the **2D transient heat equation** with physical priors, advanced optimizer strategies, and extensive visualizations.

---

## 📊 Results Overview

### Model Comparisons at \( t = 0.5 \)

| Baseline PINN | Analytic Solution | PINN (Fourier Features) |
|---|---|---|
| ![Baseline](assets/baseline_pinn.png) | ![Analytic](assets/analytic.png) | ![Fourier](assets/fourier_pinn.png) |

The **Fourier-enhanced PINN** produces richer high-frequency representations, while the baseline suffers from spectral bias. The analytic solution serves as the ground truth for comparison.

---

### PDE Residual Analysis

| Residual Map \( r(x,y,t=0.5) \) | Residual Distribution |
|---|---|
| ![Residual Map](assets/residual_map.png) | ![Residual Histogram](assets/residual_hist.png) |

Residual visualization helps identify regions where the PDE constraint is harder to satisfy, guiding further refinement strategies.

---

## 📖 Research Impact

This project demonstrates a **bridge between theoretical PINN research and applied scientific computing**. By integrating:
- Fourier features for spectral bias reduction
- Adaptive loss reweighting
- Physical priors (energy decay)
- Advanced optimizers (Adam → L-BFGS)

…it provides a **robust and interpretable framework** for solving PDEs, easily extendable to:
- Inverse problems
- Multi-physics coupling
- Acceleration of traditional solvers
