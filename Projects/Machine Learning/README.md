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

### This project utilizes several R libraries to perform data preprocessing, analysis, and visualization:

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
1. Linear Discriminant Analysis (LDA) : a supervised learning method to find a linear combination of features that best separates two or more classes of objects. As features with high absolute coefficients in the
 linear combination by the trained model are more important in separating the classes, important features can be selected based on their coefficients. The features with top 25% absolute coefficient values were selected.
2. LASSO :  a classification algorithm which uses the L1 regularization to constrain the sum of absolute model parameter values to be less than an upper bound. It penalizes regression variable coefficients,
 shrinking some to zero, and selects only those with non-zero coefficients during the feature selection process. The coefficients of features are sorted in descending order and we chose 35 features to make the number of features comparable with biological approach and other models.
3. Elastic Net : a regularized regression method which overcomes the limitations of LASSO combining LASSO and ridge regression methods linearly. The elastic net method introduces a hyperparameter that controls the balance between the L1 and L2 regularization terms, allowing the model to be tuned to the specific dataset. Same approach to choose the lambda and the number of features were applied as the LASSO method.
4. Correlation : Correlation describes how close two variables are linearly related with each other. Highly correlated features are linearly dependent and would have the same effect on the target variable. The features were converted to a correlation matrix and the pairwise correlation between all features was calculated. For a correlation cutoff value, 0.75 was employed because it is generally considered a strong correlation. Highly correlated features with greater than 0.75 were removed.
5. Combining methods : To yield a more powerful feature list, we combined three individual methods, LDA, LASSO, and Elastic net. By combining different methods, we might take advantage of the strengths of each method while
 mitigating their weaknesses. Based on the AUC scores of each method, the weights were multiplied to the coefficients of each method and summed. The weights were applied differently based on each AUC score depending on resampling methods (Table ?.). For the undersampling dataset, the weights were 0.3, 0.35, and 0.35 for LDA, LASSO, Elastic net respectively. For an oversampling dataset, the weights were equally set, 0.33.

## Models
Six models (3 baseline models and 3 advanced models) are chosen for this project as they are all famous for performing classification tasks. The baseline models are logistic regression, KNN, and decision tree, while random forest serves as one of the advanced models and is expected to give the best accuracy. As the state-of-art models, we attempted to build two deep learning models, multilayer perceptron and transformer. Due to the lack of computational resources, we applied only combined features to those models, which is considered to reflect reasonable selection from overall feature selection methods.

## Results

## Conclusion


