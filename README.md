# Data-Science-Project
Heart Disease Prediction Project 

1. Introduction 

Heart disease remains one of the leading causes of mortality worldwide, and early prediction of heart disease risk can significantly aid in timely medical intervention. This project leverages machine learning to develop a model that accurately classifies individuals as having a high or low risk of heart disease based on select health indicators. The project also examines which health features are most influential in predicting heart disease, offering valuable insights for preventive health measures. 

2. Dataset 

The dataset used in this project consists of health indicators related to heart disease, with the primary goal of predicting the binary target variable: 

HeartDiseaseorAttack: A binary variable where 1 indicates the presence of heart disease or a heart attack, and 0 indicates absence. 

Key features considered in the model include: 

HighBP: Indicator of high blood pressure 

HighChol: Indicator of high cholesterol levels 

BMI: Body Mass Index, a measure of body fat based on height and weight 

These features were selected based on their relevance in medical literature as indicators or contributors to cardiovascular health. 

3. Methodology 

3.1 Data Preprocessing 

The data preprocessing steps included: 

Handling Class Imbalance: The dataset had a significant class imbalance, with the majority of samples indicating no heart disease. To address this, we used Synthetic Minority Over-sampling Technique (SMOTE) to balance the dataset. 

Train-Test Split: The dataset was split into a training set and a test set to evaluate model performance on unseen data. 

3.2 Model Training and Evaluation 

We trained and evaluated three machine learning models: 

Logistic Regression 

Decision Tree Classifier 

Random Forest Classifier 

Each model was initially evaluated on accuracy, precision, recall, and F1-score. Decision Tree emerged as the best-performing model after hyperparameter tuning, which was conducted using GridSearchCV to identify the optimal parameters (criterion, max_depth, min_samples_leaf, min_samples_split). 

3.3 Hyperparameter Tuning 

The hyperparameters for the Decision Tree model were tuned, with the following best parameters: 

Criterion: gini 

Max Depth: 10 

Min Samples Leaf: 1 

Min Samples Split: 2 

These optimized hyperparameters improved the model’s balance between precision and recall, particularly enhancing its ability to detect cases of heart disease (recall). 

4. Results 

4.1 Model Performance on Test Data 

The final, tuned Decision Tree model produced the following results on the test set: 

Accuracy: 65% 

Precision: 17% 

Recall: 71% 

F1 Score: 28% 

Classification Report: 

Class 

Precision 

Recall 

F1-Score 

Support 

No Heart Disease (0) 

96% 

65% 

77% 

45,968 

Heart Disease (1) 

17% 

71% 

28% 

4,768 

 

Accuracy: 65% - Overall, the model correctly predicted 65% of the cases. 

Precision: 17% - Precision for detecting heart disease cases was low, indicating a high rate of false positives. 

Recall: 71% - Recall for heart disease was relatively high, meaning the model correctly identified a large portion of actual heart disease cases. 

F1 Score: 28% - The F1 score balances precision and recall for the positive class (heart disease), which was limited by low precision. 

4.2 Feature Importance 

The following are the feature importances derived from the Decision Tree model, indicating the relative influence of each feature on heart disease prediction: 

Feature 

Importance 

HighBP 

74.6% 

HighChol 

22.2% 

BMI 

3.1% 

Interpretation 

HighBP (High Blood Pressure) was the most influential feature, with an importance of 74.6%, highlighting it as a significant predictor of heart disease in this dataset. 

HighChol (High Cholesterol) followed with an importance of 22.2%, also showing a strong correlation with heart disease. 

BMI had minimal influence at 3.1%, suggesting it played a limited role in heart disease predictions within this dataset. 

5. Discussion 

The Decision Tree model's performance demonstrates the complexity of predicting heart disease based on these indicators. Although the model achieved a reasonably high recall for detecting heart disease cases (71%), precision was low (17%), which may limit its practical application due to the high rate of false positives. 

The feature importance analysis indicates that high blood pressure and high cholesterol are critical factors for heart disease risk, consistent with medical research. However, the model's low precision suggests that additional features or advanced methods may be necessary to improve prediction accuracy and reliability. 

6. Conclusion 

This project illustrates the potential and challenges of using machine learning for heart disease prediction. While the Decision Tree model with tuned hyperparameters performed best in recall, the overall precision was low. Future work could explore additional data preprocessing, incorporate more health indicators, or apply ensemble methods to enhance predictive performance. 

7. Future Work 

To improve the model's predictive performance, potential future steps include: 

Incorporating additional health features: Such as lifestyle factors, diet, or genetic markers, for a more comprehensive predictive model. 

Experimenting with ensemble models: Combining models like Gradient Boosting or AdaBoost, which may capture complex patterns and enhance accuracy. 

Using advanced feature engineering: Testing different transformations or derived features could reveal additional insights from the existing dataset. 

 
