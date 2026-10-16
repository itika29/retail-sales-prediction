# Retail Sales Analysis and Sales Prediction Using Linear Regression

**Intern:** Itika Kansal  
**Internship Track:** Data Analytics and Machine Learning  
**Dataset:** [Superstore Sales Dataset – Kaggle (vivek468)](https://www.kaggle.com/datasets/vivek468/superstore-dataset-final)

---

## Project Overview

This project performs an end-to-end data analytics and machine-learning pipeline on a real retail dataset.
Starting from raw CSV data, the project covers cleaning, exploratory analysis, business KPI calculation,
data visualisation, and a Linear Regression model that predicts monthly sales.

The deliverables are designed to be beginner-friendly and suitable for presentation at an internship evaluation.

---

## Objectives

| # | Objective |
|---|-----------|
| 1 | Load, clean, and validate the raw Superstore dataset |
| 2 | Compute business KPIs: total sales, profit margin, regional performance |
| 3 | Visualise monthly trends, growth rates, and category-level profitability |
| 4 | Train a Linear Regression model to predict monthly sales (no data leakage) |
| 5 | Generate a 3-month sales forecast with clearly stated model limitations |
| 6 | Derive five key findings, three risks, three opportunities, and five actions |

---

## Technologies

| Library | Purpose |
|---------|---------|
| Python 3.9+ | Core language |
| Pandas | Data loading, cleaning, and aggregation |
| NumPy | Numerical operations and array handling |
| Matplotlib | Custom chart plotting |
| Seaborn | Statistical visualisation styling |
| Scikit-learn | LinearRegression, MAE, RMSE, R² |
| Jupyter Notebook | Interactive, reproducible analysis |

---

## Folder Structure

```
Sales_Growth_KPI_Project/
│
├── data/
│   └── Sample - Superstore.csv          ← Raw dataset (from Kaggle)
│
├── Itika_SalesPrediction_Project.ipynb  ← Main notebook (PRIMARY DELIVERABLE)
├── Itika_SalesPrediction_ProjectReport.docx  ← Written project report
├── requirements.txt                      ← Python dependency list
└── README.md                             ← This file
```

---

## How to Run

### 1. Install dependencies

Open a terminal in this project folder and run:

```bash
pip install -r requirements.txt
```

### 2. Launch Jupyter Notebook

```bash
python -m notebook
```

Or use JupyterLab (more modern interface):

```bash
python -m jupyterlab
```

Then open `Itika_SalesPrediction_Project.ipynb` from the browser interface.

> **Note:** If `jupyter` is not recognised as a command, always use `python -m notebook` or
> `python -m jupyterlab` — this works regardless of whether the Python Scripts folder is on your PATH.

### 3. Run all cells

Use **Kernel → Restart & Run All** to execute every cell from top to bottom.

> **Important:** Always run cells in order. Later sections depend on variables created in earlier ones.

---

## Dataset

- **Source:** [Kaggle – Superstore Dataset (vivek468)](https://www.kaggle.com/datasets/vivek468/superstore-dataset-final)
- **File:** `data/Sample - Superstore.csv`
- **Records:** ~9,994 sales transactions
- **Coverage:** 2014 – 2017, US retail stores
- **Key columns:** Order Date, Sales, Profit, Quantity, Discount, Region, Category, Sub-Category

---

## Deliverables

| File | Description |
|------|-------------|
| `Itika_SalesPrediction_Project.ipynb` | Complete, annotated Jupyter Notebook |
| `requirements.txt` | Pinned library versions for reproducibility |
| `Itika_SalesPrediction_ProjectReport.docx` | Written project report |
| `README.md` | Project overview and run instructions |

---

## Notebook Sections

| Section | Contents |
|---------|----------|
| 0 – Imports | All library imports and plot style setup |
| 1 – Data Cleaning | Load CSV, fix dtypes, parse dates, remove duplicates, validate numerics |
| 2 – EDA | KPIs, regional sales, category/sub-category profit, monthly trend, growth rate |
| 3 – Visualisations | 5 EDA charts (monthly trend, growth rate, region, category, scatter) |
| 4 – Machine Learning | Monthly aggregation, chronological split, model training, MAE/RMSE/R², forecast |
| 5 – Business Insights | 5 findings, 3 risks, 3 opportunities, 5 recommended actions |
| 6 – Conclusion | Summary of learnings and next steps |

---

## Model Details

- **Algorithm:** `sklearn.linear_model.LinearRegression`
- **Feature:** Chronological month index (integer 1, 2, 3 …)
- **Target:** Monthly total sales ($)
- **Split strategy:** Chronological — last 12 months held out as test set (no shuffling)
- **Evaluation metrics:** MAE, RMSE, R²
- **Forecast horizon:** 3 months ahead
- **Known limitations:** No seasonality, no external variables, linear extrapolation only

---

*Made with Python · Pandas · Scikit-learn · Matplotlib*
