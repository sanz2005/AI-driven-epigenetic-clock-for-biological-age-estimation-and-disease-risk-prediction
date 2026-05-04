# AI-driven-epigenetic-clock-for-biological-age-estimation-and-disease-risk-prediction
AI-driven epigenetic clock for biological age estimation and disease risk prediction using DNA methylation data. Combines Elastic Net and XGBoost with SHAP-based explainability to deliver accurate, interpretable insights into aging and health risk.
This project presents an artificial intelligence–based framework for estimating biological age and predicting disease risk using genome-wide DNA methylation data. The proposed system integrates Elastic Net regression and XGBoost models to capture both linear and non-linear relationships among CpG methylation features. In addition to biological age estimation, the framework computes age acceleration as a biomarker and incorporates it into a multi-class disease prediction model. SHAP-based explainability is used to provide interpretable insights into CpG-level feature contributions.

Objectives

The primary objectives of this project are:

To estimate biological age using DNA methylation data
To compute age acceleration and analyze its association with diseases
To develop a multi-class disease prediction model
To ensure model interpretability using explainable AI techniques
Dataset

The project uses a DNA methylation dataset containing genome-wide CpG beta values along with chronological age and disease annotations. The beta values range from 0 to 1 and represent methylation levels at specific CpG sites. The dataset includes samples from healthy individuals as well as multiple disease categories such as neurological, metabolic, and autoimmune disorders.

Methodology

The project follows a structured pipeline:

Data Preprocessing
Removal of low-variance CpG features
Selection of features based on correlation with chronological age
Biological Age Prediction
Elastic Net regression for linear modeling and feature selection
XGBoost regression for capturing non-linear relationships
Age Acceleration Calculation
Age acceleration is computed as:
Age Acceleration = Predicted Age – Chronological Age
Disease Risk Prediction
Multi-class classification using XGBoost
Input features include CpG methylation data and age acceleration
Explainability
SHAP is used to interpret model predictions and identify important CpG sites
Results

The model demonstrates strong predictive performance for biological age estimation, with XGBoost outperforming Elastic Net due to its ability to model complex feature interactions. Age acceleration analysis reveals distinct patterns across different disease categories, indicating its potential as a biomarker for disease risk. The disease classification model achieves reasonable performance, with improved accuracy when age acceleration is included as a feature. SHAP analysis provides meaningful insights into CpG contributions, enhancing interpretability.

Technologies Used
Python
NumPy and Pandas
Scikit-learn
XGBoost
SHAP
Matplotlib
Applications
Biological age estimation
Early disease risk prediction
Precision and preventive healthcare
Biomedical data analysis
Limitations
Dataset imbalance across disease classes
Lack of external validation dataset
Limited biological pathway mapping of CpG sites
Absence of clinical validation
Future Work
Integration of multi-omics data such as gene expression and proteomics
Validation using external and longitudinal datasets
Mapping CpG sites to biological pathways for better interpretation
Development of a clinical decision-support system
Conclusion

This project demonstrates the effectiveness of combining machine learning and epigenetic data for biological age estimation and disease risk prediction. By integrating interpretable and non-linear models, the framework provides accurate and meaningful insights into aging and disease mechanisms, with potential applications in precision medicine and preventive healthcare.
