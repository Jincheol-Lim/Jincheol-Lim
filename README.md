## Simulation Study: Missing Data Handling in SEM Trees

This repository contains R code for a Monte Carlo simulation study evaluating the performance of various missing data handling methods in Structural Equation Modeling Trees (SEM Trees). The simulation compares subgroup recovery under different samplesize, cut point location, missingness mechanisms and proportion, using either continuous or dichotomous covariates.

Included R Scripts
1. simulation_continuous.R

Purpose:
Conducts a Monte Carlo simulation using a continuous covariate to partition SEM trees.

Details:
Simulates longitudinal data based on a Latent Growth Curve Model (LGCM), imposes missing data under MCAR and MAR mechanisms, applies five imputation methods (Ignore, missForest, kNN, FAMD, and CART), and evaluates subgroup recovery using Adjusted Rand Index (ARI).

Output:
Saves the full simulation results as simulation_ARI_continuous.xlsx.

2. simulation_dichotomous.R

Purpose:
Same as above, but uses a dichotomous (binary) covariate to partition the SEM trees.

Details:
Group labels are assigned based on a binary splitting covariate. The simulation procedure and evaluation steps are otherwise identical to the continuous version.

Output:
Saves the full simulation results as simulation_ARI_dichotomous.xlsx.

3. plot_simulation_results.R

Purpose:
Generates summary plots of the simulation results for comparison across missing data handling methods.

Details:
Reads the .xlsx result files, computes average ARI by condition (sample size, missing rate, mechanism, etc.), and creates faceted line plots using ggplot2 to visually compare performance.

Output:
Displays and optionally exports the final plot (e.g., simulation_plot.png).
