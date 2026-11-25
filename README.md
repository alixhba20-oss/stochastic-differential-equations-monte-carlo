# Stochastic Differential Equations (SDEs) & Monte Carlo Risk Modeling

Numerical analysis, maximum likelihood estimation (MLE), and Monte Carlo simulation for **Geometric Brownian Motion (GBM)** in Python.

## Mathematical Formulation
We study the stochastic differential equation:
$$dS_t = \mu S_t \, dt + \sigma S_t \, dW_t$$
with exact analytical solution:
$$S_t = S_0 \exp\left(\left(\mu - \frac{1}{2}\sigma^2\right)t + \sigma W_t\right)$$

## Key Components (`01_SDE_Simulation_and_Convergence.ipynb`)
1. **Path Simulation:** Compares exact analytical trajectories against the Euler–Maruyama discretization scheme.
2. **Strong Convergence Analysis:** Evaluates mean absolute terminal error $\mathbb{E}[|S_T - \hat{S}_T|]$ across step sizes $\Delta t$ on a log-log scale, contrasting Euler–Maruyama ($O(\Delta t^{0.5})$) with the Itô-corrected Milstein scheme ($O(\Delta t^{1.0})$).
3. **MLE Calibration & Monte Carlo Risk:** Estimates drift ($\hat{\mu}$) and volatility ($\hat{\sigma}$) from log-returns via Maximum Likelihood Estimation, simulates 10,000 trajectories, and computes the terminal confidence interval and 95% Value-at-Risk (VaR).

## Tools
Python, NumPy, Matplotlib, Google Colab
