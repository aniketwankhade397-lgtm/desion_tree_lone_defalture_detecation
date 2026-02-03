💳 Credit Risk Prediction using Decision Tree 🌳
🔥 Project Overview

This project focuses on predicting loan default risk using a Decision Tree Classifier on real-world–style credit data.
The goal is not just high accuracy, but understanding risk, especially in an imbalanced dataset where most customers repay loans.

👉 This mirrors actual banking & finance problems, where default cases are rare but critical.


🧠 Problem Statement

Banks need to decide:

Whom to give a loan?

Who is likely to default?

The challenge:

~90% customers repay loans

Only ~10% default
➡️ This creates an imbalanced classification problem, where accuracy alone can be misleading.



📊 Dataset Highlights

Key features used:

person_income

loan_amnt

loan_int_rate

loan_percent_income

loan_grade

loan_intent

credit history length

past default indicator

Target variable:

loan_status

0 → Loan Repaid

1 → Loan Default


🛠️ Feature Engineering & Preprocessing

✔️ Missing values handled logically (grade-wise median for interest rate)
✔️ Outliers removed (very small noisy segments)
✔️ Smart binning:

Age groups

Credit history buckets
✔️ One-hot encoding for categorical variables
✔️ No unnecessary scaling (tree-based model)

🌳 Model Used

Decision Tree Classifier

Controlled depth to avoid overfitting

Focus on interpretability

Metrics evaluated beyond accuracy


📈 Model Performance
✅ Accuracy
Accuracy: ~0.89

📊 Confusion Matrix Insight

True Negatives (safe loans): very high ✅

False Negatives (missed defaulters): present ⚠️ (expected due to imbalance)
| Metric              | Value     | Insight                                          |
| ------------------- | --------- | ------------------------------------------------ |
| Precision (Default) | ~0.88     | When model flags default, it’s usually right     |
| Recall (Default)    | ~0.58     | Conservative model, misses some defaulters       |
| ROC AUC             | **~0.86** | Strong separation between risky & safe customers |

ROC AUC	~0.86	Strong separation between risky & safe customers

👉 ROC AUC is emphasized, as it is more reliable than accuracy for imbalanced data.
