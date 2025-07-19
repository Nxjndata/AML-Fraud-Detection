Anti-Money Laundering (AML) Fraud Detection
<img width="1440" height="900" alt="Screenshot 2025-07-18 at 4 06 29 PM" src="https://github.com/user-attachments/assets/18cb7e24-0425-42ec-8034-203967d497a0" />

 Project Summary

This project focuses on detecting fraudulent financial transactions to strengthen Anti-Money Laundering (AML) systems. Using supervised machine learning, it aims to minimize false positives (flagging legitimate transactions) and false negatives (missing actual laundering), both of which can cost financial institutions millions in losses, compliance fines, and customer trust.

Technical Approach

We implemented and compared classification models — Random Forest, AdaBoost, and XGBoost — trained on labeled transaction data. The models were evaluated with Stratified K-Fold cross-validation to balance bias and variance, and tuned using GridSearchCV and RandomizedSearchCV.

The final model was selected based on Recall (True Positive Rate) — a priority in AML since undetected fraudulent transactions are more costly than occasional false alarms.

Business Impact

Improved Detection Accuracy: By prioritizing recall, the solution identifies more illicit transactions, reducing regulatory risks.
Minimized Compliance Costs: Better model precision reduces false positives, cutting down on manual review time and operational costs.
Enhanced Trust & Transparency: A robust AML system signals compliance maturity to regulators and builds customer trust.
Reduced Financial Losses: Early fraud detection prevents misuse of funds and protects institutional assets.
Project Workflow

Problem Understanding
→ Address the high false positive and false negative rates in traditional AML systems.
Data Collection
→ Source: Kaggle – IBM AML Transaction Dataset
Data Validation
→ Checked for missing values, inconsistencies, and outliers.
Exploratory Data Analysis (EDA)
→ Uncovered patterns, correlations, and anomalies using statistical and visual analysis.
Preprocessing & Feature Engineering
Encoded categorical variables
Normalized numeric features
Removed multicollinearity using VIF and Chi-Squared tests
Modeling & Evaluation
Trained Random Forest, AdaBoost, and XGBoost
Applied StratifiedKFold CV for stability
Hyperparameter tuning via GridSearchCV & RandomizedSearchCV
Evaluated on accuracy, precision, recall, F1-score
Model Selection
→ Chose the model with the highest Recall to reduce false negatives
Web Interfaces (Local)
Streamlit for interactive UI and visualizations
FastAPI for real-time prediction APIs

Model Performance

The best-performing model, XGBoost, was selected based on its high recall. Below are the evaluation metrics:

Metric	Random Forest	  AdaBoost	 XGBoost (Best)
Accuracy	92.4%	          91.8%	    93.1%
Precision	88.5%         	87.1%	    89.7%
Recall	90.2%	            89.4%	    92.6%
F1-Score	89.3%	          88.2%	    91.1%
Why Recall?
In AML, catching fraudulent activity is more critical than occasionally flagging legitimate ones. Maximizing Recall helps minimize the number of laundering transactions that go undetected.


Tools & Technologies

Category	Stack
Programming	Python
Data Handling	Pandas, NumPy
Modeling	Scikit-learn, XGBoost, AdaBoost, Random Forest
Evaluation	GridSearchCV, Stratified K-Fold
Experiment Tracking	MLflow
Web Interface	Streamlit, FastAPI
Data Versioning	DVC
Database	MongoDB (Atlas)
Version Control	Git, GitHub

Outcome

Developed a high-recall AML fraud detection model capable of significantly reducing undetected laundering activities.
Improved the accuracy and interpretability of model predictions via robust feature engineering and validation.
Enabled reproducible and trackable experimentation using MLflow and DVC.
Empowered non-technical users to interact with the model through intuitive Streamlit and FastAPI interfaces.
