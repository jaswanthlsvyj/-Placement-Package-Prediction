
# Placement Package Prediction

This project aims to predict the placement package of students using a dataset with 220,000 rows and 18 features. The goal is to explore various factors influencing job offers and determine the best model for accurate predictions.

## 1. Dataset Overview

**Number of Rows:** 220,000  
**Number of Columns:** 19

### Columns:

1. **Name of Student:** The name of the student. *(Data Type: String)*
2. **Roll No.:** Roll number of the student. *(Data Type: Integer)*
3. **No. of DSA questions:** Number of Data Structures and Algorithms (DSA) questions attempted by the student. *(Data Type: Integer)*
4. **CGPA:** Cumulative Grade Point Average (CGPA) of the student. *(Data Type: Float)*
5. **Knows ML:** Whether the student knows Machine Learning (ML) or not. *(Data Type: String, Yes/No)*
6. **Knows DSA:** Whether the student knows DSA or not. *(Data Type: String, Yes/No)*
7. **Knows Python:** Whether the student knows Python programming language or not. *(Data Type: String, Yes/No)*
8. **Knows JavaScript:** Whether the student knows JavaScript programming language or not. *(Data Type: String, Yes/No)*
9. **Knows HTML:** Whether the student knows HTML or not. *(Data Type: String, Yes/No)*
10. **Knows CSS:** Whether the student knows CSS or not. *(Data Type: String, Yes/No)*
11. **Knows Cricket:** Whether the student knows how to play cricket or not. *(Data Type: String, Yes/No)*
12. **Knows Dance:** Whether the student knows how to dance or not. *(Data Type: String, Yes/No)*
13. **Participated in College Fest:** Whether the student participated in the college fest or not. *(Data Type: String, Yes/No)*
14. **Was in Coding Club:** Whether the student was a member of the coding club or not. *(Data Type: String, Yes/No)*
15. **No. of backlogs:** Number of backlogs the student has. *(Data Type: Integer)*
16. **Interview Room Temperature:** Temperature of the interview room in degree Celsius. *(Data Type: Float)*
17. **Age of Candidate:** Age of the student. *(Data Type: Integer)*
18. **Branch of Engineering:** The branch of engineering the student belongs to. *(Data Type: String)*
19. **Placement Package:** The package offered to the student during placement, in lakhs per annum. *(Data Type: Float)*

## 2. Dataset Dictionary

The dataset includes a variety of features such as academic performance, technical skills, participation in extracurricular activities, and demographic information. The target variable is the **Placement Package**, which represents the salary offered to the student.

## 3. Basic Statistics and Model Selection

Initial analysis of the dataset includes calculating summary statistics such as mean, median, standard deviation, and distribution of each feature. This helps in understanding the nature of the data and identifying any potential issues such as skewness or outliers.

Based on the nature of the problem—predicting a continuous value (Placement Package)—a regression model is suitable. Support Vector Machines (SVMs) and Tree-based models have been selected due to their ability to capture complex relationships between features.

## 4. Feature Selection and Target Variable

The target variable for this project is the **Placement Package**. Features such as **CGPA, No. of DSA questions, Knows ML, Knows Python,** and **Branch of Engineering** are considered crucial for predicting the placement package, as they directly relate to a student’s technical proficiency and academic background.

Proofs for selecting these features include correlation analysis, feature importance scores, and domain knowledge.

## 5. Data Cleaning, Outlier Removal, and Feature Engineering

### Steps Involved:

1. **Data Cleaning:** Handling missing values and ensuring data consistency.
2. **Outlier Removal:** Identifying and removing outliers that could skew the results.
3. **Imputation:** Filling missing values using appropriate techniques (mean, median, mode, etc.).
4. **Feature Engineering:** Creating new features or modifying existing ones to improve model performance. This may include encoding categorical variables, scaling numerical features, and creating interaction terms.

## 6. Base Models and Hyperparameter Description

Two base models have been created:

1. **Support Vector Machines (SVM):** 
   - **Hyperparameters:** Kernel, C (Regularization parameter), Gamma.
   
2. **Tree Models:**
   - **Hyperparameters:** Max Depth, Min Samples Split, Min Samples Leaf.

These hyperparameters were initially set to default values, and the models were trained on the dataset.

## 7. Base Model Predictions and Metrics

The base models were evaluated using metrics such as Mean Absolute Error (MAE), Mean Squared Error (MSE), and R-squared (R²). Visualizations include:

- **Predicted vs Actual:** To observe the model's accuracy.
- **Error Distribution:** To identify any bias in the model’s predictions.

## 8. Hyperparameter Tuning and Estimators

To enhance model performance, hyperparameter tuning was conducted using techniques such as Grid Search and Random Search. The best estimators for each model were identified based on cross-validation results.

## 9. Testing and Selecting the Best Estimators

The tuned models were tested on a validation set to ensure their performance generalizes well to unseen data. The best-performing model was selected based on a combination of metrics and visual inspection.

## 10. Comparing Base and Tuned Models

After tuning, the performance of the models improved significantly. The tuned model demonstrated lower error metrics and a better fit to the data, as shown in the comparison visualizations.

## 11. Visualization and Conclusion

Visual comparisons between the base and tuned models highlight the improvements achieved through hyperparameter tuning. The final model, which uses the optimal hyperparameters, provides a more accurate prediction of placement packages, thus meeting the project's objectives.
