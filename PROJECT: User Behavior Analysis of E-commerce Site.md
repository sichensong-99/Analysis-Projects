# PROJECT: User Behavior Analysis of E-commerce Site
![E](https://github.com/sichensong-99/Analysis-Projects/blob/master/Pics/WeChat%20Image_20200817012454.png)

## 1. Check Data

### 1.1 Load Library in Python
![E-1](https://github.com/sichensong-99/Analysis-Projects/blob/master/Pics/E-1.jpg)

![E-2](https://github.com/sichensong-99/Analysis-Projects/blob/master/Pics/E-2.jpg)

### 1.2 Read Data
![E-3](https://github.com/sichensong-99/Analysis-Projects/blob/master/Pics/E-3.jpg)

### 1.3 Examine Data Types and Data Structures
![E-4](https://github.com/sichensong-99/Analysis-Projects/blob/master/Pics/E-4.jpg)

Output:

![E-5](https://github.com/sichensong-99/Analysis-Projects/blob/master/Pics/E-5.jpg)

![E-6](https://github.com/sichensong-99/Analysis-Projects/blob/master/Pics/E-6.jpg)

### 1.4 Handle Missing Value

![E-7](https://github.com/sichensong-99/Analysis-Projects/blob/master/Pics/E-7.jpg)

We don’t perform geographical analysis this time, so we don’t deal with the missing data on user_geohash.

## 2. Clean Data

### 2.1 Remove Duplicates

![E-8](https://github.com/sichensong-99/Analysis-Projects/blob/master/Pics/E-8.jpg)

Pandas drop_duplicates() method helps in removing duplicates from the data frame. 

Keep = ‘last’: it considers last value as unique and rest of the same values as duplicate.

Inplace = True: Boolean values, removes rows with duplicates.

### 2.2 Convert time to datetime 

![E-9](https://github.com/sichensong-99/Analysis-Projects/blob/master/Pics/E-9.jpg)

### 2.3 Extract Data on data and time

![E-10](https://github.com/sichensong-99/Analysis-Projects/blob/master/Pics/E-10.jpg)

Then we could check the data on time separately. For example: 

![E-11](https://github.com/sichensong-99/Analysis-Projects/blob/master/Pics/E-11.jpg)

![E-12](https://github.com/sichensong-99/Analysis-Projects/blob/master/Pics/E-12.jpg)

### 2.4 Convert Data Type

![E-13](https://github.com/sichensong-99/Analysis-Projects/blob/master/Pics/E-13.jpg)

## 3. Analyze Web Traffic and User Behavior

Website traffic analysis refers to the statistics and analysis of relevant data in the case of obtaining the basic data of website visits, from which we can find the rules of users visiting the website, and combine these rules with network marketing strategies, so as to find the possible problems in current network marketing activities, and provide the basis for further revision or redesign of network marketing strategies. This involves the commonly used website traffic analysis indicators: PV/UV.
