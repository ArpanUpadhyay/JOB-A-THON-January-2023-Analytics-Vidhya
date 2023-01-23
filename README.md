# JOB-A-THON-January-2023-Analytics-Vidhya
Here I am sharing my approach and code file for Job-a-thon hosted by Analytics Vidhya in January 2023.

Problem Statement :

VahanBima is one of the leading insurance companies in India. It provides motor vehicle insurances
at best prices with 24/7 claim settlement. It offers different types of policies for both personal and
commercial vehicles. It has established its brand across different regions in India.
Around 90% of the businesses today use personalized services. The company wants to launch
different personalized experience programs for customers of VahanBima. The personalized
experience can be dedicated resources for claim settlement, different kinds of services at doorstep, etc.
Inorder to do so, they would like to segment the customers into different tiers based on their customer
lifetime value (CLTV).
Inorder to do it, they would like to predict the customer lifetime value based on the activity and
interaction of the customer with the platform. So, as a part of this challenge, your task at hand is to
build a high performance and interpretable machine learning model to predict the CLTV based on the
user and policy data.

The train data given to us has information regarding the customers and policies of
VahanBima. It also tells us about each customer’s CLTV. Thus the problem given to us is a
regression problem as CLTV is a continuous variable.

First of all I have checked whether the train data contains any null values or not. Then I am
doing exploratory data analysis for each variable(column) in the train data. I have also
shown that claim_amount has a weak correlation with CLTV of the customers.

I have also shown that gender and marital status do not play a significant role in prediction of
CLTV. Thus in our data, the Independent features are ‘area', 'qualification', 'income',
'vintage', 'claim_amount', 'num_policies', 'policy', 'type_of_policy and the dependent variable
is ‘cltv’. I have removed ‘id’,’gender’ and ‘marital_status’ columns as they do not have much
significance in predicting cltv.

After doing exploratory data analysis for each column type, I have done one hot encoding for
categorical values and then splitted the train data into training and validation sets.

There are 4 models in my code notebook. The best model is the one in which I have
excluded outliers in the claim amount and have taken a natural log of CLTV and finally I have
extracted polynomial features of independent columns in my training data.

I have fitted training data using Linear regression model using Ordinary Least Squares
method.

The r2_score for Model 4 is highest among all other models and it is 0.342.
Finally I have predicted cltv for test data using the trained model.
