# Credit Card Fraud Detection Analysis

A comprehensive data science project analyzing credit card transaction patterns to identify fraudulent activities using statistical analysis, clustering, and machine learning techniques.

## Project Overview

This project examines a dataset of 100,000 credit card transactions to understand fraud patterns and build detection models. The analysis includes data exploration, statistical testing, clustering analysis, and machine learning model development.

## Dataset

- **Size:** 100,000 transactions
- **Features:** 7 columns including transaction details, merchant info, and location
- **Target:** Binary fraud indicator (1% fraud rate)
- **Quality:** Clean dataset with no missing values

## Key Findings

- Fraud occurs across all transaction amounts and times
- Geographic patterns show slight variations in fraud rates
- Machine learning models achieve ~70-80% fraud detection rate
- Random Forest outperforms Logistic Regression for this task


## Getting Started

### Prerequisites

- Python 3.13+
- Jupyter Notebook or JupyterLab

### Installation

1. **Clone or download the project**
2. **Activate the virtual environment:**
   ```bash
   source pipeline_env/bin/activate
   ```
3. **Start Jupyter:**
   ```bash
   jupyter notebook
   ```
4. **Open the notebook:**
   - Navigate to `Pipeline_YardenItzhaky_211583588.ipynb`
   - Run cells sequentially from top to bottom

## Analysis Pipeline

1. **Data Loading & Exploration** - Dataset overview and quality checks
2. **Statistical Analysis** - Fraud patterns across different dimensions
3. **Outlier Detection** - Identifying unusual transaction patterns
4. **Clustering Analysis** - Grouping transactions to find patterns
5. **Visualization** - Comprehensive fraud pattern charts
6. **Machine Learning** - Building and evaluating fraud detection models

## Key Technologies

- **Data Analysis:** pandas, numpy, scipy
- **Machine Learning:** scikit-learn
- **Visualization:** matplotlib, seaborn
- **Statistical Analysis:** Statistical testing and clustering

## Results

The analysis successfully identifies patterns in fraudulent transactions and builds machine learning models capable of detecting fraud with reasonable accuracy while maintaining low false alarm rates.
