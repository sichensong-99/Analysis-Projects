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





