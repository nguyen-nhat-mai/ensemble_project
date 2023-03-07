# Ensemble project
By Haiwei FU, Mengyu LIANG, Nhat Mai NGUYEN, Jinji SHEN and Vanshika SHARMA

## 1. Airbnb price prediction
### 1.1 Motivation
Predicting Airbnb prices in New York City can be a fascinating project because it offers an excellent opportunity to study and understand the factors that impact Airbnb prices in one of the most vibrant and diverse cities in the world. The project is relevant to real-world applications, and the insights obtained can have a practical impact in the hospitality industry. For example, the hosts and guests can make more informed decisions, leading to better experiences and more effective use of resources. 

In the context of this project, we can explore the relationship between different features such as location, amenities, and host characteristics, and how they affect the price of a listing. Additionally, we can investigate how different ensemble methods like Random Forest, Gradient Boosting, etc. can improve the accuracy and robustness of the predictions.
### 1.2 Methodology
![image](https://user-images.githubusercontent.com/85484281/223385274-e0ea8c7a-5622-4228-ac1a-3143850b2ec1.png)

During the exploration, we gain some remarkable insights into the data and process the data in accordance:
- There are no duplicates but there are about 10k null data in last_review and reviews_per_month. Since these imply the airbnb does not have review, we imput these missing values by 0
- The distribution of price is highly skewed. By taking logarithm, the distribution is closer to normal distribution. Given that many statistical models and machine learning algorithms assume that the target variable follows a normal distribution, we use log(price) as target to ensure the performance of models.

![image](https://user-images.githubusercontent.com/85484281/223405422-617fa0e0-381f-400c-be42-95701c337a5a.png)
- The price highly depends on the location of the apartment. Here, the price of airbnbs in Manhattan region are higher than other regions

![image](https://user-images.githubusercontent.com/85484281/223406679-c52b5ea6-c602-4847-b138-8a153c32572e.png)
- 
### 1.3 Conclusion

## 2. Self-built decision tree
