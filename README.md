# ST2195-MCMC-Random-Walk-Metropolis
Implementation and evaluation of the Random Walk Metropolis (MCMC) algorithm, including convergence diagnostics using the R̂ statistic, implemented in Python and R.

# Markov Chain Monte Carlo: Random Walk Metropolis (ST2195 – Part 1)

This project implements and evaluates the Random Walk Metropolis (RWM) algorithm, a Markov Chain Monte Carlo (MCMC) method used to simulate samples from a target probability distribution. The analysis focuses on convergence behavior, Monte Carlo estimation, and diagnostic evaluation.

## Objectives
The project addresses two key tasks:
1. Implement the Random Walk Metropolis algorithm to sample from a target distribution and evaluate the quality of the simulated samples.
2. Assess convergence using multiple chains and the R̂ (R-hat) convergence diagnostic across different proposal variances.

## Target Distribution
The target probability density function is:

\[
f(x) = \frac{1}{2} \exp(-|x|)
\]

This distribution is symmetric, centered at zero, and has known theoretical mean and variance, allowing direct comparison with Monte Carlo estimates.

## Methodology
### Random Walk Metropolis Algorithm
- Initialized a Markov chain with a chosen starting value
- Generated proposals from a Normal distribution centered at the current state
- Applied the Metropolis acceptance rule using log-probabilities to ensure numerical stability
- Collected simulated samples after iteration

### Monte Carlo Estimation
- Estimated the sample mean and standard deviation from simulated draws
- Compared Monte Carlo estimates against theoretical values
- Visualized results using histograms and kernel density estimates overlaid with the true density

### Convergence Diagnostics
- Ran multiple independent chains with different initial values
- Computed within-chain and between-chain variances
- Calculated the R̂ statistic to evaluate convergence
- Analyzed the impact of proposal standard deviation on convergence behavior

## Key Findings
- The Random Walk Metropolis algorithm successfully reproduces the target distribution when parameters are well chosen.
- Monte Carlo estimates of the mean and standard deviation closely match theoretical values with sufficient iterations.
- Very small proposal variances lead to poor chain mixing and high R̂ values.
- Increasing the proposal variance improves exploration and convergence, reducing R̂ toward 1.

## Tools 
- **Python:** numpy, matplotlib
- **R:** base R, ggplot2
- **Methods:** MCMC, Monte Carlo estimation, convergence diagnostics


