# AI-driven-epigenetic-clock-for-biological-age-estimation-and-disease-risk-prediction
AI-driven epigenetic clock for biological age estimation and disease risk prediction using DNA methylation data. Combines Elastic Net and XGBoost with SHAP-based explainability to deliver accurate, interpretable insights into aging and health risk.

- Overview

This project presents an Artificial Intelligence–based framework for estimating biological age and predicting disease risk using genome-wide DNA methylation data. Unlike traditional epigenetic clock models that focus only on chronological age prediction, this system integrates biological age estimation, age acceleration analysis, and multi-class disease classification within a single unified pipeline.

The project was developed and executed using Google Colab, enabling efficient handling of high-dimensional genomic data and easy reproducibility.

Problem Statement

Chronological age does not accurately reflect an individual's biological condition. People of the same age may exhibit different levels of physiological aging and disease susceptibility. While DNA methylation–based epigenetic clocks provide a promising solution, existing approaches:

- Focus mainly on age prediction
- Do not integrate disease risk modeling
- Lack interpretability
- Struggle with high-dimensional CpG data

This project addresses these limitations by developing an interpretable, AI-driven, disease-aware epigenetic clock.

Objectives:- 
- To estimate biological age using DNA methylation data
- To compute age acceleration as a biomarker
- To predict disease risk across multiple categories
- To build an interpretable AI model using SHAP
- To create a scalable pipeline using Google Colab
  
Dataset:- 

The dataset consists of genome-wide DNA methylation beta values along with metadata:

CpG methylation values (range: 0 to 1)
Chronological age
Disease labels

Disease Categories Included:
Alzheimer’s Disease
Parkinson’s Disease
Type 2 Diabetes
Stroke
Rheumatoid Arthritis
Autoimmune Disorders
Healthy Controls

The dataset is high-dimensional (p >> n), making it suitable for machine learning–based analysis.

Development Environment:- 

Platform: Google Colab
Language: Python 3.9
Execution: Cloud-based GPU/CPU environment

This ensures:

No local setup required
Easy reproducibility
Efficient computation for large datasets

Methodology:- 

1. Data Preprocessing
= Removed low-variance CpG features
= Selected relevant features using correlation with age
= Reduced dimensionality for efficient computation

2. Biological Age Prediction
   
Elastic Net Regression:- 
= Combines L1 and L2 regularization
= Performs feature selection
= Provides interpretable coefficients

XGBoost Regression:- 
= Gradient boosting algorithm
= Captures non-linear relationships
= Improves prediction accuracy

3. Age Acceleration

Age acceleration is computed as:

Age Acceleration = Predicted Age – Chronological Age

Positive → Accelerated aging
Negative → Healthy aging

Used as a key biomarker for disease analysis.

4. Disease Risk Prediction
   
- Multi-class classification using XGBoost
  
Input features:
= Selected CpG features
= Age acceleration

Output:
Disease prediction
Probability scores

5. Explainability (SHAP)
   
- Identifies important CpG features
- Explains model predictions
- Improves interpretability and trust
  
Results:- 

- Strong correlation between predicted biological age and chronological age
- XGBoost outperformed Elastic Net due to non-linear modeling capability
- Age acceleration showed clear variation across disease groups
- Disease prediction improved when age acceleration was included
- SHAP analysis highlighted key CpG sites influencing predictions
  
How to Run (Google Colab):-

1. Open the project notebook in Google Colab
2. Upload the dataset (HDF5 file)
3. Run all cells sequentially:
- Data preprocessing
- Model training
- Prediction
- SHAP analysis
4. Visualize outputs:
- Age prediction plots
- Age acceleration distribution
- Disease classification results
  
Technologies Used:-
- Python
- NumPy, Pandas
- Scikit-learn
- XGBoost
- SHAP
- Matplotlib
  
Applications:- 

- Biological age estimation
- Early disease risk detection
- Precision medicine
- Preventive healthcare
- Biomedical AI research
  
Limitations:- 

- Dataset imbalance across disease classes
- CpG sites not mapped to biological pathways

Future Work:- 

- Integration of multi-omics data (gene expression, proteomics)
- External validation using independent datasets
- Longitudinal aging analysis
- Mapping CpG sites to biological pathways
- Development of a clinical decision-support system

This project demonstrates the effectiveness of combining machine learning and DNA methylation data for biological age estimation and disease risk prediction. By integrating Elastic Net, XGBoost, and SHAP explainability, the framework provides accurate and interpretable insights into aging and disease mechanisms. The proposed system advances epigenetic clock research toward practical applications in precision and preventive healthcare.
