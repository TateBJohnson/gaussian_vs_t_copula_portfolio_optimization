# Gaussian vs t-Copula: Portfolio Tail Risk Analysis

Fits Student-t marginals and compares Gaussian vs. t-copula dependence structures on a
four-asset equity portfolio subset from the VMLS dataset. Demonstrates the tail dependence
limitations of the Gaussian copula and shows why the t-copula better captures joint extreme
moves in financial returns.

## Structure

```
gaussian_vs_t_copula_portfolio_optimization/
├── copula_portfolio_analysis.ipynb   # main analysis notebook
├── data/
│   └── vmls_portfolio_returns.csv    # daily returns, 19 risky assets + risk-free
└── .gitignore
```

## What the Notebook Covers

- **Part (a)** - Fit Student-t marginals to all 19 assets, confirm fat tails (ν < 5)
- **Part (b)** - Apply PIT transforms, visualize empirical 4x4 scatter matrix
- **Part (c)** - Fit Gaussian copula on four-asset subset
- **Part (d)** - Fit t-copula via MLE, compare copula vs marginal degrees of freedom
- **Part (e)** - Simulate from both copulas, compare corner mass side by side

## Dependencies

```
numpy, pandas, scipy, matplotlib, seaborn
```

## Running

Open `copula_portfolio_analysis.ipynb` and run all cells top to bottom.
The data file is included in `data/`.
