# PROJECT: User Churn Analysis 
![cus-1](https://github.com/sichensong-99/Analysis-Projects/blob/master/Pics/cus-1.jpg)

The project includes 6 parts: 
1. Background
2. Problem
3. Understand Data
4. Clean Data
5. Visualize analysis results
6. Findings and Recommendations

## Background
There is a view on user retention. If the user churn rate is reduced by 5%, the company's profit will increase by 25% - 85%.

Nowadays, the high cost of acquiring customers makes telecom operators encounter the "ceiling", and even fall into the dilemma of getting customers. With the increase of market saturation, telecom operators need to solve the problem of increasing user stickiness and user lifecycle. Therefore, it is very important to analyze the churn rate of telecom users. 

The data set comes from "telecom operator customer data set" in kesci.

## Problem
a. What's the relationship between user characteristics and churn rate?

b. What are the common characteristics of lost users? 

c. How to increase user stickiness and prevent user churn?

## Understand Data

According to the introduction, the dataset has 21 columns, a total of 7043 records. 

Each record contains the characteristics of each unique customer.

## Clean Data
#### Import libraries in Python

![cus-2](https://github.com/sichensong-99/Analysis-Projects/blob/master/Pics/cus-2.png)

#### Import Dataset

![cus-3](https://github.com/sichensong-99/Analysis-Projects/blob/master/Pics/cus-3.png)

#### Check data size

![cus-4](https://github.com/sichensong-99/Analysis-Projects/blob/master/Pics/cus-4.png)

#### Check the first 10 data

![cus-5](https://github.com/sichensong-99/Analysis-Projects/blob/master/Pics/cus-5.png)

#### Check Datatype
![cus-6](https://github.com/sichensong-99/Analysis-Projects/blob/master/Pics/cus-6.png)

![cus-7](https://github.com/sichensong-99/Analysis-Projects/blob/master/Pics/cus-7.png)

We could find out that the data type of TotalCharges is object, which is not correct. Then we need to transfer the data type from object into float.

![cus-8](https://github.com/sichensong-99/Analysis-Projects/blob/master/Pics/cus-8.png)

![cus-12](https://github.com/sichensong-99/Analysis-Projects/blob/master/Pics/cus-12.png)

#### Check missing value
![cus-9](https://github.com/sichensong-99/Analysis-Projects/blob/master/Pics/cus-9.png)

Here are 11 missing values.

![cus-10](https://github.com/sichensong-99/Analysis-Projects/blob/master/Pics/cus-10.png)

After observation, it is found that the "tenure" of these 11 users are 0 months, which is supposed to be the new users in the current month. According to the general experience, even if the user cancels the service within the month of registration, he/she has to pay the current month fee. 

Therefore, we need to fill the monthly charges into the total charges, which is in line with the actual situation.

![cus-11](https://github.com/sichensong-99/Analysis-Projects/blob/master/Pics/cus-11.png)

![cus-13](https://github.com/sichensong-99/Analysis-Projects/blob/master/Pics/cus-13.png)

## Visualize analysis results

User characteristics are divided into user attributes, service attributes and contract attributes, and visual analysis is carried out from these three dimensions.

#### Check the number of customer churn and ratio

![cus-14](https://github.com/sichensong-99/Analysis-Projects/blob/master/Pics/cus-14.png)

![cus-15](https://github.com/sichensong-99/Analysis-Projects/blob/master/Pics/cus-15.png)

### 1) User attributes analysis

![cus-16](https://github.com/sichensong-99/Analysis-Projects/blob/master/Pics/cus-16.png)

![cus-17](https://github.com/sichensong-99/Analysis-Projects/blob/master/Pics/cus-17.png)

![cus-18](https://github.com/sichensong-99/Analysis-Projects/blob/master/Pics/cus-18.png)

![cus-19](https://github.com/sichensong-99/Analysis-Projects/blob/master/Pics/cus-19.png)

#### Conclusion
a. User churn is not related to gender.

b. The user churn rate of SeniorCitizen is significantly higher than that of non-SeniorCitizen.

![cus-20](https://github.com/sichensong-99/Analysis-Projects/blob/master/Pics/cus-20.png)

![cus-21](https://github.com/sichensong-99/Analysis-Projects/blob/master/Pics/cus-21.png)

![cus-22](https://github.com/sichensong-99/Analysis-Projects/blob/master/Pics/cus-22.png)

![cus-23](https://github.com/sichensong-99/Analysis-Projects/blob/master/Pics/cus-23.png)

#### Conclusion

a. The churn rate of user who has partner is lower than that of user who hasn't partner.

b. Few users have dependents.

c. The churn rate of user who has dependents is lower than that of user who hasn't dependents.

d. The longer the tenure is, the lower the user churn rate is, which is in line with the general experience.

e. The user churn rate is lower than the retention rate when tenure reaches 3 months, which proves that psychological stability period of users is generally 3 months.



### 2) Service attributes analysis

![cus-24](https://github.com/sichensong-99/Analysis-Projects/blob/master/Pics/cus-24.png)

![cus-25](https://github.com/sichensong-99/Analysis-Projects/blob/master/Pics/cus-25.png)

![cus-26](https://github.com/sichensong-99/Analysis-Projects/blob/master/Pics/cus-26.png)

![cus-27](https://github.com/sichensong-99/Analysis-Projects/blob/master/Pics/cus-27.png)

![cus-28](https://github.com/sichensong-99/Analysis-Projects/blob/master/Pics/cus-28.png)

![cus-29](https://github.com/sichensong-99/Analysis-Projects/blob/master/Pics/cus-29.png)

#### Conclusion

a. Phone service has little impact on user churn.

b. The chrun rate of fiber optic users is relatively high.

c. The churn rate of optical fiber users with OnlineSecurity, OnlineBackup, DeviceProtection and TechSupport services is low.

d. The churn rate of optical fiber users with StreamingTV and SteamingMovies services is relatively high.



### 3) Contract attributes analysis

![cus-30](https://github.com/sichensong-99/Analysis-Projects/blob/master/Pics/cus-30.png)

![cus-31](https://github.com/sichensong-99/Analysis-Projects/blob/master/Pics/cus-31.png)

![cus-32](https://github.com/sichensong-99/Analysis-Projects/blob/master/Pics/cus-32.png)

![cus-33](https://github.com/sichensong-99/Analysis-Projects/blob/master/Pics/cus-33.png)

#### Conclusion

a. The churn rate of users with electronic check payment is the highest.

b. The impact of contract signing method on user churn rate is as follows: signing by month > signing by one year > signing by two years. It proves that long-term contracts      are the best way to retain customers.

c. The user churn rate is the highest when monthly charges is around $70 -$110.

d. In the long term, the higher total charges, the lower user churn rate.


## Findings and Recommendations


### User characteristics with high churn rate:

1) User attributes

SeniorCitizen, users who haven't partner and users who haven't dependent  

2) Service attributes

a. The subscription length is less than half of a year.

b. User who subscribes phone service.

c. Optical fiber users/ Optical fiber users with StreamingTV and SteamingMovies services or non-internet additional service

3) Contract attributes

a. Contract term is short.

b. Payment method is electronic check.

c. Paperless billing

d. Monthly charges is around $70 - $110


Note: Other attributes have little impact on user churn. Characteristics above are independent.


### Recommendations:

1) To make a user list with high churn rate, launch a new product feature based on user survey and invite seed users to try it out.

2) User
   For SeniorCitizen, user who hasn't partner and user who hasn't dependent, customized service can be offered such as family package, warm package, etc. It could strengthen relevance to other users and provides personalized service for target users.

3) Service
   a. For new users, providing semi-annual promotion, such as coupons, at the peak of user churn.
   
   b. For optical fiber users and optical fiber users with StreamingTV and SteamingMovies services, the key is to improve online experience and user experience of additional service. It could promote technical team to enhance network index and increase user stickiness through free extra-service such as network upgrading or movie subscription service.
   
   c. To promote additional service, including OnlineSecurity, OnlineBackup, DeviceProtection, TechSupport, etc, to the public, such as free physical examinations during the first month/ year of subscription.

4) Contract

   a. For users with month-to-month contract, promoting discount on one-year contract so that contract term and user retention could be improved.
   
   b. For users with electronic check payment, promoting coupons for other payment methods directly so that users might be guided to change their payment methods.
