# PROJECT: Customer Churn Analysis 
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

Nowadays, the high cost of acquiring customers makes telecom operators encounter the "ceiling", and even fall into the dilemma of getting customers. With the increase of market saturation, telecom operators need to solve the problem of increasing user stickiness and prolonging user life cycle. Therefore, it is very important to analyze the loss of telecom users. 

The data set comes from "telecom operator customer data set" in kesci.

## Problem
a. Analyze the relationship between user characteristics and churn. 

b. From the perspective of the overall situation, what are the common characteristics of lost users? 

c. Provide recommendations to increase user stickiness and prevent loss.

## Understand Data

According to the introduction, the data set has 21 fields, a total of 7043 records. 

Each record contains the characteristics of each unique customer. The project is to find the relationship between characteristics of the first 20 columns and the last column (the customer churn feature).

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

After observation, it is found that the "tenure" of these 11 users are 0 months, which is supposed to be the new users in the current month. According to the general experience, even if the user cancell the service within the month of registration, he has to pay the current month fee. 

Therefore, we need to fill the monthly charges into the total charges, which is in line with the actual situation.

![cus-11](https://github.com/sichensong-99/Analysis-Projects/blob/master/Pics/cus-11.png)

![cus-13](https://github.com/sichensong-99/Analysis-Projects/blob/master/Pics/cus-13.png)

## Visualize analysis results

User characteristics are divided into user attributes, service attributes and contract attributes, and visual analysis is carried out from these three dimensions.

#### Check the number of customer churn and ratio

![cus-14](https://github.com/sichensong-99/Analysis-Projects/blob/master/Pics/cus-14.png)

![cus-15](https://github.com/sichensong-99/Analysis-Projects/blob/master/Pics/cus-15.png)

### User attributes analysis

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

a. The churn rate of customer who has partner is lower than customer who hasn't partner.

b. Few customer has dependents.

c. The churn rate of customer who has dependents is lower than customer who hasn't dependents.

d. The longer the tenure is, the lower the customer churn rate is, which is in line with the general experience.

e. The customer churn rate is lower than the stay-in rate when tenure reaches 3 months, which proves that psychological stability period of users is generally 3 months.

### Service attributes analysis

![cus-24](https://github.com/sichensong-99/Analysis-Projects/blob/master/Pics/cus-24.png)

![cus-25](https://github.com/sichensong-99/Analysis-Projects/blob/master/Pics/cus-25.png)

![cus-26](https://github.com/sichensong-99/Analysis-Projects/blob/master/Pics/cus-26.png)

![cus-27](https://github.com/sichensong-99/Analysis-Projects/blob/master/Pics/cus-27.png)

![cus-28](https://github.com/sichensong-99/Analysis-Projects/blob/master/Pics/cus-28.png)

![cus-29](https://github.com/sichensong-99/Analysis-Projects/blob/master/Pics/cus-29.png)

#### Conclusion

a. Phone service has little impact on customer churn.

b. The customer chrun rate of fiber optic is relatively high.

c. The churn rate of optical fiber users with OnlineSecurity, OnlineBackup, DeviceProtection and TechSupport services is low.

d. The churn rate of optical fiber users with StreamingTV and SteamingMovies services is relatively high.

### Contract attributes analysis

![cus-30](https://github.com/sichensong-99/Analysis-Projects/blob/master/Pics/cus-30.png)

![cus-31](https://github.com/sichensong-99/Analysis-Projects/blob/master/Pics/cus-31.png)

![cus-32](https://github.com/sichensong-99/Analysis-Projects/blob/master/Pics/cus-32.png)

![cus-33](https://github.com/sichensong-99/Analysis-Projects/blob/master/Pics/cus-33.png)

## Findings and Recommendations

#### According to analysis above, the user characteristics of high churn rate are obtained:

1) User attributes

SeniorCitizen, user who hasn't partner and user who hasn't dependent  

2) Service attributes

a. The subscription length is less than half of a year.

b. User who subscribes phone service.

c. Optical fiber users/ Optical fiber users with StreamingTV and SteamingMovies services or without internet additional service

3) Contract attributes

a. Contract term is short.

b. Payment method is electronic check.

c. Paperless billing

d. Monthly charges is around $70 - $110


Note: Other attributes have little impact on user churn. Characteristics above are independent.


#### According to findings above, here are recommendations:

1) To make a user list with high churn rate, launch a new product feature based on user survey and invite seed users to try it out.

2) Product

a. For SeniorCitizen, user who hasn't partner and user who hasn't dependent, customized service can be offered such as family package, warm package, etc.

用户方面：针对老年用户、无亲属、无伴侣用户的特征退出定制服务如亲属套餐、温暖套餐等，一方面加强与其它用户关联度，另一方对特定用户提供个性化服务。
服务方面：针对新注册用户，推送半年优惠如赠送消费券，以渡过用户流失高峰期。针对光纤用户和附加流媒体电视、电影服务用户，重点在于提升网络体验、增值服务体验，一方面推动技术部门提升网络指标，另一方面对用户承诺免费网络升级和赠送电视、电影等包月服务以提升用户黏性。针对在线安全、在线备份、设备保护、技术支持等增值服务，应重点对用户进行推广介绍，如首月/半年免费体验。
合同方面：针对单月合同用户，建议推出年合同付费折扣活动，将月合同用户转化为年合同用户，提高用户在网时长，以达到更高的用户留存。 针对采用电子支票支付用户，建议定向推送其它支付方式的优惠券，引导用户改变支付方式。

