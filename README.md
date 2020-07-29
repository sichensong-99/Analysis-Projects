# PROJECT: EXPLORING 67 YEARS OF LEGO
![LOGO](https://github.com/sichensong-99/My-Analysis-Projects/blob/master/LOGO.png)
## 1. Reading Data
A comprehensive database of lego blocks is provided by Rebrickable. The data is available as csv files and the schema is shown below.
![schema](https://github.com/sichensong-99/My-Analysis-Projects/blob/master/schema.png)

--Import modules

import pandas as pd

--Read colors data

colors = pd.read_csv('datasets/colors.csv')

--Print the first few rows

colors.head()

