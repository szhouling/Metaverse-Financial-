# Metaverse Financial Blockchain Analysis - Fraud Detection
**Zhouling Shen**

## Executive Summary

In this project, I leverage an extensive dataset from the Open Metaverse, an expansive digital realm where blockchain technology is crucial for ensuring secure and transparent transactions. My focus is on detecting anomalies and assessing risks within 78,600 blockchain financial transactions. By applying advanced machine learning techniques, including Linear Regression, Regularizations, Decision Trees, Random Forest, and Neural Network, I aim to enhance the detection of fraudulent activities and identify characteristics of transactions that indicate risk. This effort is pivotal for maintaining the integrity of virtual economies.
https://www.kaggle.com/datasets/faizaniftikharjanjua/metaverse-financial-transactions-dataset

## Background

The Open Metaverse is a burgeoning virtual world that closely mimics real-life economies. It's a place where all manner of buying and selling occurs, just like in the real world, but with digital items. From individual users to large companies, participation spans a broad spectrum. The competition among various virtual worlds to attract more users is fierce, with a strong emphasis on ensuring all transactions are safe and reliable.

Blockchain technology plays a critical role in this economy, providing the security and trust necessary for smooth operations and user confidence. In such a competitive environment, creativity and the ability to detect patterns of risky transactions are crucial for a platform's success and distinctiveness in the digital market.

## Discussion

Traditionally, firms in the digital asset management space rely on rule-based systems to flag fraudulent transactions. These systems often involve setting thresholds for transaction amounts or frequencies that, when exceeded, trigger a review. However, such approaches lack the nuance to detect sophisticated fraud patterns and can result in a high rate of false positives, leading to customer dissatisfaction and operational inefficiencies.
my specific strategy diverges from conventional rule-based systems by employing machine learning models that can learn from data to identify subtle and complex patterns indicative of fraud. This aligns with the business model by:
- Reducing the incidence of false positives, thus improving customer experience.
- Increasing the detection rate of actual fraud, thereby enhancing security.
- Automating part of the risk assessment process, leading to operational cost savings.
- Providing scalable solutions that can evolve with the metaverse's growth.
By aligning my analytical approach with the business objectives of security, user satisfaction, and operational efficiency, I ensured that my solution directly contributes to the firm's competitive advantage in the growing industry of virtual economies.


## Exploratory Data Analysis (EDA)

Initially, I've uncovered intriguing insights through exploratory data analysis. The count distribution of transaction types across regions showed that standard transactions like "transfer," "purchase," and "sale" are far more common than negative ones such as "scam" and "phishing," regardless of location. This trend holds universally, underscoring the predominance of legitimate transactions in the global economic landscape. Furthermore, my examination of user engagement metrics highlighted two peak times at 10 am and 3 pm for both login frequency and session duration, with an intriguing pattern in the late evening where longer sessions occur despite fewer logins. This may indicate a subset of users engaging more deeply with the platform at night. My risk analysis associated with transaction anomalies showed a stark contrast between high and low-risk scores, averaging around 97 and 36 respectively, painting a clear picture of risk stratification. Finally, despite their lower frequency, "phishing" and "scam" transactions tend to carry significantly higher risk scores compared to other transaction types. These patterns, consistent across different analyses, lay a strong foundation for further investigation into the mechanisms driving these behaviors and risks within the transactional ecosystem of my study.


## Data Preprocessing

In the data preprocessing stage, I employed one-hot encoding on multiple categorical columns to enhance interpretability. For "sending_address" and "receiving_address" columns, label encoding was chosen to prevent an unwieldy increase in variable numbers. I also dropped the "timestamp" variable as the presence of "hour_of_day" already captures the timing aspect of the data. The central objective here is to identify factors influencing the "risk_score," which measures the risk level of each transaction by assessing the attributes of the transactions and patterns of user activity.

## Model Comparisons

In the model comparison section of my project report, I evaluated the performance of seven different predictive models. The Ordinary Least Squares (OLS), LASSO, Ridge, and Elastic Net models demonstrated similar performance metrics, with Mean Absolute Error (MAE) around 2.91, Mean Squared Error (MSE) around 14.11, Root Mean Squared Error (RMSE) around 3.75, and R-squared values approximately 0.97. This suggests that they were quite consistent with one another in terms of accuracy and explained variance. The Neural Network model showed moderate error metrics with an MAE of 0.223509, MSE of 0.193810, RMSE of 0.440239, and an R-squared of 0.999591. 

In sharp contrast, the Bootstrapped Random Forest and Decision Tree models exhibited outstanding performance with significantly lower MAE (0.00193 and 0.000581 respectively), MSE (0.005222 and 0.002239 respectively), and RMSE (0.072264 and 0.047316 respectively), alongside almost perfect R-squared values (close to 1.0), indicating an excellent fit to the test data. The significant features identified by these two models will serve as the insights and conclusions I draw in my project. 


## Recommendations & Business Value

From bootstrapped random forest and decision trees models, I found these variables are important in both: purchase_pattern_focused, hour_of_day, transaction_type_purchase, transaction_type_sale. With these insights, here’s what I suggests: 
- Behavioral Analytics: Intensify the behavioral analysis based on 'purchase_pattern_focused' and 'hour_of_day' to detect deviations that could signify fraudulent activity. Patterns in purchase behavior and transaction timings are rich indicators that can be monitored in real-time for preemptive fraud detection.
- Transactional Monitoring: Develop a sophisticated monitoring system that differentiates between 'transaction_type_purchase' and 'transaction_type_sale', deploying appropriate fraud detection mechanisms for each category due to their distinct risk profiles.
- Real-Time Alert Systems: Establish a real-time alert system leveraging the identified features to rapidly respond to potential fraud, minimizing financial losses and maintaining user trust.

## Summary

My analysis within the Open Metaverse identified prevalent legitimate transactions and critical engagement periods, employing machine learning to anticipate transaction risks. The standout performance of Bootstrapped Random Forest and Decision Tree models in predicting risk leads to my strategy for fraud detection. These insights include enhanced behavioral analytics, tailored monitoring of transaction types, and the implementation of an alert system, positioning us to protect the security and trust in the digital economy of the Metaverse.
