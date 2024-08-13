# Bank Customer Churn Prediction

## Project Overviews
Customer churn prediction is crucial for banks aiming to retain clients and improve their services. By understanding the factors that lead to customer churn, banks can take proactive measures to enhance customer satisfaction and loyalty. In this blog, we'll explore a comprehensive approach to predicting customer churn using machine learning models and techniques, including data preprocessing, model training, and performance evaluation.

## Data Overview
### Dataset:
**Source**: [Bank Customer Churn Prediction](https://www.kaggle.com/datasets/shantanudhakadd/bank-customer-churn-prediction)

We utilized a dataset containing various features about bank customers, including their demographics, financial status, and engagement with the bank. The primary features in the dataset are:
| **Feature**       | **Description**                                               |
|-------------------|---------------------------------------------------------------|
| CreditScore       | The credit score of the customer.                              |
| Geography         | The country where the customer resides.                        |
| Gender            | The gender of the customer.                                    |
| Age               | The age of the customer.                                       |
| Tenure            | The number of years the customer has been with the bank.       |
| Balance           | The balance left in the customer's account.                    |
| NumOfProducts     | The number of products the customer has with the bank.         |
| HasCrCard         | Whether the customer has a credit card.                        |
| IsActiveMember    | Whether the customer is an active member.                      |
| EstimatedSalary   | The estimated salary of the customer.                          |
| Exited            | Whether the customer has churned (target variable).            |



## Data Preprocessing
### Exploratory Data Analysis (EDA)
To understand the dataset better, we performed EDA. Key insights include:

- **Distribution of Numeric Features**: We used box plots and distribution plots to visualize the spread and central tendencies of features like CreditScore, Age, Tenure, Balance, and EstimatedSalary.
- **Categorical Feature Analysis**: Count plots helped us analyze the distribution of categorical features such as Geography, HasCrCard, IsActiveMember, and NumOfProducts.
- **Pairwise Relationships**: A pair plot showed the relationships between different features, colored by the target variable, Exited.

### Handling Missing Values and Encoding
- **No Missing Values**: The dataset did not have any missing values.
- **One-Hot Encoding**: We applied one-hot encoding to nominal features like Geography and Gender to convert them into numerical values suitable for model training.

### Addressing Class Imbalance
To address the class imbalance in the target variable, we used Synthetic Minority Over-sampling Technique (SMOTE) to balance the classes in the training set.

## Model Training
We experimented with several machine learning models to predict customer churn, including Decision Tree, Random Forest, AdaBoost, and XGBoost. Below are the key steps and results for each model:
| **Model**                 | **Training Score** | **Test Score** | **F1 Score** | **Recall** | **Precision** |
|---------------------------|--------------------|----------------|--------------|------------|---------------|
| Decision Tree Classifier   | 81.71%             | 81.85%         | 0.5734       | 0.5995     | 0.5496        |
| Random Forest Classifier   | 90.41%             | 80.80%         | 0.5724       | 0.6315     | 0.5234        |
| AdaBoost Classifier        | 82.94%             | 78.30%         | 0.5470       | 0.6437     | 0.4755        |
| XGBoost Classifier         | 95.20%             | 81.30%         | 0.5769       | 0.6265     | 0.5346        |
| Voting Classifier          | 87.59%             | 82.05%         | 0.5680       | 0.5799     | 0.5566        |

## Model Evaluation
We evaluated each model using various metrics, including accuracy, precision, recall, and F1-score. Feature importance plots helped us identify which features had the most significant impact on predicting customer churn.

### Key Findings
- **Feature Importance**: Balance, Age, and CreditScore were among the most influential features in determining customer churn.
- **Model Performance**: While all models had their strengths, the Voting Classifier provided the best balance between training and test performance with an accuracy of 82.05% and an F1-score of 0.5680.
## Conclusion
Predicting customer churn is vital for banks to maintain their customer base and improve their services. Through a detailed analysis involving data preprocessing, EDA, handling class imbalance, and model tuning, we were able to develop effective models for churn prediction. By understanding and leveraging key features, banks can implement targeted strategies to retain their customers and reduce churn rates.
