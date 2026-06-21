# Reproducibility

The repository preserves the original directory structure used during model development.

The Jupyter notebook `Final_EUDAMED_CRISPDM_Code_with_modeling.ipynb` and the corresponding `source/` directory are intentionally stored within the same folder.

This design avoids broken file paths and allows the complete CRISP-DM workflow to be reproduced without additional configuration.

All input datasets are loaded directly from the accompanying source directory using relative paths.

To reproduce the analysis: 
Open the notebook in /analysis. Ensure the datasets in /analysis/source remain in their original structure.

Install dependencies:
```bash
pip install -r requirements.txt

    
