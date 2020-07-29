# PROJECT: EXPLORING 67 YEARS OF LEGO
![LOGO](https://github.com/sichensong-99/My-Analysis-Projects/blob/master/Pics/LOGO.png)
## 1. Reading Data
A comprehensive database of lego blocks is provided by Rebrickable. The data is available as csv files and the schema is shown below.
![schema](https://github.com/sichensong-99/My-Analysis-Projects/blob/master/Pics/schema.png)

#### Import modules

import pandas as pd

#### Read colors data

colors = pd.read_csv('datasets/colors.csv')

#### Print the first few rows

colors.head()

The head() function returns the first n rows for the object based on position. It is useful for quickly testing if your object has the right type of data in it.


![read_data_output](https://github.com/sichensong-99/My-Analysis-Projects/blob/master/Pics/read_data_output.png)

## 2.Exploring Colors

#### How many distinct colors are available?

num_colors = colors.rgb.size

print('Number of distinct colors:', num_colors)


#### Out[]:

#### Number of distinct colors: 135

As shown above, rgb is one of columns in the colors table. We use the size function here to count the number of elements along a given axis.

