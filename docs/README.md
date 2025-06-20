Project Overview:
A data-driven approach to customer segmentation using K-Means clustering, evaluating cluster quality with 
PCA optimization and validation metrics. Designed for marketing strategy optimization and customer behavior analysis.

This project implements an end-to-end customer segmentation pipeline using:
K-Means clustering for unsupervised grouping
PCA dimensionality reduction for visualization and performance improvement
Silhouette Analysis & Davies-Bouldin Index for validation

Business Objective: Identify distinct customer groups based on spending behavior, credit patterns, and payment 
habits to enable targeted marketing strategies.

Repository Structure:
K-Means-Clustering-Analysis/
├── data/
│ ├── raw/ Original dataset (clusteringDataset.csv) 
├── notebooks/
│ ├── 1_Data_Exploration.ipynb 
│ ├── 2_KMeans_Baseline.ipynb 
│ ├── 3_PCA_Transformation & imrpoved clustering.ipynb 
│ ├── 4_DBI after PCA.ipynb 
│ └──5_silhouette evaluation.ipynb 
├── src/
│ ├── preprocessing.ipynb
│ └── evaluation.ipynb
├── output files/
│ ├── visualizations/ 
| └── metrics/ 

Installation Guide:
System Requirements:
Python 3.8+ (Anaconda recommended)
4GB RAM minimum
Jupyter Notebook/Lab

requirements:
numpy==1.21.4
pandas==1.3.5
scikit-learn==1.0.2
matplotlib==3.5.1
seaborn==0.11.2
plotly==5.8.0
jupyter==1.0.0
ipywidgets==7.6.5 # For interactive visuals

Data Pipeline:
Source: Internal CRM database
Size: 8,950 records × 18 features

Key Features:
BALANCE: Account balance
PURCHASES: Total purchase amount
CREDIT_LIMIT: Allocated credit
PAYMENTS: Payment history
MINIMUM_PAYMENTS: Minimum due payments

Preprocessing:
Handle missing values and Normalize the data

Modeling:
k-baselime model:
-Optimal k Selection
-PCA Optimization
 Variance Explained:
Component	Variance (%)
PC1          62.3
PC2	         23.1
Cumulative   85.4
-PCA Transformation

Evaluation:
Metric	         
Silhouette: Before PCA : 0.338, After PCA : 0.438	         
Davies-Bouldin: Before PCA :	1.416, After PCA :	0.817

Silhouette Score & Davies-Bouldin Index (DBI) in K-Means Clustering:
Silhouette Score (0 to 1) measures cluster cohesion vs. separation (higher = better-defined clusters). 
Davies-Bouldin Index (DBI) (≥ 0) quantifies cluster compactness and separation (lower = better). Together, 
they validate optimal k in K-Means—maximize Silhouette while minimizing DBI for robust clustering.
