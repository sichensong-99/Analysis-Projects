# PROJECT: EXPLORING 67 YEARS OF LEGO
![LOGO](https://github.com/sichensong-99/My-Analysis-Projects/blob/master/Pics/LOGO.png)
## 1. Reading Data
A comprehensive database of lego blocks is provided by Rebrickable. The data is available as csv files and the schema is shown below.
![schema](https://github.com/sichensong-99/My-Analysis-Projects/blob/master/Pics/schema.png)

Import modules

### import pandas as pd

Read colors data

### colors = pd.read_csv('datasets/colors.csv')

Print the first few rows

### colors.head()




The head() function returns the first n rows for the object based on position. It is useful for quickly testing if your object has the right type of data in it.


![read_data_output](https://github.com/sichensong-99/My-Analysis-Projects/blob/master/Pics/read_data_output.png)

## 2.Exploring Colors

How many distinct colors are available?

### num_colors = colors.rgb.size

### print('Number of distinct colors:', num_colors)


### Out[]:Number of distinct colors: 135




As shown above, rgb is one of columns in the colors table. We use the size function here to count the number of elements along a given axis. Why don't use shape() here? Let's pay attention on the difference between size() and shape(). 

### Here's the examples:

size() function count the number of elements along a given axis. Parameters: arr: [array_like] Input data.

![size](https://github.com/sichensong-99/My-Analysis-Projects/blob/master/Pics/size().png)

The function "shape" returns the shape of an array. The shape is a tuple of integers. These numbers denote the lengths of the corresponding array dimension. In other words: The "shape" of an array is a tuple with the number of elements per axis (dimension).

![shape](https://github.com/sichensong-99/My-Analysis-Projects/blob/master/Pics/shape().png)

## 3.Transparent Colors in Lego Sets

The colors data has a column named is_trans that indicates whether a color is transparent or not. It would be interesting to explore the distribution of transparent vs. non-transparent colors.

colors_summary: Distribution of colors based on transparency

Summarize colors based on whether they are transparent or not?

### colors_summary = colors.groupby('is_trans', as_index = True).count()
### colors_summary

![transparent](https://github.com/sichensong-99/My-Analysis-Projects/blob/master/Pics/transparent.png)

We show the dataset using pivot table. In this way, we use count() function here to calculate value of each category. When as_index=True the key(s) you use in groupby() will become an index in the new dataframe. What's the difference between as_index=True and as_index=False?

### Take a look:

![as_index1](https://github.com/sichensong-99/My-Analysis-Projects/blob/master/Pics/as_index1.png)

![as_index2](https://github.com/sichensong-99/My-Analysis-Projects/blob/master/Pics/as_index2.png)

## 4.Explore Lego Sets
Another interesting dataset available in this database is the sets data. It contains a comprehensive list of sets over the years and the number of parts that each of these sets contained.

![theme_dataset](https://github.com/sichensong-99/My-Analysis-Projects/blob/master/Pics/theme-dataset.png)

### %matplotlib inline
Read sets data as `sets`
### sets=pd.read_csv('datasets/sets.csv')
Create a summary of average number of parts by year: `parts_by_year`
### parts_by_year = sets[['year', 'num_parts']].groupby('year', as_index = False).mean()
Plot trends in average number of parts by year
### sets.plot(x='year', y='num_parts')
### parts_by_year.head()

Note: “%matplotlib inline” will lead to static images of your plot embedded in the notebook.

![matplot1](https://github.com/sichensong-99/My-Analysis-Projects/blob/master/Pics/matplot1.png)
![matplot2](https://github.com/sichensong-99/My-Analysis-Projects/blob/master/Pics/matplot2.png)

## 5.Lego Themes Over Years
Lego blocks ship under multiple themes. Let us try to get a sense of how the number of themes shipped has varied over the years.

themes_by_year: Number of themes shipped by year
### themes_by_year = sets[['year', 'theme_id']].groupby('year', as_index = False).agg({'theme_id': pd.Series.nunique})
### themes_by_year.head()

![over_year](https://github.com/sichensong-99/My-Analysis-Projects/blob/master/Pics/over_year.png)

Series is a one-dimensional labeled array capable of holding data of any type (integer, string, float, python objects, etc.). The axis labels are collectively called index.

nunique() function return Series with number of distinct observations over requested axis. If we set the value of axis to be 0, then it finds the total number of unique observations over the index axis. If we set the value of axis to be 1, then it find the total number of unique observations over the column axis.

In the table above, it shows the theme_id and year. But We need to figure out the number of each theme id. It means that we count the number of one of columns in table, so we use agg() function here.
