# Analytic500_lung-cancer

The dataset we use is called 'dataset.csv'. Same data is also available as 'dataset.json'. 

EDA on the data:
1. Predictor variables are: 'AGE'	'SMOKING'	'YELLOW_FINGERS'	'ANXIETY'	'PEER_PRESSURE'	'CHRONIC_DISEASE'	'FATIGUE'	'ALLERGY'	'WHEEZING'	'ALCOHOL_CONSUMING'	'COUGHING'	'SHORTNESS_OF_BREATH'	'SWALLOWING_DIFFICULTY'	'CHEST_PAIN'.
2. Target variable is 'LUNG_CANCER'. The distribution of target variable in the code shows that the data is well balanced.
3. Except 'GENDER', all the other variables are numerical. 'GENDER' is of the data type 'object' with either 'M' or 'F'.
4. All numerical variables except 'AGE' are either '1' or '2'. This means they are all categorical variables. The 'AGE' range is between 30-80 years. The distribution of 'AGE' shows that data has been collected among all age ranges without any bias. The histogram of all variables gives us a better understanding about this.
5. All the categorical variables are converted from ('1', '2') to ('0', '1') levels. This is to standardize the levels and for better interpretation in models.
6. There are no missing values in any of the columns.
7. The correlation matrix shows that all the variables are independent of each other, thus removing any possibility of multicollinearity.
8. We now proceed to perform some checks for additivity, linearity, homoscedasticity, homogenity and normality. For non-parametric models and tree based models like Random Forest and Gradient Boosting, we don't need to perform these checks. But for Logistic Regression model, we need to perform a linearity and additivity check between the continous variable and target variable since it assumes a linear relationship between them.
9. The linearity check between 'AGE' and target variable fails. This means we need to use a non-linear model like Random Forest or GBM.  
10. The additivity checks works since the p value is greater than 0.05.

Next steps to do:
1. Feature Engineering
2. Model development
3. Model evaluation

