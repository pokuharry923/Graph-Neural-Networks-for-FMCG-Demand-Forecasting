# Graph-Based FMCG Demand Forecasting

This repository contains the implementation used for an MSc research project on demand forecasting with Social Network Analysis (SNA) and Graph Neural Networks (GNNs).

## Research workflow

1. Prepare weekly product-demand observations.
2. Construct a weighted product co-purchase network.
3. analyse network structure using SNA.
4. formulate one-step-ahead weekly node-level forecasting.
5. train and compare ARIMA, MLP, GCN, GraphSAGE and SAGE_NoGraph.
6. evaluate performance using RMSE, MAE, MAPE, R² and the Diebold–Mariano test.
7. validate the benchmark findings using an anonymised industrial FMCG dataset.
8. Apply Holm correction to the statistical significance tests.
9. Estimate bootstrap confidence intervals for forecasting performance.
10. Assess model robustness using multiple random seeds (42, 123 and 456).


## Repository structure

```text
.
├── notebooks/
│   ├── 01_benchmark_instacart.ipynb
│   └── 02_industrial_validation.ipynb
├── data/
│   └── README.md
├── results/
├── figures/
├── docs/
│   └── REPRODUCIBILITY.md
├── requirements.txt
├── .gitignore
└── README.md
```

## Installation

Create and activate a Python environment, then install the required packages:

```bash
python -m venv .venv
# Windows
.venv\Scripts\activate
# macOS/Linux
source .venv/bin/activate

pip install -r requirements.txt
```

## Data access

The public benchmark experiment uses the Instacart Online Grocery Shopping Dataset. Follow the instructions in `data/README.md`.

The anonymised industrial FMCG dataset is confidential and is not included. Access is restricted to supervisors and authorised reviewers.


The Instacart benchmark dataset is available at:
https://www.kaggle.com/datasets/yasserh/instacart-online-grocery-basket-analysis-dataset

The original dataset is not redistributed in this repository.
See `data/README.md` for dataset preparation instructions.


## Running the experiments

Launch Jupyter and run the notebooks in order:

```bash
jupyter notebook
```

1. `notebooks/01_benchmark_instacart.ipynb`
2. `notebooks/02_industrial_validation.ipynb` — authorised reviewers only

## Reproducibility


The primary experiments use random seed 42. Additional multi-seed
robustness analysis considers seeds 42, 123 and 456.

The software dependencies are pinned in `requirements.txt`.
Python 3.13.15 was reported in the documented Colab environments.

The notebooks include Diebold–Mariano testing, Holm correction,
bootstrap confidence intervals and multi-seed analysis.

Further execution and environment information is provided in
`docs/REPRODUCIBILITY.md`.


## Confidentiality

No raw industrial data, customer identities, organisation names or confidential business records are distributed in this repository.
