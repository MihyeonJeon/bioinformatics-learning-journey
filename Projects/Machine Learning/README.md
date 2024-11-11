# Protein-Protein Interaction Prediction Model
This project was a team project from the Machine Learning course in VU Amsterdam, especially in a master's Bioinformatics and Systems Biology.
My role in this project was data preprocessing and feature selection based on data analysis.

## Background
Understanding biochemical processes and cellular pathways is fundamentally linked to knowledge of protein-protein interactions (PPIs), which are central to nearly every process in a living cell, including signaling, metabolism, and gene expression. Many diseases, such as cancer, Alzheimer's, and infectious diseases, are associated with abnormal protein interactions. Predicting these interactions is crucial for understanding how cells function and respond to different conditions. With high-throughput techniques, researchers can now identify PPIs across entire genomes for many model species. Databases such as the Human Protein Reference Database (HPRD), STRING, and others serve as repositories for these vast amounts of data, which include both experimentally verified and computationally predicted interactions. By predicting PPIs, researchers can identify potential disease mechanisms and targets for therapeutic intervention. Furthermore, machine learning (ML) significantly enhances PPI prediction by improving accuracy, efficiency, and the management of large datasets.

## Objective
This project aims to improve the accuracy of protein-protein interaction (PPI) prediction using a combination of machine learning models. Since the dataset had more than a hundred of features, the main focus was feature selection and preprocessing with R to ensure data quality and efficiancy in modeling.

 ## Research Question
- How different/similar will the feature selection between biological approach and Data Analysis methods be?
- Can we build a model to predict an interface amino acid in production by combining both methods?

## The Workflow
![image](https://github.com/user-attachments/assets/48547f9c-35d4-49ac-8c5e-2a4a2cae093b)

## Data
Data contains more than 65,000 protein sequence with 137 features, including the target variable which indicates the amino acid is interface or not. The features include information about each amino acid such as protein ID from Uniplot, protein length, PSSM matrix scores and hydropathy index.

## This project utilizes several R libraries to perform data preprocessing, analysis, and visualization:

- `dplyr`: Used for data manipulation and transformation.
- `faux`: Employed for generating simulated datasets (if applicable).
- `DataExplorer`: Utilized for automatic data exploration which speeds up the initial data understanding process.
- `caret`: Provides a suite of tools for creating predictive models and performing cross-validation.
- `randomForest`: Used to fit random forest models for classification or regression tasks.
- `ggplot2`: Applied for creating various aesthetic data visualizations.
- `corrplot`: Used for generating correlation matrices to identify relationships between variables.
- `MASS`: Employed for its statistical tools and data sets which are used in several data analysis techniques.


## Data Preprocessing
As suggested from the workflow, we applied undersampling (or downsampling) and oversampling to overcome the class imbalance. Several algorithm techniques have been proposed, there is no clear conclusion suggesting a single best algorithm.
For oversampling, two widely used methods were considered : Synthetic Minority Over-sampling Technique (SMOTE) and Random oversampling (ROS). With this dataset, ROS might result in an overfitting problem. On the other hand, SMOTE performs well in most of the cases. Undersampling was performed by decreasing the number of majority target instances or samples.

## Feature Selecion 
### Data Analytical Approach
1. Linear Discriminant Analysis (LDA)


## Conclusion


