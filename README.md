# Transaction Behavior and Fraud Analysis Using Machine Learning

This repository contains an end-to-end analysis of transactional behavior and potential fraud detection using **Python** and **machine learning**.  
The project explores transaction data to uncover relationships between user activity, payment behavior, and system reliability through **statistical visualization** and **feature importance** analysis.

---

##  Key Explorations

###  Descriptive Analysis
- Used histograms to explore numeric distributions (`No_Transactions`, `No_Orders`, `No_Payments`) to understand customer activity and transaction frequency.

### Categorical Insights
- Bar charts were created for categorical variables such as:
  - `paymentMethodType`
  - `paymentMethodProvider`
  - `paymentMethodRegistrationFailure`
  - `transactionFailed`
  - `orderState`
  
  These visualizations helped identify user preferences, system reliability, and the most common payment methods.

###  Correlation Analysis
- A correlation matrix was used to examine linear relationships between numeric variables.  
  - Found a **strong positive correlation** between `No_Transactions` and `No_Orders` (0.91).  
  - Identified a **moderate relationship** between `transactionAmount` and `Fraud` (0.28).  
  - Other variables showed weak or negligible correlations, indicating independent behaviors.

###  Feature Importance (Machine Learning)
- Using a **tree-based model** (e.g., Random Forest or XGBoost), feature importance was computed to understand which factors most influence predictions.
- The top contributing features were:

| Rank | Feature | Importance | Interpretation |
|------|----------|-------------|----------------|
| 1 | `customerIPAddress_freq_encoded` | 0.1465 | IP frequency is the strongest indicator of suspicious activity — repeated IPs may signal abnormal patterns. |
| 2 | `customerDevice_freq_encoded` | 0.0889 | Device frequency suggests multiple accounts using the same device or shared usage patterns. |
| 3 | `No_Payments` | 0.0783 | The number of payments indicates user consistency and transactional engagement. |
| 4 | `transactionAmount` | 0.0735 | Larger transactions carry slightly higher fraud risk. |
| 5| `customerEmail_freq_encoded` | 0.0731 | Repeated email usage might point to duplicate or fraudulent accounts. |

---

##  Tech Stack
- **Language:** Python  
- **Libraries:** pandas, seaborn, matplotlib, scikit-learn  
- **Modeling:** Random Forest / XGBoost (for feature importance extraction)  
- **Visualization:** Correlation heatmaps, categorical bar plots, and numeric histograms  

---

##  Key Findings
- 90% of users successfully registered payment methods.  
- 84% of orders were fulfilled successfully, while 10% failed.  
- Card payments dominate at 79%, followed by minor adoption of Bitcoin, Apple Pay, and PayPal.  
- 25% of transactions failed — further investigation needed into causes (e.g., provider issues or user-side problems).  
- Fraud risk increases slightly with higher transaction amounts.  
- Behavioral features (IP, Device, Email frequency) are stronger predictors than transactional value alone.
