# Time Series Analysis and Forecasting

1. Import the necessary libraries
```Python
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

from sklearn.metrics import mean_squared_error
from math import sqrt
from statsmodels.tsa.arima_model import ARIMA
```
2. Load the data, can be found [here](https://raw.githubusercontent.com/nick-singh/Time-Series-Analysis-Tutorial/master/data.csv)
3. Explore the dataset 
4. Convert the date column to datetime and set as the index
5. Plot the data for all the columns
6. Identify Trends in Time Series
7. Identify Seasonal Patterns in Time Series
8. Create a separate dataframe to hold only the gym records
9. Separate the gym dataset into training and testing data, the test data will be for the year `2017`.
```Python
train = gym[gym.index.year < 2017]
test = gym[gym.index.year == 2017]
```
10. Perform Forecasting on the gym dataset with each of the following methods:
	1. Method 1 – Start with a Naive Approach
	2. Method 2 – Simple average
	3. Method 3 – Moving average
	4. Method 4 – Single Exponential smoothing
11. Plot for each method the graph showing the actual values along with the projected  values.
12. For each of the methods keep track of the RMSE to compare the performance
