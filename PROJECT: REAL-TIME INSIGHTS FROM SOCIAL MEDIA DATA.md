# PROJECT: REAL-TIME INSIGHTS FROM SOCIAL MEDIA DATA

## 1. Load data

![twitter](https://github.com/sichensong-99/My-Analysis-Projects/blob/master/Pics/Twitter.png)

Twitter provides both global and local trends. Let's load and inspect data for topics that were hot worldwide (WW) and in the United States (US) at the moment of query — snapshot of JSON response from the call to Twitter's GET trends/place API.

![twitter-task1](https://github.com/sichensong-99/My-Analysis-Projects/blob/master/Pics/twitter-task1.png)

In this case, we load data from JSON file, so use open() method to open the JSON file. 

And then call the read() method on the opened file to read its content;

json.loads() is for turning JSON encoded data into Python objects. The result will be a Python dictionary.


Output:

![twitter-task1-output](https://github.com/sichensong-99/My-Analysis-Projects/blob/master/Pics/twitter-task1-output.png)

## 2. Prettifying the output

Our data was hard to read! Luckily, we can resort to the json.dumps() method to have it formatted as a pretty JSON string.

![twitter-task2](https://github.com/sichensong-99/My-Analysis-Projects/blob/master/Pics/twitter-task2.png)

json.dumps() formats data as a JSON string. If you pass 'indent' to the method (a positive integer), then all the elements in the JSON array are printed with that indent level. This makes it easy to read the results — pretty-printed.

![twitter-task2-output](https://github.com/sichensong-99/My-Analysis-Projects/blob/master/Pics/twitter-task2-output.png)

## 3. Finding common trends

Now, we already finished uploading the data. Next, we'll try to discover insights from the data.

🕵️‍♀️ From the pretty-printed results (output of the previous task), we can observe that:

a. We have an array of trend objects having: the name of the trending topic, the query parameter that can be used to search for the topic on Twitter-Search, the search URL and the volume of tweets for the last 24 hours, if available. (The trends get updated every 5 mins.)

b. At query time #BeratKandili, #GoodFriday and #WeLoveTheEarth were trending WW.

c. "tweet_volume" tell us that #WeLoveTheEarth was the most popular among the three.

d. Results are not sorted by "tweet_volume".

e. There are some trends which are unique to the US.

It’s easy to skim through the two sets of trends and spot common trends, but let's not do "manual" work. We can use Python’s set data structure to find common trends — we can iterate through the two trends objects, cast the lists of names to sets, and call the intersection method to get the common names between the two sets.

![twitter-task3-1](https://github.com/sichensong-99/My-Analysis-Projects/blob/master/Pics/twitter-task3-1.png)

Extract the name field, trend['name'], from the list of trends in WW_trends

Output:
![twitter-task3-1-output](https://github.com/sichensong-99/My-Analysis-Projects/blob/master/Pics/twitter-task3-1-output.png)

As shown, we already gotten the name list of WW_trends.

The same for US_trend:

![twitter-task3-2](https://github.com/sichensong-99/My-Analysis-Projects/blob/master/Pics/twitter-task3-2.png)

Here's the name list of US_trend.

Output:
![twitter-task3-2-output](https://github.com/sichensong-99/My-Analysis-Projects/blob/master/Pics/twitter-task3-2-output.png)

You can just use WW_trends[0]['trends']and US_trends[0]['trends'] for iterations to get the names because the trends objects are lists with only one element.

Call the intersection() method on world_trends with us_trends as input parameter to get the common items between the two; store the output in the variable called common_trends.






