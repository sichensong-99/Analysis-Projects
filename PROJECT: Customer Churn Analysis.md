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

b. Proportion of SeniorCitizen is significantly higher than that of non-SeniorCitizen.

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

