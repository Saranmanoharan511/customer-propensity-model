📌 Customer Propensity to Purchase Model

This project builds a machine learning model to predict whether a customer is likely to make a purchase, using customer-level behavioral features derived from transaction data.
----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
🔄 Data Transformation

Started with transaction-level data and transformed it into a customer-level dataset.

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

Features engineered:

🔹 Recency – Time since last purchase
🔹 Frequency – Number of transactions
🔹 Monetary – Total spend
🔹 Avg Order Value – Average value per transaction
🔹 Avg Purchase Interval – Average time gap between purchases

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

🚨 Key Insight

The initial model achieved 100% accuracy, which indicated a potential issue rather than success.

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

Investigation steps:

🔍 Checked for data leakage → ❌ None found
📊 Analyzed feature importance → ✅ Recency = 1.0
📈 Explored data distribution → ✅ Perfect class separation

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
Findings:

📉 Customers with low Recency → Always purchased
📈 Customers with high Recency → Never purchased

The model was not learning patterns — it was capturing a deterministic rule.

Root Cause:

⚠️ Feature engineering unintentionally created a feature (Recency) that perfectly separated the target variable.

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

📊 Tech Stack

🐍 Python
🐼 Pandas
🧠 Scikit-learn
⚡ XGBoost
📉 Matplotlib

📁 Project Structure

📂 notebook.ipynb → End-to-end workflow including data loading, feature engineering, EDA, and model training
