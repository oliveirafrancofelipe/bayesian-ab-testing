# Bayesian A/B Testing

Two self-contained notebooks that treat A/B testing as a decision problem rather than a significance test. Each one starts from prior beliefs, updates them with the data, and turns the resulting posterior into a concrete business recommendation, with the analytic math and the computation cross-checked against each other.

## Notebooks

### 1. Bayesian A/B Testing as a Decision Problem
File: `bayesian_ab_exercise1.ipynb`

A new product experience tested against a control, worked end to end and in two independent ways:

- A logistic (GLM) parameterisation with Normal priors on the log-odds scale
- Bayes' theorem written out term by term, with the Binomial likelihood derived explicitly
- Two computational engines, deterministic grid integration and MCMC with PyMC, run side by side and checked for agreement
- Expected regret as the decision rule, with an honest discussion of where regret alone is not enough
- A posterior-predictive simulation of whether next week's revenue target is met

### 2. Bayesian Decision-Making for a Marketing Experiment
File: `bayesian_ab_exercise2.ipynb`

Two marketing strategies and a sharper question: commit now, or pay to run an experiment first?

- Beta priors over signup rates, updated in closed form through Beta-Binomial conjugacy
- Expected regret as the decision metric, and why it coincides here with the higher-mean rule
- The probability of committing to the wrong strategy without testing
- The dollar value of running the experiment, estimated by Monte-Carlo over the full process (value of information)

## Viewing the notebooks

Both render on GitHub, but they are figure-heavy, so nbviewer is the more reliable way to read them with all outputs:

- [Notebook 1 on nbviewer](https://nbviewer.org/github/oliveirafrancofelipe/bayesian-ab-exercises/blob/main/bayesian_ab_exercise1.ipynb)
- [Notebook 2 on nbviewer](https://nbviewer.org/github/oliveirafrancofelipe/bayesian-ab-exercises/blob/main/bayesian_ab_exercise2.ipynb)

## Tech stack

Python, NumPy, SciPy, pandas, Matplotlib, PyMC, ArviZ, Jupyter

## Running it yourself

```bash
conda env create -f environment.yml
conda activate bayesian-ab
jupyter lab
```
