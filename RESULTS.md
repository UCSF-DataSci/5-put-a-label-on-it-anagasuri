# Assignment 5: Health Data Classification Results

This file contains your manual interpretations and analysis of the model results from the different parts of the assignment.

## Part 1: Logistic Regression on Imbalanced Data

### Interpretation of Results

In this section, provide your interpretation of the Logistic Regression model's performance on the imbalanced dataset. Consider:

- Which metric performed best and why?
The accuracy at 0.9168 appears the be the strong metric. This could have been due to the class imbalance though. The model predicted the majority class the best but not the other classes so well. 

- Which metric performed worst and why?
The worst metric would be recall at 0.3007. This indicates that the model misclassifed a large number of true positive disease cases when the postive class was underepresented. 

- How much did the class imbalance affect the results?
The imbalance impact score of 0.50 indicates taht the metric like F1 and recall are significantly depressed compared to accuracy. 

- What does the confusion matrix tell you about the model's predictions?
The high tru enegatives and low true positives suggest that the model is over learning the majority class and not learning the minority classes enough. 



## Part 2: Tree-Based Models with Time Series Features

### Comparison of Random Forest and XGBoost

In this section, compare the performance of the Random Forest and XGBoost models:

- Which model performed better according to AUC score?
The xgboost model did slighlty better than the random forest model with AUC scores of 0.9977 and 0.9794 respectively. 

- Why might one model outperform the other on this dataset?
The xgboost reduces bias and variance better than the random forest. This is helpful in healthcare data becuase it is able to capture more complex and non linear patterns. 

- How did the addition of time-series features (rolling mean and standard deviation) affect model performance?
Including rolling means and standard deviations probably helped the model perfomr better oby providing context over time. 



## Part 3: Logistic Regression with Balanced Data

### Improvement Analysis

In this section, analyze the improvements gained by addressing class imbalance:

- Which metrics showed the most significant improvement?
The est improved metric was recall which increased from 0.3007 to 
0.8531. 

- Which metrics showed the least improvement?
The least improved measure is precision which reduced from 0.6615 to 0.3995 due to more positive predictions. 

- Why might some metrics improve more than others?
Recall and F1 improved more than others because they were focused on the minority classes of the dataset. Balancing helped the model better detect positive outcomes. 

- What does this tell you about the importance of addressing class imbalance?
SMOTE allows us to address class imbalances. This improves the fairness and clinical relevance which allows the model to correctly predict disease outcomes. This is especially relevant in healthcare. 



## Overall Conclusions

Summarize your key findings from all three parts of the assignment:

- What were the most important factors affecting model performance?
The key factors whic impaated performance was class imbalances, time dependant features, and model choices. And data preparation as well. 

- Which techniques provided the most significant improvements?
Using SMOTE to deal with class imbalance was a huge reason for better model performance. The time series feature was also important because dynamic data is always better than static. And using xgboost over a simpler model like logistic regression was important to look at complex trends in the data. 

- What would you recommend for future modeling of this dataset?
For the future, we need to look at class imbalance more closely and possibly collect data that captures patient changes over time better. And when dealing with noisy and nonlinear datasets, use slighlty more complex models like xgboost which can handle more nuances in data. 

