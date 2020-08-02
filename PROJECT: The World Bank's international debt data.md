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



