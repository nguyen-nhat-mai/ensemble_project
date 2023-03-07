# Ensemble project
By Haiwei FU, Mengyu LIANG, Nhat Mai NGUYEN, Jinji SHEN and Vanshika SHARMA

## 1. Airbnb price prediction
### 1.1 Motivation
Predicting Airbnb prices in New York City can be a fascinating project because it offers an excellent opportunity to study and understand the factors that impact Airbnb prices in one of the most vibrant and diverse cities in the world. The project is relevant to real-world applications, and the insights obtained can have a practical impact in the hospitality industry. For example, the hosts and guests can make more informed decisions, leading to better experiences and more effective use of resources. 

In the context of this project, we can explore the relationship between different features such as location, amenities, and host characteristics, and how they affect the price of a listing. Additionally, we can investigate how different ensemble methods like Random Forest, Gradient Boosting, etc. can improve the accuracy and robustness of the predictions.
### 1.2 Methodology
![image](https://user-images.githubusercontent.com/85484281/223385274-e0ea8c7a-5622-4228-ac1a-3143850b2ec1.png)

During the exploration, we gain some remarkable insights into the data and process the data in accordance:
- From our check, there are no duplicates or format inconsistency but there are about 10k null data in last_review and reviews_per_month. Since these imply the airbnb does not have review, we impute these missing values by 0
- The distribution of price is highly skewed. By taking logarithm, the distribution is closer to normal distribution. Given that many statistical models and machine learning algorithms assume that the target variable follows a normal distribution, we use log(price) as target to ensure the performance of models. Normally, any observations that are more than 1.5 IQR below Q1 or more than 1.5 IQR above Q3 are considered outliers. In this case, we can see that log(price) has the huge amount of outliers (22% belongs to "outlier" category). However, such huge amount of outliers sometimes can be useful info that reflect the underlying distribution. So we decide to create 2 scenarios to test out:
  - Consider such 22% data as outliers => remove them
  - Consider such 22% data as useful info for prediction => keep them

![image](https://user-images.githubusercontent.com/85484281/223415608-7fdf04a6-7f9e-48d1-a6e5-d64f5b91c8e0.png)
- The price highly depends on the location of the apartment. Here, the prices of airbnbs in Manhattan region are higher than other regions

![image](https://user-images.githubusercontent.com/85484281/223406679-c52b5ea6-c602-4847-b138-8a153c32572e.png)
- Except for location features, distributions of other numerical variables are high skewed. Though taking logarithm does not help normalize these variables, we still keep them as potential features. Besides, since the variables are highly concentrated in certain values, we think other yes/no features such as no_review, fully_available, low_available, etc. can provide some some information for predicting price, we added them to the feature pool

![image](https://user-images.githubusercontent.com/85484281/223412707-150b3836-a99f-4985-8d5d-2fe20c50a1f8.png)
- Most of the variables are uncorrelated (except for newly added features and original features that these new features are extracted from)

![image](https://user-images.githubusercontent.com/85484281/223413913-01b17d09-d610-4626-a066-13e4366c7fb5.png)
- After encoding categorical data and rescaling values to avoid the dominance of large-value features, we measure the feature importance by impurity reduction via default random forest model. Location info and room type info seems to have high predicting power. Using such insight, we proceed with the modeling phase.

For this classification problem, we used the following models:
- Decision tree: a supervised learning algorithm used in machine learning for classification and regression analysis. It creates a tree-like structure where each internal node represents a feature or attribute, each branch represents a decision rule, and each leaf node represents a class label or a numerical value. Decision trees work by recursively splitting the data into smaller subsets based on the most informative features until a stopping criterion is met, such as reaching a maximum depth or minimum number of samples per leaf. They are popular for their interpretability and ability to handle categorical and numerical data, but they can be prone to overfitting and instability.
- Random forest

....

Evaluation metrics
...

### 1.3 Conclusion

## 2. Self-built decision tree
