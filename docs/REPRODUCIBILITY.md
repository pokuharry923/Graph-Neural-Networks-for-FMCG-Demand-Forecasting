# Reproducibility notes

## Experimental environment

- Python: 3.12.13
- PyTorch: 2.11.0
- PyTorch Geometric: 2.8.0
- NumPy: 2.0.2
- Pandas: 2.2.2
- NetworkX: 3.6.1
- Statsmodels: 0.14.6
- Scikit-learn: 1.6.1
- CUDA: 12.8
- GPU used in the reported experiments: NVIDIA Tesla T4
- Random seed: 42

## Forecasting design

- Weekly aggregation
- Eight lagged demand observations per node
- One-step-ahead weekly forecasting horizon
- Chronological training, validation and test partitions
- Validation-based hyperparameter selection

## Execution order

Run each notebook from the first cell to the last after placing the required data in the `data/` directory.

## Industrial validation

The validation notebook is included for methodological transparency. Reproduction requires authorised access to the anonymised industrial dataset. The raw industrial dataset must not be uploaded, redistributed or committed to version control.
