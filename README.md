# E-Commerce-Fraud-Analysis
Transaction Behavior and Fraud Analysis Using Machine Learning

This repository contains an end-to-end analysis of transactional behavior and potential fraud detection using Python and machine learning.
The project explores transaction data to uncover relationships between user activity, payment behavior, and system reliability through statistical visualization and feature importance analysis.

🔍 Key Explorations
	•	Descriptive Analysis:
Histograms were used to explore numeric distributions (No_Transactions, No_Orders, No_Payments) to understand user activity and payment frequency.
	•	Categorical Insights:
Bar charts were created for variables such as paymentMethodType, paymentMethodProvider, paymentMethodRegistrationFailure, transactionFailed, and orderState to visualize system performance and user preferences.
	•	Correlation Analysis:
A correlation matrix identified relationships between key numeric features, showing strong correlation between No_Transactions and No_Orders, and moderate linkages between transaction amount and fraud likelihood.
	•	Feature Importance (Machine Learning Model):
Using tree-based models, feature importance revealed that behavioral indicators such as customerIPAddress_freq_encoded, customerDevice_freq_encoded, and customerEmail_freq_encoded play dominant roles in detecting anomalies, surpassing even monetary variables like transactionAmount.

Tech Stack
	•	Python: pandas, seaborn, matplotlib, scikit-learn
	•	Machine Learning: Tree-based models (e.g., Random Forest Classification) for feature importance extraction
	•	Visualization: Correlation heatmaps, categorical bar plots, and distribution histograms

Key Findings
	•	Most users successfully register payment methods (90%) and complete orders (84%).
	•	Transactions are predominantly card-based (79%), with minor adoption of Bitcoin, PayPal, and Apple Pay.
	•	Around 25% of transactions fail, requiring further diagnostic analysis.
	•	Fraud likelihood slightly increases with higher transaction amounts.
	•	IP, device, and email frequency are critical behavioral signals for detecting suspicious patterns.
