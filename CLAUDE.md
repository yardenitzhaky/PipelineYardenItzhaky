# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a data science project focused on credit card fraud detection analysis. The main work is contained in a Jupyter notebook that performs comprehensive analysis including statistical analysis, clustering, visualization, and machine learning model development.

## Environment Setup

### Python Virtual Environment
- **Environment location**: `pipeline_env/` directory
- **Python version**: 3.13.2
- **Activate environment**: `source pipeline_env/bin/activate` (on macOS/Linux)

### Key Dependencies
- **Data Analysis**: pandas (2.2.3), numpy (2.2.6), scipy (1.15.3)
- **Machine Learning**: scikit-learn (1.6.1), shap (0.47.2)
- **Visualization**: matplotlib (3.10.3), seaborn (0.13.2), wordcloud (1.9.4)
- **Text Processing**: nltk (3.9.1), textblob (0.19.0)
- **Performance**: numba (0.61.2), joblib (1.5.1)

## Project Structure

### Core Files
- **`Pipeline_YardenItzhaky_211583588.ipynb`**: Main analysis notebook containing the complete data science pipeline
- **`credit_card_fraud_dataset.csv`**: Dataset with 100,000 credit card transactions (6.4MB)
- **`pipeline_env/`**: Python virtual environment with all required packages

### Dataset Information
- 100,000 transactions with 7 features
- Target variable: `IsFraud` (1% fraud rate)
- Features include: TransactionID, TransactionDate, Amount, MerchantID, TransactionType, Location
- No missing values, clean dataset

## Development Workflow

### Running the Analysis
1. Activate virtual environment: `source pipeline_env/bin/activate`
2. Start Jupyter: `jupyter notebook` or `jupyter lab`
3. Open `Pipeline_YardenItzhaky_211583588.ipynb`
4. Run cells sequentially for complete analysis

### Code Execution
- The notebook is designed to run sequentially from top to bottom
- All necessary imports are in the first code cell
- Helper functions are defined before use
- Visualizations are embedded throughout the analysis

## Analysis Pipeline Architecture

### 1. Data Loading and Exploration
- Automated data loading with error handling
- Comprehensive data quality checks
- Statistical summary generation

### 2. Statistical Analysis
- Time-based feature extraction from transaction dates
- Categorical and numerical feature analysis
- Fraud pattern identification across different dimensions

### 3. Outlier Detection
- IQR-based outlier identification
- Statistical significance testing
- Special case analysis (high-value, off-hours transactions)

### 4. Clustering Analysis
- K-means clustering with feature scaling
- Silhouette score evaluation
- PCA visualization for cluster interpretation

### 5. Machine Learning Pipeline
- Balanced sampling for imbalanced dataset
- Feature engineering (encoded categories, derived features)
- Model comparison (Logistic Regression vs Random Forest)
- Cross-validation and comprehensive evaluation metrics

### 6. Visualization Dashboard
- Multi-panel fraud pattern visualizations
- ROC and Precision-Recall curves
- Feature importance plots
- Interactive exploration charts

## Key Technical Patterns

### Data Handling
- Uses pandas for data manipulation with proper datetime parsing
- Implements label encoding for categorical features
- Applies standard scaling for ML features

### Model Evaluation
- Focuses on AUC-PR over accuracy due to class imbalance
- Uses stratified cross-validation
- Employs comprehensive metrics (precision, recall, F1, AUC-ROC, AUC-PR)

### Code Organization
- Helper functions to avoid code duplication
- Modular analysis sections
- Clear separation between exploration and modeling

## Important Notes

### Class Imbalance Handling
- Dataset has severe class imbalance (1% fraud)
- Uses `class_weight='balanced'` in models
- Sampling strategy balances fraud/legitimate cases for ML

### Performance Considerations
- Large dataset requires sampling for some ML operations
- Uses efficient pandas operations and vectorization
- Notebook includes memory usage monitoring

### Reproducibility
- All random operations use `random_state=42`
- Environment dependencies are locked to specific versions
- Clear documentation of analysis steps and decisions

## Typical Development Tasks

### Adding New Analysis
1. Follow existing pattern of markdown explanation followed by code
2. Use helper functions where possible to maintain consistency
3. Include visualizations and interpretations
4. Update summary sections with new findings

### Model Improvements
1. Add new models to the `models` dictionary in the ML section
2. Ensure consistent evaluation metrics
3. Update comparison visualizations
4. Document model-specific considerations

### Data Updates
1. Modify `load_data()` function for new dataset paths
2. Update feature engineering if schema changes
3. Verify all analysis sections work with new data structure
4. Rerun complete pipeline to ensure consistency