# Metaverse Financial Analysis Project
**Zhouling Shen**

## Executive Summary

In this project, I leverage an extensive dataset from the Open Metaverse, an expansive digital realm where blockchain technology is crucial for ensuring secure and transparent transactions. My focus is on detecting anomalies and assessing risks within 78,600 blockchain financial transactions. By applying advanced machine learning techniques, including Linear Regression, Regularizations, Decision Trees, Random Forest, and Neural Network, I aim to enhance the detection of fraudulent activities and identify characteristics of transactions that indicate risk. This effort is pivotal for maintaining the integrity of virtual economies.
https://www.kaggle.com/datasets/faizaniftikharjanjua/metaverse-financial-transactions-dataset

## Background

The Open Metaverse is a burgeoning virtual world that closely mimics real-life economies. It's a place where all manner of buying and selling occurs, just like in the real world, but with digital items. From individual users to large companies, participation spans a broad spectrum. The competition among various virtual worlds to attract more users is fierce, with a strong emphasis on ensuring all transactions are safe and reliable.

Blockchain technology plays a critical role in this economy, providing the security and trust necessary for smooth operations and user confidence. In such a competitive environment, creativity and the ability to detect patterns of risky transactions are crucial for a platform's success and distinctiveness in the digital market.

## Discussion

Traditionally, digital asset management firms rely on rule-based systems to flag fraudulent transactions, which often result in a high rate of false positives, leading to customer dissatisfaction and operational inefficiencies. My strategy diverges from conventional systems by employing machine learning models capable of learning from data to identify subtle and complex patterns indicative of fraud. This approach aligns with my objectives by reducing false positives, increasing the detection rate of actual fraud, automating parts of the risk assessment process, and providing scalable solutions that can evolve with the metaverse's growth.

## Exploratory Data Analysis (EDA)

My initial exploratory data analysis uncovered intriguing insights. The count distribution of transaction types across regions showed that standard transactions like "transfer," "purchase," and "sale" are far more common than negative ones such as "scam" and "phishing," regardless of location. This trend underscores the predominance of legitimate transactions in the global economic landscape. Additionally, my examination of user engagement metrics revealed peak times at 10 am and 3 pm for both login frequency and session duration, with a notable pattern in the late evening where longer sessions occur despite fewer logins. This may indicate a subset of users engaging more deeply with the platform at night. The risk analysis associated with transaction anomalies showed a clear stratification of risk scores, further laying a strong foundation for in-depth investigation into the mechanisms driving these behaviors and risks within the transactional ecosystem.

## Data Preprocessing

In the data preprocessing stage, I employed one-hot encoding on multiple categorical columns to enhance interpretability. For "sending_address" and "receiving_address" columns, label encoding was chosen to prevent an unwieldy increase in variable numbers. I also dropped the "timestamp" variable as the presence of "hour_of_day" already captures the timing aspect of the data. The central objective here is to identify factors influencing the "risk_score," which measures the risk level of each transaction by assessing the attributes of the transactions and patterns of user activity.

## Model Comparisons

I evaluated the performance of several predictive models, including OLS, LASSO, Ridge, Elastic Net, and more advanced models like Neural Network, Bootstrapped Random Forest, and Decision Tree. The latter models showed particularly outstanding performance, indicating excellent fit to the test data and providing significant insights for the project.

## Recommendations & Business Value

From the insights gained, particularly through the bootstrapped random forest and decision trees models, I suggest a focus on behavioral analytics and transactional monitoring, and the establishment of a real-time alert system. These recommendations aim to intensify fraud detection mechanisms, minimize financial losses, and maintain user trust in the digital economy of the Metaverse.

## Summary

My analysis within the Open Metaverse identified prevalent legitimate transactions and critical engagement periods, employing machine learning to anticipate transaction risks effectively. The standout performance of advanced models in predicting risk leads to a comprehensive strategy for enhancing fraud detection, offering valuable contributions to the security and trust in digital economies.
