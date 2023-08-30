# Customer Churn Prediction
Customer Churn Prediction using ML:  Effective solution to anticipate customer churn, improve retention, and drive business growth
![Customer-Churn](https://github.com/preemaldsouzaa/Customer_Churn_Prediction/assets/117831091/bf059bcd-692c-452f-8e48-5fc3aeb4f654)


## Introduction
Customer churn is a major issue for every firm, especially those in the telecommunications industry. Churn is the occurrence in which clients cancel their services or memberships with a company. Identifying consumers who are likely to churn ahead of time can greatly benefit the organization by allowing it to take proactive actions to keep these customers.
The goal of this study is to apply Machine Learning (ML) techniques to anticipate customer turnover in a telecommunications company. We can uncover patterns and factors that contribute to churn by studying past customer data and developing a predictive model. This will allow the telecommunications company to develop targeted retention measures and improve customer satisfaction, reducing churn and enhancing long-term business performance.

## Problem Statement:
The problem that we want to address is predicting customer attrition in a telecommunications company using historical customer data. We will create a predictive model that can categorize clients as churned or non-churned by applying machine learning methods on the given dataset. The goal is to develop an accurate and dependable model to assist the Telco company in reducing customer turnover.

## Objectives:
1. Data Preprocessing: Clean the dataset, handle missing values (if any), and encode categorical variables.

2. Exploratory Data Analysis (EDA): Perform a comprehensive analysis of the dataset to identify patterns, correlations, and insights that may influence churn.

3. Feature Selection: Select the most relevant features that have a significant impact on churn prediction.

4. Model Selection: Choose appropriate machine learning algorithms for classification and compare their performance.

5. Model Training: Train the selected models on the preprocessed data.

6. Model Evaluation: Evaluate the models using appropriate evaluation metrics like accuracy, precision, recall, F1 score, etc.

7. Hyperparameter Tuning: Optimize the chosen models by tuning hyperparameters to improve predictive performance.

8. Churn Prediction: Deploy the best-performing model to predict customer churn for the Telco company.

## Advantages
1. Retention Strategies: The predictive model will enable the Telco company to implement targeted retention strategies, such as personalized offers or discounts, to retain customers at risk of churning.

2. Resource Allocation: By identifying potential churners, the company can allocate resources more efficiently by focusing efforts on high-risk customers, rather than implementing broad and costly retention strategies.

3. Customer Satisfaction: Understanding churn factors can help the company improve services, address pain points, and enhance overall customer satisfaction.

4. Competitive Edge: Utilizing ML for churn prediction can give the Telco company a competitive edge by being proactive and responsive to customer needs.

## Information of Dataset:
The dataset contains 7043 rows (customers) and 21 columns (features) which provides comprehensive information about a Telco company's customers, enabling a detailed analysis of customer churn and preferences. It includes the following key aspects:

1. CustomerId : Customer Id
2. Gender : Gender
3. SeniorCitizen : Whether the customer is a senior citizen (1, 0)
4. Partner : Whether the client has a partner (Yes, No) ? Married or not. Living together, being roommates
5. Dependents : Whether the client has dependents (Yes, No) (Child, mother, father, grandmother)
6. tenure : Number of months the customer stays with the company PhoneService : Whether the customer has phone service (Yes, No)
7. MultipleLines : Whether the customer has more than one line (Yes, No, No phone service)
8. InternetService : Customer's internet service provider (DSL, Fiber optic, No)
9. OnlineSecurity : Whether the customer has online security (Yes, No, No Internet service)
10. OnlineBackup : Whether the customer has online backup (Yes, No, No Internet service)
11. DeviceProtection : Whether the customer has device protection (Yes, No, No Internet service)
12. TechSupport : Whether the customer receives technical support (Yes, No, No Internet service)
13. StreamingTV : Whether the customer has streaming TV (Yes, No, no Internet service) (The customer has a third-party indicates whether the provider uses the Internet service to broadcast television programs)
14. StreamingMovies : Whether the customer has streaming movies (Yes, No, No Internet service) (Customer has a third-party Indicates whether the customer is using the Internet service to stream movies from the provider)
15. Contract : Duration of the customer's contract (Month to month, One year, Two years)
16. PaperlessBilling : Whether the customer has a paperless bill (Yes, No)
17. PaymentMethod : Customer's payment method (Electronic check, Postal check, Bank transfer (automatic), Credit card (automatic)
18. MonthlyCharges : Amount charged to the customer monthly
19. TotalCharges : Total amount charged to the customer
20. Churn : Whether the customer is using or not (Yes or No) - Customers who left in the last month or quarter.

Each row represents a unique customer. Variables contain information about customer service, account and demographic data. Services that customers sign up for => phone, multiple lines, internet, online security, online backup, device protection, technical support and TV and movie streaming. Customer account information => how long they have been a customer, contract, payment method, paperless billing, monthly fees and total fees. Demographic information about clients => gender, age range and partners and dependents whether or not.

## Exploratory Data Analysis (Key Points)
Here's a summary of some key points that we have derived from our EDA (Exploratory Data Analysis):
1. Gender distribution among customers is almost equal. Churn rate is similar between genders, indicating both genders have similar churn behavior.
2. Customers with month-to-month contracts have a significantly higher churn rate. One-year and two-year contract customers exhibit lower churn rates.
3. Customers using Electronic Check as their payment method have a higher churn rate. Credit Card Automatic Transfer and Bank Automatic Transfer users are less likely to churn.
4. Customers with Fiber optic service have a higher churn rate compared to DSL users. DSL users have a lower churn rate, suggesting higher satisfaction.
5. Customers without dependents are more likely to churn compared to those with dependents.
6. Customers without partners are often more likely to churn than those with partners.
7. Senior citizens have a higher churn rate, although their fraction in the dataset is low.
8. The absence of online security leads to higher churn rates.
9. Customers with paperless billing are more likely to churn.
10. Lack of tech support increases the likelihood of churn.
11. A small fraction of customers without phone service, one-third of whom are more likely to churn.
12. Customers with higher monthly charges are more likely to churn.
13. The distribution of total charges is similar for churn and non-churn customers.
14. New customers tend to have higher churn rates.

These insights provide a comprehensive understanding of factors contributing to customer churn. Businesses can use this information to develop strategies aimed at reducing churn and improving customer retention.

## Data Preprocessing - Handling Class Imbalance with SMOTE

In the context of binary classification, such as predicting customer churn, class imbalance occurs when one class significantly outnumbers the other. In our dataset, we observed a class distribution as follows:

-Class 0 (No Churn): 5163 samples
-Class 1 (Churn): 1869 samples

This class imbalance issue can impact the performance of machine learning models. When one class dominates, the model may become biased towards predicting the majority class, resulting in poor predictions for the minority class. To address this issue and we have ensured that the model can effectively learn from both classes, we have then employed a technique called SMOTE (Synthetic Minority Over-sampling Technique).

## Model Development:
In the process of developing predictive models for customer churn, a diverse set of machine learning algorithms was explored and evaluated. Each model, from K-Nearest Neighbors to Random Forest, exhibited varying degrees of accuracy and predictive capability. The Decision Tree Classifier stood out as the top performer among individual models, achieving an accuracy of approximately 81.70%. This model's detailed classification report showcased strong precision, recall, and F1-score metrics. Moreover, ensemble learning techniques, including AdaBoost and Gradient Boosting, proved highly effective, with the Gradient Boosting Classifier emerging as the best performer among all models, boasting an accuracy of 86.16%. The ensemble model, created using a Voting Classifier, further enhanced predictive accuracy to 86.50%, underlining the importance of combining the strengths of multiple models in solving complex business challenges like customer churn prediction.

This comprehensive approach to model development equips decision-makers with a diverse toolkit to make accurate predictions and strategically address customer churn. These models, backed by robust evaluation metrics, offer valuable insights into customer behavior and provide a solid foundation for optimizing retention strategies and enhancing the overall customer experience.

## Conclusion:
As we can see, ensemble learning is beneficial because it leverages the diverse strengths of each model, leading to improved overall performance compared to using individual models alone. By combining multiple models, the VotingClassifier helps to mitigate the risk of overfitting and enhances the model's ability to generalize well on unseen data.

After training the VotingClassifier on the customer churn dataset, we evaluated its performance. The final accuracy score achieved by the VotingClassifier was 86.6%, indicating that it accurately predicted customer churn in a significant portion of cases.

The classification report provided additional insights into the model's performance. It revealed balanced precision and recall scores for both churned and retained customers. Balanced precision and recall are essential metrics in churn prediction because they ensure that the model accurately identifies both customers who are likely to churn (recall) and those who genuinely churn (precision).

Furthermore, we visualized the confusion matrix, which showcased the model's correct and incorrect predictions. It correctly predicted 917 retained customers and 870 churned customers. However, there were 121 false positives (incorrectly predicted as churned) and 159 false negatives (incorrectly predicted as retained). The balanced number of false positives and false negatives indicates that the VotingClassifier maintains a good balance between avoiding unnecessary actions for false positives and minimizing revenue loss due to false negatives.

Overall, the VotingClassifier demonstrated its effectiveness and robustness in predicting customer churn, making it a suitable and reliable choice for this particular task. Its ability to combine the strengths of different models allows it to make accurate predictions and provides valuable insights to help businesses retain customers and optimize their strategies.
