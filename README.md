# Credit-Card-Fraud-Detection-Analysis--EDA

## Objective
This project aims to analyze a dataset containing credit card transactions, enabling us to identify and understand patterns indicative of fraudulent activity. The dataset comprises numerical features, primarily principal components obtained through PCA transformation, along with original features like 'Time' and 'Amount,' and a 'Class' variable indicating genuine or fraudulent transactions. We embarked on this Exploratory Data Analysis (EDA) to uncover critical insights into the nature of credit card fraud. Our objective was to assess how fraud rates vary across different transaction amounts, pinpointing the value ranges most susceptible to fraudulent activity. This understanding is crucial for developing robust fraud detection systems that can effectively minimize financial losses.

## Dataset Information
The dataset includes the following columns:

- Time: The elapsed time in seconds between each transaction and the first transaction in the dataset.
- V1-V28: These are anonymized principal components obtained from a PCA transformation, representing various transaction features.
- Amount: The transaction amount.
- Class: The target variable, indicating whether a transaction is fraudulent (1) or legitimate (0).

## Key questions
1. What is the proportion of fraud vs. non-fraud transactions?
2. How do transaction amounts differ between fraud and non-fraud cases?
3. When does fraud typically occur during the day?
4. What’s the correlation between features and fraud?
5. What are the top 10 highest fraud transactions by amount?¶
6. Is there a trend in fraud over time (line plot)?
7. Does the amount of fraudulent transactions differ significantly from non-fraudulent ones?

## Key insights
- Severe Class Imbalance: Fraudulent transactions are extremely rare, accounting for approximately 0.17% of the dataset, making fraud detection a rare-event problem.

- PCA Transformed Features (V1-V28): These features show distinct patterns for fraudulent transactions, indicating their importance in distinguishing fraud from legitimate transactions.

- Time Feature Distribution: Transaction times are uniformly distributed across both fraud and non-fraud cases, suggesting that the time of day alone might not be a strong indicator of fraud.

- Transaction Amount Distribution: Fraudulent transactions generally involve smaller amounts, while non-fraudulent transactions cover a wide range of amounts.

- Fraud Rate by Transaction Amount: Fraud rates are higher for very low-value transactions (e.g., < $25), potentially indicating automated or bot-driven fraud attempts.

##  Recommendations
- Handle Data Imbalance: Address the dataset's severe class imbalance using techniques like oversampling/undersampling and stratified cross-validation for fair model training and evaluation.
- Enhance Features: Create new, informative features from existing data (e.g., 'Time', 'Amount') to better capture complex fraud patterns.
- Select Suitable Models & Metrics: Employ anomaly detection algorithms and focus on performance metrics such as Precision, Recall, and F1-score, which are crucial for imbalanced fraud datasets.
- Implement Real-time Monitoring: Develop a system to monitor transactions in real-time for immediate detection and flagging of suspicious activities.

## Conclusion
The credit card transaction dataset is highly imbalanced, with a minuscule percentage of fraudulent activities. PCA-transformed features are crucial for distinguishing between fraudulent and legitimate transactions, which typically involve smaller amounts and exhibit distinct patterns. Effective fraud detection requires specialized modeling techniques and careful evaluation metrics due to this inherent data imbalance. Therefore, future efforts should prioritize robust modeling strategies and real-time anomaly detection to minimize financial losses from fraud.
