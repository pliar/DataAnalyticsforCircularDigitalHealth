# EU Circular Medical Device Adoption Framework (EUCMDAF)

## Overview
This repository contains the analytical workflow, regulatory scoring logic, and modelling components used in the study:

**“EU Circular Medical Device Adoption Framework (EUCMDAF): Combining Regulatory Analytics and EUDAMED Registry Data for Circular Medical Device Adoption.”**

The framework integrates:
- Regulatory Circularity Quotient (RCQ)
- Analytic Hierarchy Process (AHP) weighting
- EUDAMED-based device and market analytics incl. Logistic regression, clustering, and MCDA modelling

---

## Repository Structure

### `/analysis`
Contains the full CRISP-DM analytical workflow implemented in a Jupyter Notebook (`.ipynb`), including:
- data understanding  
- data preparation  
- feature engineering  
- modelling  
- evaluation  

The subfolder `/analysis/source` contains the EUDAMED snapshot (October 2025) in form of 18 .csv files and the EMDN nomenclature list used to derive device categories (device_category.xlsx.

### `/ahp`
Contains the AHP weighting and consistency check file:

- **`ahp_weights_and_consistencycheck.xlsx`**  
  Includes the Saaty pairwise comparison matrix, normalized matrix, eigenvector weights, λ_max, CI, RI, and CR.  
  The resulting weights (w1–w5) are used to compute the RCQ.

### `/quotients`
Contains:
- **`Quotients_EN.docx`**  
  Summarizes the RCQ results for Germany, Denmark, and Croatia across MDR, IVDR, SUD, and WEEE regulatory areas.  
  These values feed directly into the regulatory layer of the EUCMDAF.

---

## Data Sources

### EUDAMED
EUDAMED is the EU’s central regulatory database for medical devices, established under MDR (EU 2017/745) and IVDR (EU 2017/746).  
It provides structured information on:
- device registrations  
- UDI attributes  
- certificates  
- market distribution  
- actor information  

Public interface:  
https://ec.europa.eu/tools/eudamed/#/screen/home

### EMDN (European Medical Device Nomenclature)
Official resources:
- https://webgate.ec.europa.eu/dyna2/emdn/

The EMDN list was used to derive intermediate device categories for modelling.

---

## Regulatory Circularity Quotient (RCQ)

The RCQ quantifies how enabling or restrictive national regulations are for circular medical device pathways.

### MCDA Criteria
1. Legal clarity & permissibility  
2. Additional compliance burden (inverted)  
3. Incentive & demand impact  
4. Data & traceability impact  
5. Operationalizability  

Each criterion uses a standardized 0–1 scale.

### AHP Weighting
Weights are derived from the AHP matrix in `ahp_weights_and_consistencycheck.xlsx`.  
Consistency ratio: **CR = 0.0059** (highly consistent).

### RCQ Results
The file `Quotients_EN.docx` provides the full scoring tables and final RCQ values for:
- Germany  
- Denmark  
- Croatia  

---

## EUCMDAF Framework

The EUCMDAF integrates:
1. **Regulatory layer**  
   - RCQ scores per country  
   - regulatory heterogeneity  
   - operational feasibility of circular pathways  

2. **Market adoption layer**  
   - logistic regression (circularity probability)  
   - K-means clustering (market maturity)  
   - composite Market Success Score  

Outputs include:
- cross-country adoption matrix  
- market segments  
- stakeholder-specific recommendations  

---

## Reproducibility

This repository provides:
- RCQ scoring codebook  
- AHP matrix, weights, and consistency check  
- feature definitions  
- clustering and regression scripts  
- EUDAMED data preparation workflows  
- device category mapping (EMDN-based)

