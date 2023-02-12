# Phase_3_project Tanzania Water Wells

![insurance](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*Wme4Qf9vUx2ZEe6J7iKB6g.jpeg)

# Overview
The problem of providing clean water to the population of over 57,000,000 in Tanzania is a major concern, as many existing water points in the country are in need of repair or have failed altogether. To address this issue, a classifier will be built to predict the condition of a water well based on information such as the type of pump, date of installation and others. The target audience for this classifier could be an NGO focused on repairing wells or the Government of Tanzania looking to improve the construction of new wells.

# Business Understanding
The objective of building this classifier is to assist the NGO or the Government of Tanzania in their efforts to provide clean water to the population. By predicting the condition of a water well, the NGO can prioritize their resources and focus on the wells that are in need of repair, while the Government of Tanzania can use the insights to make informed decisions about the construction of new wells. The classifier will provide a reliable and efficient solution to the problem of ensuring clean water in Tanzania, which is essential for the health and well-being of its population.

# Data Understanding
The data used in this analysis was obtained from <a href="https://www.drivendata.org/competitions/7/pump-it-up-data-mining-the-water-table/page/25/">DrivenData</a> and was sourced from <a href="https://taarifa.org/">Taarifa</a> and the  <a href="https://www.maji.go.tz/">Tanzanian Ministry of Water</a> . It contains information on water wells in Tanzania and is divided into three files, including training set values, training set labels, and test set values. The training data has 59,400 observations and 41 variables, providing extensive information on various aspects of the water pumps:

# Modelling
- The goal of this project was to evaluate and compare the performance of three machine learning models on a binary classification problem with imbalanced data. The models used were a baseline Logistic Regression Model, a tuned Random Forest Model, and a tuned XGBoost Model.
- The data was preprocessed to handle the imbalance issue by using Synthetic Minority Over-sampling Technique (SMOTE). This method generated synthetic samples of the minority class to balance the distribution of the classes in the data.
### Baseline Logistic Regression Model
The baseline Logistic Regression Model was trained on the imbalanced data and achieved the following results:
- Precision: 0.71
- Recall: 0.68
- F1-Score: 0.70
- Accuracy: 0.71
These results indicate that the model was able to correctly identify 71% of the positive cases (precision) and retrieve 68% of all positive instances (recall). The F1-score of 0.70 gives a more comprehensive evaluation of the model's performance, and the accuracy of 0.71 shows that the model correctly predicted the outcomes of 71% of the data points.
### Tuned Random Forest Model
The Random Forest Model was trained on the balanced data and achieved the following results:

- Precision: 0.76
- Recall: 0.74
- F1-Score: 0.75
- Accuracy: 0.75
The model was trained with the following hyperparameters:

n_estimators: 100
max_depth: None
min_samples_split: 5
min_samples_leaf: 4
These results show that the Random Forest Model performed better than the Logistic Regression Model, achieving a higher precision, recall, F1-score, and accuracy.
### Tuned XGBoost Model
The XGBoost Model was trained on the balanced data and achieved the following results:
- Precision: 0.76
- Recall: 0.74
- F1-Score: 0.75
- Accuracy: 0.75
The model was trained with the following hyperparameters:

n_estimators: 100
max_depth: 3
learning_rate: 0.1
gamma: 0.0
subsample: 0.8
colsample_bytree: 0.8
reg_alpha: 0.05
These results show that the XGBoost Model performed similarly to the Random Forest Model, achieving a precision, recall, F1-score, and accuracy that was comparable to the Random Forest Model.
In conclusion, the tuned Random Forest Model and the tuned XGBoost Model both outperformed the baseline Logistic Regression Model, achieving higher precision, recall, F1-score, and accuracy. Both of these models performed similarly, and therefore, the choice of model will depend on specific project requirements and limitations.

# Evaluation
Based on the evaluation of the classification reports and scores for each model, it can be concluded that both XGBoost and Random Forest have comparable outcomes. The Random Forest Classifier has a slightly better performance in predicting the positive class (Repair), but XGBoost has a slightly higher overall accuracy. However, further investigation and fine-tuning of the models might be necessary to determine the best fit for the business requirements. Additionally, exploring other algorithms or models could potentially yield better results, considering the unique characteristics of the data and the business goals. After thorough evaluation, it has been determined that the Random Forest Classifier is the most suitable model for this dataset, due to its performance in predicting the positive class and faster processing time.

# Recommendations
- Cost analysis was not taken into consideration due to lack of cost data
- The focus of the study was on human wellbeing
- Cost data is essential for a more accurate cost-benefit analysis and should be collected in future studies
- Study was limited by the resources available and could have been more efficient with better resources
- The goal was to maximize the model's efficiency while considering human wellbeing
- Future studies should prioritize the collection of cost data, improve the efficiency of the study, and consider alternative models or algorithms for better performance
Given the unique characteristics of the dataset and business requirements, further investigation of alternative models may provide better results.
