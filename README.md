# Numerical Methods for Solving ODEs

This repository contains Python implementations and experiments for solving ordinary differential equations (ODEs) using different numerical methods. The primary goal is to explore and compare the accuracy and efficiency of classical and modern approaches.

---

## Table of Contents

- [Introduction](#introduction)  
- [Methods Implemented](#methods-implemented)  
- [Experiment and Results](#experiment-and-results)  
- [Usage](#usage)  
- [Dependencies](#dependencies)  
- [Conclusion](#conclusion)  

---

## Introduction

Solving ODEs numerically is a fundamental task in scientific computing. This repository demonstrates three common approaches to solving a simple first-order linear ODE:

\[
\frac{dy}{dx} = -2y, \quad y(0) = 1
\]

The exact solution is:

\[
y(x) = e^{-2x}
\]

We analyze the accuracy and performance of each method.

---

## Methods Implemented

1. **Euler Method**  
   - Simple fixed-step method  
   - Easy to implement but less accurate; errors accumulate quickly  

2. **Runge-Kutta 4th Order (RK4)**  
   - Fixed-step, higher-order method  
   - Highly accurate even with moderate step sizes  

3. **SciPy `solve_ivp`**  
   - Adaptive step solver using advanced algorithms (e.g., Dormand-Prince)  
   - Automatically balances accuracy and computational efficiency  

---

## Experiment and Results

We compare the numerical solutions against the exact solution and evaluate the maximum absolute error.

| Method        | Maximum Error           | Observation                               |
|---------------|-----------------------|-------------------------------------------|
| Euler         | ≈ 0.04                | Error accumulates; noticeable deviation   |
| RK4           | ≈ 5.8 × 10⁻⁶         | Almost identical to exact solution       |
| SciPy `solve_ivp` | ≈ 0.00041          | Adaptive step solver balances accuracy & efficiency |

**Observations:**
- Euler's error grows steadily with step number.  
- RK4 remains extremely accurate even with the same step size.  
- SciPy's adaptive solver adjusts step size automatically, keeping errors low while saving computation.

---

## Usage

Clone the repository:

```bash
git clone https://github.com/yourusername/numerical-ode.git
cd numerical-ode
