# KNN-Data-Mining

A1: PROPOSAL OF QUESTION:

What factors predict the category of monthly charges for customers?

A2: DEFINED GOAL:

My goal for this data analysis is to find out what factors predict the category of monthly charges (low = 1, medium = 2, high = 3) for our customers. This is possible with the data we have, as it includes many features like demographics, service usage, and contract details that might influence monthly charges. By categorizing the MonthlyCharge into groups, cleaning and preprocessing the data, and selecting relevant features, I can train classification models like KNN to make these predictions. Evaluating the models will help me understand which factors are most important. This will help the company target the right customers with specific service deals, improve customer satisfaction, and increase revenue.

B1: EXPLANATION OF CLASSIFICATION METHOD:

I chose the K-Nearest Neighbors (KNN) classification method because it's simple and effective for this type of data. KNN analyzes the dataset by looking at the 'neighbors' of each data point. When predicting the category of monthly charges for a customer, KNN finds the most similar customers based on their features like age, income, and service usage and looks at the categories they belong to. The predicted category for a new customer is determined by the majority category among these neighbors. I expect that KNN will help identify clear patterns in how different customer characteristics influence their monthly charges, making it easier to predict whether a new customer will have low, medium, or high charges.

B2: SUMMARY OF METHOD ASSUMPTION:

One important idea behind using K-Nearest Neighbors (KNN) is that things that are close together are more likely to be the same. This means KNN assumes that if customers have similar features, like age or income, they will probably have similar monthly charges. The algorithm works by measuring the distance between data points, so it assumes that these distances actually show how similar the data points are.

B3: PACKAGES OR LIBRARIES LIST:

- Pandas is used to load, clean and prep the data for analysis.
- Numpy has numerical computations and matrices which is needed for feature scaling.
- Scikit-learn is necessary for Machine Learning because it has tools to implement KNN, split the data, evaluate the model.
- Matplotlib helps create visualizations of the data and present analysis results.
- Seaborn also has visualization capabilities, also can help us identify patters and understand the data.
- StandardScaler helps standardize the data to insure that KNN features contribute equally for distance calculations.

C1: DATA PREPROCESSING:

One data preprocessing goal relevant to the K-Nearest Neighbors (KNN) is to standardize the features. This goal ensures that all features contribute equally to the distance calculations used in KNN. Since KNN relies on measuring the distance between data points, having features on different scales, like income in thousands versus age in years, can skew the results. Standardizing the features by removing the mean, and scaling to unit variance ensures that each feature has an equal influence on the model.

C2: DATA SET VARIABLES
The variable I used in my analysis are:
1. Population (Numeric)
2. Area (Categorical)
3. Job (Categorical)
4. Children (Numeric)
5. Age (Numeric)
6. Income (Numeric)
7. Marital (Categorical)
8. Gender (Categorical)
9. Outage_sec_perweek (Numeric)
10. Email (Numeric)
11. Contacts (Numeric)
12. Yearly_equip_failure (Numeric)
13. Techie (Categorical)
14. Contract (Categorical)
15. Port_modem (Categorical)
16. Tablet (Categorical)
17. InternetService (Categorical)
18. Phone (Categorical)
19. Multiple (Categorical)
20. OnlineSecurity (Categorical)
21. OnlineBackup (Categorical)
22. DeviceProtection (Categorical)
23. TechSupport (Categorical)
24. StreamingTV (Categorical)
25. StreamingMovies - (Categorical)
26. PaperlessBilling (Categorical)
27. PaymentMethod (Categorical)
28. Tenure (Numeric)
29. Bandwidth_GB_Year (Numeric)

C3: STEPS FOR ANALYSIS:

The steps I took to prepare for this analysis were to import the necessary libraries and load the dataset. I then dropped irrelevant columns that would not contribute to predicting customer monthly charge categories. Next, I handled missing values by filling in numeric features with their median values and categorical features with the mode. After that, I one-hot encoded the categorical variables to convert them into a format suitable for machine learning models. For binary categorical variables, I converted them to 0 and 1, and used one-hot encoding for the rest. I kept the 'MonthlyCharge' as a numerical value instead of categorizing it into text labels. Finally, I split the data into training and testing sets to create and test the model.


D2: OUTPUT AND INTERMEDIATE CALCULATIONS:

The KNN model provided an overall accuracy of 66%, with varying precision and recall across different categories. The category '1' had the highest recall and F1-score, indicating better performance in predicting this category. The low precision and recall for categories '0' and '2' suggest a need for further data preprocessing, feature selection, or algorithm tuning to improve model performance.

![image](https://github.com/user-attachments/assets/4d3e1392-3885-4068-8590-0d08b5598ab3)

![image](https://github.com/user-attachments/assets/72cde2d7-e477-4c55-ab01-2a5bacf156ce)

E1: ACCURACY AND AUC:

The accuracy of my KNN classification model is 66%, meaning it correctly predicts the monthly charge category (0, 1, 2) for customers 66% of the time. However, the macro-averaged AUC is 0.51, which shows that the model's ability to distinguish between the different charge categories is only slightly better than random guessing. While the accuracy is decent, the low AUC indicates that the model struggles to differentiate well between the categories. To improve the model's performance, I need to focus on better data preprocessing, selecting more relevant features, and fine-tuning the KNN algorithm parameters.

E2: RESULTS AND IMPLICATIONS:

The results of my classification analysis show that while my KNN model has a 66% accuracy, its macro-averaged AUC of 0.51 indicates that it doesn't effectively distinguish between the 0, 1, and 2 charge categories. This means that the model is only slightly better than guessing when it comes to telling the categories apart. These results imply that there is a need for improvement in how the model handles the data and makes predictions. To get better results, I should look into improving data preprocessing, choosing better features, and adjusting the model's parameters to make more accurate predictions about monthly charges for customers.


E3: LIMITATION:

One limitation of my data analysis is that the KNN model's performance heavily depends on the quality and scale of the input features. Since KNN is sensitive to the distance between data points, any irrelevant or noisy features can negatively impact the model's accuracy. Additionally, without proper feature scaling, the model might give more importance to certain features over others. Despite my efforts to preprocess the data, there might still be underlying issues such as unaccounted biases or correlations that the model couldn't capture well, which could explain the lower-than-expected performance in distinguishing between the charge categories.

E4: COURSE OF ACTION:

I recommend that the organization focus on improving data preprocessing and feature selection to enhance the model's performance. This could involve collecting more relevant data, removing noisy or irrelevant features, and ensuring that all features are properly scaled. Additionally, experimenting with different algorithms or tuning the parameters of the KNN model could lead to better predictions. By refining the data and the model, the organization can achieve more accurate predictions of monthly charges, which can help in better understanding customer behaviors and making more informed business decisions.


