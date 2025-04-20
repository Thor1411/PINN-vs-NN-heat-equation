# PINN-vs-NN-heat-equation 🔥🧠

This project demonstrates how to solve the **1D Heat Equation** using:
- A standard **Feedforward Neural Network (FNN)**, and
- A **Physics-Informed Neural Network (PINN)** that incorporates boundary and initial conditions directly into its loss function.

## 📖 Equation Overview

The heat equation is:
![Heat Equation](https://latex.codecogs.com/png.latex?%5Ccolor%7Bwhite%7D%5Cfrac%7B%5Cpartial%20u%7D%7B%5Cpartial%20t%7D%20%3D%20%5Calpha%20%5Cfrac%7B%5Cpartial%5E2%20u%7D%7B%5Cpartial%20x%5E2%7D)

where `u(x, t)` is the temperature at position `x` and time `t`, and `α` is the thermal diffusivity constant.

## 🧪 Approach

### Method 1: Standard Neural Network
- Samples random `(x, t)` points.
- Minimizes residual loss from the heat PDE.

### Method 2: Physics-Informed Neural Network (PINN)
- Also includes losses from:
  - Boundary condition: `u(0,t) = u(1,t) = 0`
  - Initial condition: `u(x,0) = sin(πx)`

## 🛠️ Dependencies
- Python 3.x
- PyTorch
- NumPy
- Matplotlib

Install them using:
```bash
pip install torch numpy matplotlib
```
