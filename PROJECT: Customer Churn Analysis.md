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

After observation, it is found that the "tenure" of these 11 users is 0 months, which is supposed to be the new users in the current month. According to the general experience, even if the user cancell the service within the month of registration, he has to pay the current month fee. 

Therefore, we need to fill the monthly charges into the total charges, which is in line with the actual situation.

![cus-11](https://github.com/sichensong-99/Analysis-Projects/blob/master/Pics/cus-11.png)

![cus-13](https://github.com/sichensong-99/Analysis-Projects/blob/master/Pics/cus-13.png)

## Visualize analysis results


