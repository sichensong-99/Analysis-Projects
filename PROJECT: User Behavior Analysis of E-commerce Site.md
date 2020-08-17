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

Website traffic analysis refers to the statistics and analysis of relevant data in the case of obtaining the basic data of website visits, from which we can find the rules of users visiting the website, and combine these rules with network marketing strategies, so as to find the possible problems in current network marketing activities, and provide the basis for further revision or redesign of network marketing strategies. 

This involves the commonly used website traffic analysis indicators: PV/UV.

### 3.1 PV and UV Statistics

![E-14](https://github.com/sichensong-99/Analysis-Projects/blob/master/Pics/E-14.jpg)

• What is PV?

PV (page view), that is, page views, or clicks, is usually the main indicator of a website.

The expert’s explanation for PV is that a visitor actually sees several pages of your website within 24 hours (from 0 to 24). 

Here we need to emphasize: the same person browse the same page of your website, do not repeat the calculation of PV volume, point 100 is also calculated once. 

To put it bluntly, PV is a visitor who opens several of your pages.



• What is UV?

UV (unique visitor) refers to the number of different IP addresses accessing a site.

In the same day, UV only records visitors with independent IP who enter the website for the first time, but not counts those who visit the website again in the same day.

Independent IP visitors provide statistical indicators of the number of different users over a period of time, but do not reflect the overall activities of the website.

### 3.2 Daily Trend in PV and UV

![E-19](https://github.com/sichensong-99/Analysis-Projects/blob/master/Pics/E-15.jpg)

![E-20](https://github.com/sichensong-99/Analysis-Projects/blob/master/Pics/E-16.jpg)

![E-21](https://github.com/sichensong-99/Analysis-Projects/blob/master/Pics/E-17.jpg)

![E-18](https://github.com/sichensong-99/Analysis-Projects/blob/master/Pics/E-18.jpg)

![E-19](https://github.com/sichensong-99/Analysis-Projects/blob/master/Pics/E-19.jpg)

The December 12 online shopping festival (often referred to as 12/12) has routinely been the busiest shopping day of the year in China since 2012. Many stores offer highly promoted sales on 12/12, which is similar to Black Friday in the United States.

In this way, we could find out that the values of PV and UV were higher than normal level. So we’ll dig into the data on 12/12 next chapter.

### 3.3 User Behavior at Different Times

![E-20](https://github.com/sichensong-99/Analysis-Projects/blob/master/Pics/E-20.jpg)

![E-21](https://github.com/sichensong-99/Analysis-Projects/blob/master/Pics/E-21.jpg)

## 4. Promotion Campaign Data and Daily Data

Because of sales promotion campaign on December 12th, we cannot mix data in promotion campaign with daily data to conduct trend analysis. It’ll be biased and not in line with the truth. 

So we seperate data in promotion campaign from daily data and conduct comparative analysis.

### 4.1 Convert time to datatime

![E-22](https://github.com/sichensong-99/Analysis-Projects/blob/master/Pics/E-22.jpg)

### 4.2 Variance Analysis of PV and UV (Per day)

![E-23](https://github.com/sichensong-99/Analysis-Projects/blob/master/Pics/E-23.jpg)

![E-24](https://github.com/sichensong-99/Analysis-Projects/blob/master/Pics/E-24.jpg)

![E-25](https://github.com/sichensong-99/Analysis-Projects/blob/master/Pics/E-25.jpg)

![E-26](https://github.com/sichensong-99/Analysis-Projects/blob/master/Pics/E-26.jpg)

### 4.3 Extract Data in Sales Pomotion Campaign and Daily Data

![E-27](https://github.com/sichensong-99/Analysis-Projects/blob/master/Pics/E-27.jpg)

As mentioned, December 12th was the online shopping festival. 

So we extract data on the day before festival and the day after festival to dig into the business trend during promotion campaign.

### 4.4 User Behavior at different times in Promotion Campaign

![E-28](https://github.com/sichensong-99/Analysis-Projects/blob/master/Pics/E-28.jpg)

![E-29](https://github.com/sichensong-99/Analysis-Projects/blob/master/Pics/E-29.jpg)

![E-30](https://github.com/sichensong-99/Analysis-Projects/blob/master/Pics/E-30.jpg)

![E-31](https://github.com/sichensong-99/Analysis-Projects/blob/master/Pics/E-31.jpg)

![E-32](https://github.com/sichensong-99/Analysis-Projects/blob/master/Pics/E-32.jpg)

As shown in the chart, it shows daily avarage data during the sales promotion campaign. 

We could see that 24:00 was the peak time for sales promotion campaign so that users were in high cycle regaring purchase at 24:00 as well. Promotion campaign had been a major boost for user purchase. 

Click rate entered the peak period from 21:00 to 22:00. In this way, it’s important for sellers to finish improving user interface for promotion before 20:00 so that they could attract users to participate in the promotion acticity at 24:00.

### 4.5 Daily User Behavior at Different Times

![E-33](https://github.com/sichensong-99/Analysis-Projects/blob/master/Pics/E-33.jpg)

![E-34](https://github.com/sichensong-99/Analysis-Projects/blob/master/Pics/E-34.jpg)

![E-35](https://github.com/sichensong-99/Analysis-Projects/blob/master/Pics/E-35.jpg)

During daily time, the number of buyers were not changed from 10:00 to 23:00. 

The number of visitors, the number of people who add items to shopping cart and the number of people who save items were in peak time from 21:00 to 22:00. It means that users would like to browse items at night. Sellers could focus more on promotion activities during this time.

![E-36](https://github.com/sichensong-99/Analysis-Projects/blob/master/Pics/E-36.jpg)

![E-37](https://github.com/sichensong-99/Analysis-Projects/blob/master/Pics/E-37.jpg)

During daily time, the highest buying rate reached a peak from 10:00 to 15:00 and at 21:00. It’s different from the buying rate during promotion activities. 

But obviously, more peak values were shown at 21:00. In this way, sellers could focus more on marketing campaign to attract users at this time.

## 5. Conversion Funnel Analysis

### 5.1 Conversion Funnel in Sales Promotion Activity

![E-38](https://github.com/sichensong-99/Analysis-Projects/blob/master/Pics/E-38.jpg)

![E-39](https://github.com/sichensong-99/Analysis-Projects/blob/master/Pics/E-39.jpg)

During sales promotion activity, the conversion rate from clicking to adding to cart was only 4.97% and buying rate was 2%. It means that the seller got lots of page views. But few of users were willing to buy. 

Although it was the large-scale promotion campaign, the conversion rate was still low. Sellers could focus more on how to attract users to save items and to add items to shopping cart so that the buying rate would be increased.

### 5.2 Daily Conversion Funnel 

![E-40](https://github.com/sichensong-99/Analysis-Projects/blob/master/Pics/E-40.jpg)

![E-41](https://github.com/sichensong-99/Analysis-Projects/blob/master/Pics/E-41.jpg)

According to daily click rate, 4.45% of users added items to shopping cart and 3.3% of users saved items. As a result, there were only 1.4% of users buying the items. In this way, we could conclude that the conversion rate was too low and still was in grow potential.

According to color indication, red part was changed the most. It means that the conversion rate from clicking to adding to cart was minumum. 

Then we dig into the user behavior path, which refers to click - add to cart - save - purchase. Sellers could focus on the conversion rate from clicking to adding to cart in order to further improve buying rate. After adding to cart, sellers could issue more coupons to stimulate users desire to buy.

## 6. Conclusion

Data range in the project is from 2014/11/18 - 2014/12/18. 

It is a remarkable fact that we need pay more attention on data on December 12th ,which need a special treatment. 

The December 12 online shopping festival (often referred to as 12/12) has routinely been the busiest shopping day of the year in China since 2012. Many stores offer highly promoted sales on 12/12, which is similar to Black Friday in the United States. 

In order to improve the efficiency and accuracy of analysis, we divide data into 2 parts: daily and sales promotion campaign (2014/12/11 - 2014/12/13) and conduct analysis separately.

![WERCHART](https://github.com/sichensong-99/Analysis-Projects/blob/master/Pics/WeChat%20Image_20200817145456.png)
