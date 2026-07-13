# Dataset setup

## Benchmark dataset

Download the Instacart Online Grocery Shopping Dataset from its authorised public source and extract the files into:

```text
data/instacart/
```

The benchmark notebook expects at least:

```text
orders.csv
products.csv
order_products__prior.csv
```

Do not commit the downloaded dataset to GitHub.

## Industrial validation dataset

The industrial validation dataset is confidential and is not included in this repository.

Authorised reviewers may place the anonymised file at:

```text
data/industrial_fmcg_anonymised.csv
```

The file must retain the anonymised column structure expected by the validation notebook. Do not commit this file.
