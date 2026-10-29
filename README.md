# Week 2: House Price Regression

This project uses four notebooks to predict house sale prices in USD from Kaggle's House Sales in King County, USA dataset:

- `Dataset_clean.ipynb` downloads and cleans the data, then saves `Cleaned_Datasets/house_sales_clean.csv`.
- `Exploratory_data_analysis.ipynb` summarizes the cleaned data and displays plots.
- `Model_Training.ipynb` filters highly correlated features, scales the data, fits Ridge, Lasso, and Elastic Net, and compares their held-out test results.
- `Random_Forest_Training.ipynb` fits a Random Forest model on the same features and test split for comparison.

## Run the project

In a terminal opened in this folder, create and activate a virtual environment:

```bash
python3 -m venv .venv
source .venv/bin/activate
```

Install the requirements, then open each notebook in VS Code and select the `.venv` Python kernel:

```bash
python -m pip install -r requirements.txt
```

Run the notebooks in this order: `Dataset_clean.ipynb`, `Exploratory_data_analysis.ipynb`, `Model_Training.ipynb`, then `Random_Forest_Training.ipynb`. The target is `price`; each model reports test-set MAE, RMSE, and R-squared.

Internet access is needed to download the dataset. Kaggle may ask you to configure account access before the first download.

## Model Comparison

Results on the held-out test set:

| Model | MAE (USD) | RMSE (USD) | R-squared |
| --- | ---: | ---: | ---: |
| Ridge | 124,398.96 | 211,429.56 | 0.701 |
| Lasso | 125,872.81 | 210,204.11 | 0.705 |
| Elastic Net | 124,262.16 | 217,942.92 | 0.682 |
| Random Forest | 72,415.01 | 142,467.80 | 0.864 |

## Conclusion

Random Forest performed best on this test split, with the lowest MAE and RMSE and the highest R-squared. Results may vary with a different data split or model settings.
