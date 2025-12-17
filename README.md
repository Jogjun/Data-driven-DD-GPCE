# Data-driven DD-GPCE

Data-driven **Dimensionally Decomposed Generalized Polynomial Chaos Expansion (DD-GPCE)** for forward uncertainty quantification with **unknown input distributions**.

This repository provides a Jupyter notebook implementation of a data-driven DD-GPCE framework that constructs measure-consistent orthonormal polynomial bases directly from sample data using kernel density estimation (KDE) and bootstrapping.

---

## Overview

Conventional GPCE and DD-GPCE methods require prior knowledge of input probability distributions.  
However, in many real-world engineering applications, such information is unavailable or unreliable.

This project proposes a data-driven DD-GPCE approach that:
- Infers input distributions directly from sample data
- Avoids high-dimensional KDE using dimension decomposition
- Constructs orthonormal polynomial bases via whitening transformation
- Enables efficient and accurate forward uncertainty quantification

---

## Input Data

Example input datasets used in the notebook can be downloaded from:

🔗 **Input data download:**  
https://drive.google.com/file/d/1ajNCALMUUJoiaWKuB4lxiSvnofsOaJyw/view?usp=drive_link

Place the downloaded input data in the same folder as the notebook (or update paths accordingly).

---

## Key Features

- Data-driven input distribution estimation (KDE + bootstrap)
- Dimensionally decomposed marginal KDE for high-dimensional problems
- Monte Carlo–based whitening transformation
- Measure-consistent orthonormal polynomial basis construction
- DD-GPCE surrogate modeling
- Accurate estimation of output mean and variance

---

## Repository Structure

├── Data-driven DD-GPCE.ipynb # Main notebook (implementation & examples)
├── input_data/ # (optional) download location for input datasets
└── README.md # Project description


---

## Methodology

1. **Input distribution estimation**  
   Input probability distributions are inferred from data using kernel density estimation with smoothed bootstrap for robustness.

2. **Dimension decomposition**  
   Only low-dimensional marginal distributions are estimated, avoiding the curse of dimensionality.

3. **Whitening transformation**  
   A Monte Carlo–based whitening process is used to map samples to a standard probability space.

4. **DD-GPCE construction**  
   The output response is decomposed into low-order interaction components and approximated using orthonormal polynomial bases.

5. **Uncertainty quantification**  
   The surrogate model is used to compute output statistics such as mean and variance and is validated against Monte Carlo simulation.

---

## Numerical Examples

- Mathematical benchmark problems
- Comparison with Monte Carlo simulation results
- Performance comparison with conventional data-driven DD-GPCE assuming Gaussian input distributions
- Demonstration of improved accuracy in mean and variance estimation

---

## Requirements

- Python 3.8 or higher
- numpy
- scipy
- scikit-learn
- matplotlib
- joblib

---

## Usage

Run the notebook using:

```bash
jupyter notebook "Data-driven DD-GPCE.ipynb"
