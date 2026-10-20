# Reproducibility notes

## Experimental environment

- Python: 3.13.15
- NumPy 2.1.3
- Pandas 2.2.3
- SciPy 1.16.3
- Scikit-learn 1.6.1
- Statsmodels 0.15.0
- NetworkX 3.7
- Matplotlib 3.10.0
- PyTorch 2.11.0+cu130
- PyTorch Geometric 2.8.1

The versions above reflect the environments inspected during the final reproducibility review and are specified in requirements.txt. They are not independently verified as the exact versions used in the original model-training runs.

The original reproducibility notes also recorded an NVIDIA Tesla T4 GPU and CUDA 12.8. These historical hardware details have not been independently reverified.

The primary model experiments used random seed 42. Additional robustness analysis considered seeds 42, 123 and 456.



## Forecasting design

- Weekly aggregation
- Eight lagged demand observations per node
- One-step-ahead weekly forecasting horizon
- Chronological training, validation and test partitions
- Validation-based hyperparameter selection

## Execution order

Run each notebook from the first cell to the last after placing the required data in the `data/` directory.
Note: The multi-seed robustness analysis requires the prediction files corresponding to seeds 42, 123 and 456. These files must be generated or made available at the paths specified in the notebooks before executing the multi-seed analysis sections.

## Industrial validation

The validation notebook is included for methodological transparency. Reproduction requires authorised access to the anonymised industrial dataset. The raw industrial dataset must not be uploaded, redistributed or committed to version control.
