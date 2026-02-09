# Bayesian Analysis of Air Pollution Effects on Mortality in Milan

A comprehensive Bayesian statistical analysis examining the short-term effects of air pollution on mortality in Milan, Italy.

## Project Overview

This project uses Bayesian hierarchical models to investigate the relationship between air pollution (PM10) and daily mortality rates in Milan, while accounting for confounding factors such as temperature, seasonality, and day-of-week effects.

## Repository Structure

```
├── short_term_effects_of_air_pollution_on_mortality_in_milan_analysis.Rmd    # Part 1: Exploratory Data Analysis
├── short_term_effects_of_air_pollution_on_mortality_in_milan_analysis.html # Part 1: Exploratory Data Analysis
├── short_term_effects_of_air_pollution_on_mortality_in_milan_models.Rmd # Part 2: Bayesian Model Development
├── short_term_effects_of_air_pollution_on_mortality_in_milan_models.html # Part 2: Bayesian Model Development
├── mil.txt # dataset
└── README.md
```

## Analysis Components

### Part 1: Exploratory Data Analysis
- Data loading and preprocessing
- Temporal patterns in mortality data
- Air pollution trends (PM10)
- Temperature effects
- Seasonal and weekly patterns
- Correlation analysis

### Part 2: Bayesian Model Development

The analysis progressively builds and compares multiple Bayesian models:

1. **Model 0: Baseline (Poisson)**
   - Basic model with temporal trends
   - Day of week effects
   - Seasonal patterns using splines

2. **Model 0-NB: Baseline (Negative Binomial)**
   - Addresses overdispersion in count data
   - More flexible variance structure

3. **Model Temperature**
   - Incorporates temperature effects
   - Non-linear temperature relationships
   - Lag effects

4. **Model Pollution (Linear)**
   - Adds PM10 pollution effects
   - Linear relationship with mortality

5. **Full Model**
   - Combines all predictors
   - Interaction effects
   - Complete hierarchical structure

## Key Features

- **Bayesian Framework**: Uses Stan/brms for full Bayesian inference
- **Hierarchical Modeling**: Accounts for temporal dependencies
- **Posterior Predictive Checks**: Validates model assumptions
- **Model Comparison**: Uses LOO-CV and WAIC for model selection
- **Effect Estimation**: Quantifies pollution impact on mortality
- **Uncertainty Quantification**: Full posterior distributions for all parameters

## Statistical Methods

- Generalized Linear Models (GLM)
- Negative Binomial regression for overdispersed count data
- Spline smoothing for temporal trends
- Distributed lag models for lagged effects
- Bayesian model averaging and selection

## Dependencies

### R Packages
```r
- brms          # Bayesian regression models
- ggplot2       # Visualization
- dplyr         # Data manipulation
- tidyr         # Data tidying
- bayesplot     # Posterior visualization
- loo           # Model comparison
- splines       # Temporal smoothing
```

## Results & Findings

The analysis quantifies:
- The magnitude of pollution effects on mortality
- Temperature-mortality relationships
- Seasonal patterns in mortality risk
- Day-of-week variations
- Lag structures for environmental exposures

Model comparison reveals the relative importance of different predictors and identifies the best-fitting model for the data.

## Data

The analysis uses daily time series data from Milan including:
- Daily mortality counts
- PM10 pollution measurements
- Temperature data
- Calendar variables (day of week, month, year)


## Usage

1. Open the HTML files in a web browser to view the complete analysis
2. The reports are self-contained with all code, results, and visualizations
3. Part 1 provides context and exploratory analysis
4. Part 2 contains the core Bayesian modeling and inference

## Model Diagnostics

All models include:
- Trace plots for MCMC convergence
- R-hat statistics
- Effective sample size (ESS)
- Posterior predictive checks
- Residual diagnostics

## Reproducibility

The analysis is fully reproducible. Each HTML report contains:
- Complete R code
- Model specifications
- Random seeds for MCMC sampling
- Package versions

## Future Directions

Potential extensions include:
- Additional pollutants (NO2, O3, PM2.5)
- Age-stratified analyses
- Cause-specific mortality
- Spatial components
- Multi-city comparisons

---

**Note**: This analysis is for research and educational purposes. Results should be interpreted in context with domain expertise in environmental epidemiology.
