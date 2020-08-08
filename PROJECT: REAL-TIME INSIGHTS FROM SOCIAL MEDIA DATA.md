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

Output:
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

### Step 1: List the names in WW_trends

![twitter-task3-1](https://github.com/sichensong-99/My-Analysis-Projects/blob/master/Pics/twitter-task3-1.png)

Extract the name field, trend['name'], from the list of trends in WW_trends

Output:

![twitter-task3-1-output](https://github.com/sichensong-99/My-Analysis-Projects/blob/master/Pics/twitter-task3-1-output.png)

As shown, we already gotten the name list of WW_trends.

### Step 2: List the names in US_trend

The same for US_trend:

![twitter-task3-2](https://github.com/sichensong-99/My-Analysis-Projects/blob/master/Pics/twitter-task3-2.png)

Here's the name list of US_trend.

Output:
![twitter-task3-2-output](https://github.com/sichensong-99/My-Analysis-Projects/blob/master/Pics/twitter-task3-2-output.png)

You can just use WW_trends[0]['trends']and US_trends[0]['trends'] for iterations to get the names because the trends objects are lists with only one element.

### Step 3: Find the intersection 

After listing the name lists, we are trying to find the intersection between twO sets.

![twitter-task3-3](https://github.com/sichensong-99/My-Analysis-Projects/blob/master/Pics/twitter-task3-3.png)

Call the intersection() method on world_trends with us_trends as input parameter to get the common items between the two; store the output in the variable called common_trends.

Output:
![twitter-task3-3-output](https://github.com/sichensong-99/My-Analysis-Projects/blob/master/Pics/twitter-task3-3-output.png)

# 4. Exploring the hot trend

🕵️‍♀️ From the intersection (last output) we can see that, out of the two sets of trends (each of size 50), we have 11 overlapping topics. In particular, there is one common trend that sounds very interesting: #WeLoveTheEarth — so good to see that Twitteratis are unanimously talking about loving Mother Earth! 💚

![earth](https://github.com/sichensong-99/My-Analysis-Projects/blob/master/Pics/earth.png)

We have found a hot-trend, #WeLoveTheEarth. Now let's see what story it is screaming to tell us!
If we query Twitter's search API with this hashtag as query parameter, we get back actual tweets related to it. We have the response from the search API stored in the datasets folder as 'WeLoveTheEarth.json'. So let's load this dataset and do a deep dive in this trend.

![TWITTER-TASK4](https://github.com/sichensong-99/My-Analysis-Projects/blob/master/Pics/TWITTER-TASK4.png)

Output:
![twitter-task4-output](https://github.com/sichensong-99/My-Analysis-Projects/blob/master/Pics/TWITTER-TASK4-OUTPUT.png)

Just like in Task 1, use theopen() method with 'datasets/WeLoveTheEarth.json' as input parameter to open the file -> call the read() method on the opened file to read its content -> pass the read JSON string to the json.loads() method as input parameter for decoding it -> store the decoded output in tweets.

## 5. Digging deeper

🕵️‍♀️ Printing the first two tweet items makes us realize that there’s a lot more to a tweet than what we normally think of as a tweet — there is a lot more than just a short text!

But hey, let's not get overwhemled by all the information in a tweet object! Let's focus on a few interesting fields and see if we can find any hidden insights there.

![twitter-task5-1](https://github.com/sichensong-99/My-Analysis-Projects/blob/master/Pics/twitter-task5-1.png)

![twitter-task5-2](https://github.com/sichensong-99/My-Analysis-Projects/blob/master/Pics/twitter-task5-2.png)

For each tweet in the tweets object , extract its text field, tweet['text'], using list comprehension. Store all the ouput texts in a list called texts.
For each tweet in tweets, create an inner loop to iterate through usermentions, tweet['entities']['user_mentions']. From each user_mention extract its screenname field, user_mention['screen_name']. Store the output in names.
For each tweet in tweets, create an inner loop to iterate through hashtags, tweet['entities']['hashtags']. From each hashtag extract its text field, hashtag['text']. Store the output in hashtags.

Output:
![twitter-task5-output1](https://github.com/sichensong-99/My-Analysis-Projects/blob/master/Pics/twitter-task5-output1.png)
![twitter-task5-output2](https://github.com/sichensong-99/My-Analysis-Projects/blob/master/Pics/twitter-task5-output2.png)
![twitter-task5-output3](https://github.com/sichensong-99/My-Analysis-Projects/blob/master/Pics/twitter-task5-output3.png)






