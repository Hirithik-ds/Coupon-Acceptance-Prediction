# Coupon-Acceptance-Prediction
Model built with XGBoost, LGBM, Catbost, Random Forest, SVM, Logistic regression

# Problem Statement
The purpose of this project is to apply machine learning techniques to assess driving scenarios and user information gathered from an e-commerce website. By precisely predicting whether users will accept coupons during their trips, the goal is to improve coupon distribution techniques and increase user engagement with the platform's products.
 The survey discusses various driving scenarios, such as the user's destination, current time, weather, passenger, coupon qualities, user attributes, and contextual factors, before asking the user if he or she will take the coupon or not.

 # Data Dictionary

- Gender: Female, Male
- Age: 21, 46, 26, 31, 41, 50plus, 36, below21
- Marital Status: Unmarried partner, Single, Married partner, Divorced, Widowed
- has_Children: 1: has children, 0: No children
- Education: Some colleges — no degree, bachelor’s degree, Associates degree, High School Graduate, Graduate degree (Master or Doctorate), Some High School
- Occupation: Traveller’s occupation
- Income: income of the traveler
- Car: Description of vehicle driven by the traveller
- Bar: how many times does the traveler go to a bar every month?
- Coffee House: how many times does the user go to a coffeehouse every month?
- Carry Away: how many times does the user get takeaway food every month?
- RestaurantLessThan20: how many times does the user go to a restaurant with an average expense per person of less than $20 every month?
- Restaurant20To50: how many times does the user go to a restaurant with an average expense per person of  20— 50 every month
- Destination: destination of traveler
- Passenger: who are the passengers in the car
- Weather: weather when the user is driving (Sunny, Rainy, Snowy)
- Temperature: temperature in Fahrenheit when the user is driving
- Coupon: Type of Coupon
- Expiration: Validity of Coupon
- toCoupon_GEQ5min: driving distance to the restaurant/cafe/bar for using the coupon is greater than 5 minutes (0,1)
- toCoupon_GEQ15min: driving distance to the restaurant/cafe/bar for using the coupon is greater than 15 minutes (0,1)
- toCoupon_GEQ25min: driving distance to the restaurant/cafe/bar for using the coupon is greater than 25 minutes (0,1)
- direction_same: whether the restaurant/cafe/bar is in the same direction as the traveler’s current destination (0,1)
- direction_opp: whether the restaurant/cafe/bar is in the opposite direction as the user’s current destination (0,1)
- Accept(Y/N?)- Target column( whether user will accept the coupon or not?)

# Data Cleaning and Preprocessing

- The Column Car have been removed because it has more than 90 % null values
- Duplicate rows have been removed from the dataset
- Studied Univariate and Bivariate Analysis on the feature columns and studied the distribution pattern based on various coupons product the target variable is mostly dependent on type of coupon age  income and occupation of the indvidual
- Used Label Encoding for the categorical Features.

# MultiColinearity

There were no Multicolinearity found among the features.

![image](https://github.com/user-attachments/assets/9b8d8c3c-69c2-4f47-b921-c3c5aa83ce54)

# Machine Learning Models used:
- Logistic Regression
- Support Vector Machines (SVM)
- Random Forest Classifier
- XGBoost
- CatBoost
- LightBGM

# Feature Selection by Random Forest

![image](https://github.com/user-attachments/assets/8e431819-d860-41c1-83a1-5e6a80798954)


# ROC Curve

![image](https://github.com/user-attachments/assets/fddf9d28-6a6c-4cba-9efe-1fce065517cd)

SVM and Logistic Regression Model were not performing good for this dataset due to low accuracy rate we are considering only XGBoost, RandomForest, Catboost amd LightBGM.

# Models Performance(Accuracy):

![image](https://github.com/user-attachments/assets/434f4a13-2458-4de4-bce6-4c4f7379e909)

We could see the Performance of the Tree Based Algorithm are better comparing the SVM and Logistic Regression Algorithm and CatBoost have the Highest Accuracy of 74.77%





