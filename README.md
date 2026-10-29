# Week 2: House Price Regression

This project uses three  notebooks to predict house sale prices in USD from Kaggle's House Sales in King County, USA dataset:

- `Dataset_clean.ipynb` downloads and cleans the data, then saves `Cleaned_Datasets/house_sales_clean.csv`.
- `Exploratory_data_analysis.ipynb` summarizes the cleaned data and displays plots.
- `Model_Training.ipynb` filters highly correlated features, scales the data, fits Ridge, Lasso, and Elastic Net, and compares their held-out test results.

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

Run the notebooks in this order: `Dataset_clean.ipynb`, `Exploratory_data_analysis.ipynb`, then `Model_Training.ipynb`. The model notebook uses a training-data heatmap to remove one feature from each pair above 0.85 absolute correlation. Its target is `price`; it reports test-set MAE, RMSE, and R-squared for each model.

Internet access is needed to download the dataset. Kaggle may ask you to configure account access before the first download.# Week-2-Target-Regression--US-House-prediction
