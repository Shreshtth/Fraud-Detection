# FRAUD DETECTION
Dataset used : https://www.kaggle.com/datasets/nelgiriyewithana/credit-card-fraud-detection-dataset-2023
<br>
Libraries : numpy, **pandas**, os, time (optional), matplotlib, seaborn, **sklearn**, **xgboost**, warnings (optional)
<br>
## Summary - Project Building
I invested my time into learning all the machine/deep learning techniques related to fraud detection and carried out all the techniques I knew. My efforts were worth it after i saw the higgest accuracy 
of **99.94 %**.
<br>
### About Dataset -
This dataset contains credit card transactions made by European cardholders in the year 2023. It comprises over 550,000 records, and the data has been anonymized to protect the cardholders' identities. 
The primary objective of this dataset is to facilitate the development of fraud detection algorithms and models to identify potentially fraudulent transactions. Dataset is completely balanced.
<br>
Key Features:
- id: Unique identifier for each transaction
- V1-V28: Anonymized features representing various transaction attributes (e.g., time, location, etc.)
- Amount: The transaction amount
- Class: Binary label indicating whether the transaction is fraudulent (1) or not (0)

### Data Preprocessing and Preparation -

Distribution of "Fraud" class :

![image](https://github.com/Shreshtth/Fraud-Detection/assets/98511654/f0786af6-7460-4d0f-a9e7-057ba7ef1b9b)

Heatmap of parameter correlation:

![image](https://github.com/Shreshtth/Fraud-Detection/assets/98511654/b97f5b98-acb9-43f7-8883-e8fcff0a40d3)

Performed PCA and Feature Scaling, and choose a 85-25 Train-Test datasplit.

### Model and Evaluation -

1. Logistic Regression: Logistic regression is a supervised machine learning algorithm used for classification tasks. It estimates the probability of an event occurring based on a given data set of independent variables.

![image](https://github.com/Shreshtth/Fraud-Detection/assets/98511654/9c89de5f-0fd4-418a-a334-1f799da88f06)


2. Gaussian Naive Bayes: The Gaussian Naive Bayes classifier is a supervised machine learning algorithm used for classification tasks. It assumes that the features follow a normal (Gaussian) distribution and are independent of each other. This allows for efficient calculation of probabilities and makes it suitable for problems with continuous features.

![image](https://github.com/Shreshtth/Fraud-Detection/assets/98511654/3d7dc83d-bde0-4c4a-80c4-4257ebc36be5)


3. Decision Tree: A decision tree is a decision support hierarchical model that uses a tree-like model of decisions and their possible consequences, including chance event outcomes, resource costs, and utility.

![image](https://github.com/Shreshtth/Fraud-Detection/assets/98511654/17d9f921-0b2c-4144-a419-8b0e0ad19aef)


4. Random Forest: Random forest is a supervised machine learning algorithm that combines multiple decision trees to improve prediction accuracy and prevent overfitting

![image](https://github.com/Shreshtth/Fraud-Detection/assets/98511654/02b9f976-407f-486a-ba37-45129038c597)


5. XGBoost: XGBoost is a machine learning algorithm that belongs to the ensemble learning category, specifically the gradient boosting framework. It utilizes decision trees as base learners and employs regularization techniques to enhance model generalization.

![image](https://github.com/Shreshtth/Fraud-Detection/assets/98511654/7c25a90d-b71c-4444-94bb-d7fb863cfe68)

### Hyperparameter Tuning (XGBoost)
Just to improve XGBoost model performance, I tried **RandomizedSearchCV** method to determine best parameters for XGB.

### Results -
```markdown
| Model         | Accuracies | F1 Scores | ROC AUC  | Time Taken |
|---------------|------------|-----------|----------|------------|
| LogisticReg   | 0.9538     | 0.9538    | 0.9538   | 2.0527     |
| GaussianNB    | 0.9355     | 0.9354    | 0.9355   | 1.0889     |
| DecisionTree  | 0.9954     | 0.9954    | 0.9954   | 21.3026    |
| RandomForest  | 0.9994     | 0.9994    | 0.9994   | 292.0923   |
| XGB           | 0.9622     | 0.9622    | 0.9622   | 4.8818     |
```
**Random Forest** gave the best accuracy *99.94%* being computational expensive while **Decision Tree** provided *99.54%* accuracy being computational inexpensive.

## Potential Use Cases:

- **Credit Card Fraud Detection**: Build machine learning models to detect and prevent credit card fraud by identifying suspicious transactions based on the provided features.
- **Merchant Category Analysis**: Examine how different merchant categories are associated with fraud.
- **Transaction Type Analysis**: Analyze whether certain types of transactions are more prone to fraud than others.
