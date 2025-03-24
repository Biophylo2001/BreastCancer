# Breast Cancer Survival Prediction using METABRIC Dataset

This project explores clinical and genetic factors affecting overall survival in breast cancer patients using the METABRIC dataset. It applies preprocessing, statistical analysis, correlation exploration, and multiple linear regression models (including regularized and polynomial regression) to predict survival time in months.

##  Dataset

- **Source**: [Kaggle - METABRIC: Breast Cancer Gene Expression Profiles](https://www.kaggle.com/datasets/raghadalharbi/breast-cancer-gene-expression-profiles-metabric)
- **Files Used**:
  - `final_cleaned_METABRIC.csv`: Preprocessed version with selected relevant features.
  - `final_labeled_METABRIC.csv`: Encoded categorical variables for regression modeling.

##  Methods

- Label encoding for categorical features (`type_of_breast_surgery`, `cancer_type_detailed`, `cellularity`)
- Summary statistics and histograms for data exploration
- Correlation analysis (Pearson) with heatmaps and scatter plots
- Train-test split (80-20), verified with Kolmogorov-Smirnov test for representativeness
- Model training:
  - **Linear Regression (Closed-form)**
  - **Regularized Regression using SGD**:
    - Ridge (L2), Lasso (L1), Elastic Net (L1+L2)
  - **Polynomial Regression** with regularization
- Evaluation with:
  - Mean Squared Error (MSE)
  - R² Score
  - Training vs Validation Loss Visualization

##  Analysis

- Strongest negative correlations with survival time:
  - Nottingham Prognostic Index
  - Number of positive lymph nodes
- Regularized models (especially Elastic Net with α=1.0) showed improved generalization over plain linear regression.
- Polynomial regression captured more complexity but required stronger regularization to avoid overfitting.

##  Technologies Used

- Python (Pandas, NumPy, Matplotlib, Seaborn, scikit-learn)
- Jupyter Notebook

##  Results

- Best Model: **Elastic Net Regression (α=1.0)**
- Test MSE: ~5376
- R² Score: ~0.11 (Model captures some variance but underfits; future improvements needed)

##  Future Improvements

- Feature selection (Lasso, PCA)
- Ensemble models (e.g., Random Forest, XGBoost)
- Neural networks for capturing non-linear patterns
- Enhanced hyperparameter tuning and cross-validation

##  Author

**Sanyukta Chapagain**  
M.S. in Bioinformatics  
GitHub: [@Biophylo2001](https://github.com/Biophylo2001)

---

*Disclaimer: This project was created as part of coursework. ChatGPT was used for code structuring and explanation guidance.*
