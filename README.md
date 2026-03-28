**COMPAS Fairness Analysis – Python Replication**


**1. Purpose of the Analysis**

This project replicates, in Python, the machine learning workflow demonstrated in R for DNSC 6330 (Responsible Machine Learning) Lecture 01 on the COMPAS recidivism dataset.

The goals are to:

- Reproduce the exploratory data analysis (EDA), preprocessing, and filtering steps used in the R script.
- Implement an equivalent logistic regression model in Python. 
- Recreate model evaluation and fairness diagnostics and interpret any differences.


**2. Data and Problem Description**

The analysis uses the public COMPAS dataset released by ProPublica and referenced in the lecture materials.

- Source URL:  

[  `https://raw.githubusercontent.com/propublica/compas-analysis/master/compas-scores-two-years.csv`](https://raw.githubusercontent.com/propublica/compas-analysis/master/compas-scores-two-years.csv)

Key tasks:
- Clean and filter the data to match the cohort used in the lecture 
- Construct features such as age, race, priors, charge degree, and a binary risk label based on COMPAS decile scores. 
- Fit a logistic regression model predicting high vs. low COMPAS risk scores and evaluate performance and group-conditional error rates. 


**3. Python Environment and Libraries**

This project was implemented and tested in Python 3.x using Jupyter Notebook.

Main libraries used:
- `pandas` – data loading, cleaning, and manipulation
- `numpy` – numerical operations
- `matplotlib` / `seaborn` – descriptive plots and EDA visualizations
- `statsmodels` – logistic regression model with formula syntax and summaries
- `scikit-learn` – confusion matrices and evaluation utilities


**4. Repository Structure**

Suggested structure:

text
.
- ├── README.md                 # This file
- └── compas\_analysis.ipynb     # Jupyter notebook with full Python workflow

compas\_analysis.ipynb contains the full pipeline:

- Data loading from the ProPublica GitHub URL
- Preprocessing and filtering to match the R script
- EDA summaries and basic plots
- Logistic regression model
- Confusion matrices overall and by race
- Fairness metrics (FPR, FNR, disparities) 


**5. How to Reproduce the Results**

Clone or download this repository.

Install required packages:

`pip install -r requirements.txt`

Launch Jupyter Notebook:

`jupyter notebook`

Open compas_analysis.ipynb and run all cells from top to bottom.

The notebook will:

- Download the COMPAS dataset from the public URL.
- Apply the same filters and transformations described in the R script.
- Fit the logistic regression model and compute evaluation metrics.
- Produce confusion matrices and group-conditional metrics needed for the fairness discussion.


**6. Notes on Alignment with the R Workflow**

The Python pipeline follows the R steps shown in Lecture 01 as closely as possible in terms of:

- Variables retained
- Filtering rules
- Model formula structure
- Definition of binary high-risk labels and group-specific metrics 

Small numerical differences may arise due to library implementations or default options, but the conceptual results should match the R analysis. 

