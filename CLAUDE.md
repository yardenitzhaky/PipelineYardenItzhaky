# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a data science project for credit card fraud detection analysis. The project contains a comprehensive Jupyter notebook pipeline that analyzes a credit card fraud dataset using various machine learning and statistical techniques.

## Key Files

- **Pipeline_YardenItzhaky_211583588.ipynb** - Main analysis notebook containing the complete data science pipeline
- **credit_card_fraud_dataset.csv** - Credit card transaction dataset (100,000 transactions, 7 columns)
- **pipeline_env/** - Python virtual environment for project dependencies

## Python Environment

The project uses a Python virtual environment located in `pipeline_env/` with Python 3.13.2. To activate the environment:

```bash
source pipeline_env/bin/activate
```

## Dataset Structure

The credit card fraud dataset contains:
- **TransactionID**: Unique transaction identifier
- **TransactionDate**: Transaction timestamp
- **Amount**: Transaction amount ($1.05 - $4,999.77)
- **MerchantID**: Merchant identifier (1-1000)
- **TransactionType**: "purchase" or "refund"
- **Location**: Transaction location (10 US cities)
- **IsFraud**: Target variable (0=legitimate, 1=fraud, 1% fraud rate)

## Pipeline Architecture

The notebook implements a structured 10-stage data science pipeline:

1. **Dataset Selection** - Business justification and data overview
2. **File System Analysis** - Data loading and validation
3. **Metadata Inspection** - Structure and quality analysis
4. **Descriptive Statistics** - Statistical analysis of all features
5. **Outlier Detection** - Anomaly identification and fraud correlation
6. **Clustering Analysis** - K-means customer segmentation
7. **Segment Analysis** - Cluster profiling and interpretation
8. **Categorical Analysis** - Transaction type and location patterns
9. **Visualization** - Comprehensive charts and graphs
10. **Model Building** - Machine learning fraud detection models

## Key Libraries Used

- **pandas, numpy** - Data manipulation and analysis
- **matplotlib, seaborn** - Data visualization
- **scikit-learn** - Machine learning models and preprocessing
- **wordcloud** - Text visualization (for categorical analysis)

## Analysis Highlights

- **Class Imbalance**: 99% legitimate vs 1% fraudulent transactions
- **Feature Engineering**: Temporal features extracted from transaction dates
- **Clustering**: K-means with 3-4 optimal clusters based on silhouette analysis
- **Best Model**: Random Forest with balanced class weights
- **Performance**: AUC 0.85-0.95 range expected for fraud detection

## Data Science Methodology

The pipeline follows best practices:
- Stratified sampling for model training
- Cross-validation for robust evaluation
- Feature importance analysis
- Comprehensive visualization suite
- Business-focused insights and recommendations

## Running the Analysis

To execute the full pipeline:
1. Activate the virtual environment
2. Launch Jupyter: `jupyter notebook`
3. Open `Pipeline_YardenItzhaky_211583588.ipynb`
4. Run cells sequentially or use "Run All"

The notebook is designed to run end-to-end without manual intervention, with all dependencies and data paths properly configured.