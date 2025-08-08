# 🔥 Advanced Physics-Informed Neural Network (PINN) for 2D Heat Equation

This repository contains a **research-grade implementation** of a Physics-Informed Neural Network (PINN) that solves the **2D transient heat equation** with physical priors, advanced optimizer strategies, and extensive visualizations.

---

## 📐 Problem Definition

We solve the PDE:

\[
\frac{\partial u}{\partial t} = \alpha \left( \frac{\partial^2 u}{\partial x^2} + \frac{\partial^2 u}{\partial y^2} \right)
\]
with:
- **Domain:** \( x, y \in [0,1], t \in [0,1] \)
- **Initial Condition:** \( u(x,y,0) = \sin(\pi x) \sin(\pi y) \)
- **Boundary Condition:** \( u = 0 \) on all edges
- **Analytic Solution:** \( u(x,y,t) = e^{-2\pi^2\alpha t} \sin(\pi x) \sin(\pi y) \)

---

## 🧠 Key Features

- **Fourier Feature Encoding** to mitigate spectral bias  
- **Hybrid Optimization**: Adam → L-BFGS (Wolfe line search)  
- **Adaptive Loss Reweighting** for balanced PDE/IC/BC/energy terms  
- **Energy-Decay Penalty** to enforce physical constraints  
- **Curriculum Sampling** focusing on challenging regimes early  
- **Extensive Visualization**:
  - Training loss curves
  - PDE residual maps & histograms
  - 3D surface plots
  - Profiles vs analytic solution
  - Error vs time curves
  - Animated time evolution (GIF)

---

## 📊 Results Overview

### Predicted vs Analytic Solution at \( t = 0.5 \)
| PINN (Fourier) | Analytic Solution | Baseline PINN |
|---|---|---|
| ![PINN](<img width="403" height="289" alt="image" src="https://github.com/user-attachments/assets/309094aa-4ea0-430e-b229-998667c3b568" />) | ![Analytic](<img width="378" height="293" alt="image" src="https://github.com/user-attachments/assets/7e95a8f3-6ee9-40d9-932f-fce4a4070104" />) | ![Baseline](<img width="424" height="295" alt="image" src="https://github.com/user-attachments/assets/4332bed9-604a-45e5-b6ca-e1c31e63f39b" />) |

### PDE Residual Map
![Residual Map](assets/residual.png)

---

## 📖 Research Impact

This project showcases how **domain-specific physics can be integrated directly into neural network training** for robust, interpretable, and data-efficient solutions to PDEs.  
Potential extensions include:
- Inverse problem solving (parameter estimation from sparse observations)  
- Multi-physics PINNs for coupled systems  
- Using PINNs to accelerate traditional finite-element or finite-difference solvers  
- Applying advanced sampling strategies to improve generalization in PDE learning  

By combining **spectral bias mitigation, curriculum learning, hybrid optimization, and physical priors**, this implementation bridges the gap between theoretical PINN research and real-world scientific computing.

---

## 🛠 Tech Stack
- `PyTorch`
- `NumPy`
- `Matplotlib`
- `ImageIO`
- `TQDM`

---

## 📌 Applications
- Scientific machine learning
- Computational fluid dynamics
- Thermal simulations
- Materials science
- PDE-constrained optimization
- Inverse problem solving

---

## 📬 Author
**Abhishek Yadav**  
Passionate about AI for physics, scientific ML, and PDE-constrained deep learning.  
Let’s connect on [LinkedIn](https://www.linkedin.com/).

---
