# EU Circular Medical Device Adoption Framework (EUCMDAF)

## Overview

This repository contains the code and supporting material used in the paper:

**"EU Circular Medical Device Adoption Framework (EUCMDAF): Combining Regulatory Analytics and EUDAMED Registry Data for Circular Medical Device Adoption"**

The study investigates how national regulatory conditions influence the adoption potential of circular and digital medical devices across European markets.

The repository provides:

* EUDAMED data preparation and feature engineering workflows.
* Regulatory Circularity Quotient (RCQ) calculations.
* AHP weighting files and consistency checks.
* Clustering and logistic regression analyses.
* Feature definitions and codebooks supporting reproducibility.

---

## Repository Structure

### notebooks/

Contains the Jupyter notebook used for the CRISP-DM workflow:

* Data understanding
* Data preparation
* Feature engineering
* Modeling
* Evaluation

### source/

Contains the original EUDAMED tables and external reference files.

### ahp/

Contains the pairwise comparison matrix and AHP calculations used for deriving the RCQ criterion weights.

### codebooks/

Contains definitions of analytical variables and the RCQ scoring framework.

---

## Data

The repository contains the EUDAMED snapshot used during model development together with the EMDN nomenclature reference list provided by the European Commission.

The EMDN list was used to derive intermediate device categories from nomenclature codes to create a more stable functional classification than device names while preserving higher granularity than top-level EMDN classes.

---

## Reproducibility

This repository provides:

* RCQ codebook and scoring logic,
* AHP pairwise comparison matrix,
* criterion weights,
* consistency ratio calculations,
* feature definitions,
* clustering and regression scripts.

These materials support methodological transparency and reproducibility.

---

## Software Requirements

Python 3.12

Install dependencies:

pip install -r requirements.txt

---

## Citation

If you use this repository, please cite:

Gonzalez Guevara, P., Zhou, R., Petke, P., et al. (2026). EU Circular Medical Device Adoption Framework (EUCMDAF): Code and AHP calculation files. GitHub repository.
