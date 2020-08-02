# PROJECT: The World Bank's International Debt Data
![thesis](https://github.com/sichensong-99/My-Analysis-Projects/blob/master/Pics/thesis.png)

It's not that we humans only take debts to manage our necessities. A country may also take debt to manage its economy. For example, infrastructure spending is one costly ingredient required for a country's citizens to lead comfortable lives. The World Bank is the organization that provides debt to countries.

In this project, we are going to analyze international debt data collected by The World Bank. The dataset contains information about the amount of debt (in USD) owed by developing countries across several categories. We are going to find the answers to questions like:

What is the total amount of debt that is owed by the countries listed in the dataset?

Which country owns the maximum amount of debt and what does that amount look like?

What is the average amount of debt owed by countries across different debt indicators?

## 1. Reading data

Let’s start with this one, as it will allow you to enter multi-line SQL statements. The only requirement is to make a %%sql prefix on the start. 

![dataset1](https://github.com/sichensong-99/My-Analysis-Projects/blob/master/Pics/dataset1.png)

The second line of code connects us to the international_debt database where the table international_debt is residing. Let's first SELECT all of the columns from the international_debt table. Also, we'll limit the output to the first ten rows to keep the output clean.

![dataset2](https://github.com/sichensong-99/My-Analysis-Projects/blob/master/Pics/dataset2.png)
![dataset3](https://github.com/sichensong-99/My-Analysis-Projects/blob/master/Pics/dataset3.png)

## 2. Finding the number of distinct countries

From the first ten rows, we can see the amount of debt owed by Afghanistan in the different debt indicators. But we do not know the number of different countries we have on the table. There are repetitions in the country names because a country is most likely to have debt in more than one debt indicator.

Without a count of unique countries, we will not be able to perform our statistical analyses holistically. In this section, we are going to extract the number of unique countries present in the table.

![task2](https://github.com/sichensong-99/My-Analysis-Projects/blob/master/Pics/task2.png)

![task-out](https://github.com/sichensong-99/My-Analysis-Projects/blob/master/Pics/task2-out.png)

## 3. Finding out the distinct debt indicators

We can see there are a total of 124 countries present on the table. As we saw in the first section, there is a column called indicator_name that briefly specifies the purpose of taking the debt. Just beside that column, there is another column called indicator_code which symbolizes the category of these debts. Knowing about these various debt indicators will help us to understand the areas in which a country can possibly be indebted to.

![task3](https://github.com/sichensong-99/My-Analysis-Projects/blob/master/Pics/task3.png)

![task3-out](https://github.com/sichensong-99/My-Analysis-Projects/blob/master/Pics/task3-out.png)
![task3-out2](https://github.com/sichensong-99/My-Analysis-Projects/blob/master/Pics/task3-out2.png)
![task3-out3](https://github.com/sichensong-99/My-Analysis-Projects/blob/master/Pics/task3-out3.png)

## 4. Totaling the amount of debt owed by the countries

As mentioned earlier, the financial debt of a particular country represents its economic state. But if we were to project this on an overall global scale, how will we approach it?

Let's switch gears from the debt indicators now and find out the total amount of debt (in USD) that is owed by the different countries. This will give us a sense of how the overall economy of the entire world is holding up.

![task4](https://github.com/sichensong-99/My-Analysis-Projects/blob/master/Pics/task4.png)

![task4-out](https://github.com/sichensong-99/My-Analysis-Projects/blob/master/Pics/task4-out.png)

## 5. Country with the highest debt

"Human beings cannot comprehend very large or very small numbers. It would be useful for us to acknowledge that fact." - Daniel Kahneman. That is more than 3 million million USD, an amount which is really hard for us to fathom.

Now that we have the exact total of the amounts of debt owed by several countries, let's now find out the country that owns the highest amount of debt along with the amount. Note that this debt is the sum of different debts owed by a country across several categories. This will help to understand more about the country in terms of its socio-economic scenarios. We can also find out the category in which the country owns its highest debt. But we will leave that for now.

![task5](https://github.com/sichensong-99/My-Analysis-Projects/blob/master/Pics/task5.png)

![task5-out](https://github.com/sichensong-99/My-Analysis-Projects/blob/master/Pics/task5-out.png)

## 6. Average amount of debt across indicators

We now have a brief overview of the dataset and a few of its summary statistics. We already have an idea of the different debt indicators in which the countries owe their debts. We can dig even further to find out on an average how much debt a country owes? This will give us a better sense of the distribution of the amount of debt across different indicators.

![task6](https://github.com/sichensong-99/My-Analysis-Projects/blob/master/Pics/task6.png)

![task6-out](https://github.com/sichensong-99/My-Analysis-Projects/blob/master/Pics/task6-out.png)

## 7. The highest amount of principal repayments

An interesting observation in the above finding is that there is a huge difference in the amounts of the indicators after the second one. This indicates that the first two indicators might be the most severe categories in which the countries owe their debts.

We can investigate this a bit more so as to find out which country owes the highest amount of debt in the category of long term debts (DT.AMT.DLXF.CD). Since not all the countries suffer from the same kind of economic disturbances, this finding will allow us to understand that particular country's economic condition a bit more specifically.

![task7](https://github.com/sichensong-99/My-Analysis-Projects/blob/master/Pics/task7.png)

![task7-out](https://github.com/sichensong-99/My-Analysis-Projects/blob/master/Pics/task7-out.png)

## 8. The most common debt indicator

China has the highest amount of debt in the long-term debt (DT.AMT.DLXF.CD) category. This is verified by The World Bank. It is often a good idea to verify our analyses like this since it validates that our investigations are correct.

We saw that long-term debt is the topmost category when it comes to the average amount of debt. But is it the most common indicator in which the countries owe their debt? Let's find that out.

![task8](https://github.com/sichensong-99/My-Analysis-Projects/blob/master/Pics/task8.png)

![task8-out](https://github.com/sichensong-99/My-Analysis-Projects/blob/master/Pics/task8-out.png)
![task8-out2](https://github.com/sichensong-99/My-Analysis-Projects/blob/master/Pics/task8-out2.png)

## 9. Other viable debt issues and conclusion

There are a total of six debt indicators in which all the countries listed in our dataset have taken debt. The indicator DT.AMT.DLXF.CD is also there in the list. So, this gives us a clue that all these countries are suffering from a common economic issue. But that is not the end of the story, a part of the story rather.

Let's change tracks from debt_indicators now and focus on the amount of debt again. Let's find out the maximum amount of debt across the indicators along with the respective country names. With this, we will be in a position to identify the other plausible economic issues a country might be going through. By the end of this section, we will have found out the debt indicators in which a country owes its highest debt.

In this notebook, we took a look at debt owed by countries across the globe. We extracted a few summary statistics from the data and unraveled some interesting facts and figures. We also validated our findings to make sure the investigations are correct.

![task9](https://github.com/sichensong-99/My-Analysis-Projects/blob/master/Pics/task9.png)

![task9-out](https://github.com/sichensong-99/My-Analysis-Projects/blob/master/Pics/task9-out.png)



