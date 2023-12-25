# Exploratory-Data-Analysis-on-Online-Retail - Python
Performing exploratory data analysis of the features of the Unicorn Companies dataset to draw insights and provide recommendations to help Unicorn Companies create good business models and make decisions that will lead companies with high growth potential, diversify investment portfolios, and prioritize companies with experienced leadership teams.

# Investigation Overview
Perform customer behavioral analysis to enhance customer retention and satisfaction of online retail, geared toward business improvement.

# Data Overview

The data feature includes InvoiceNo, StockCode,	Description	Quantity, InvoiceDate, UnitPric, CustomerID, Country.

# Data Preparation
Let's import all  necessary libraries
import numpy as np
import pandas as pd

for visuals
import matplotlib.pyplot as plt
import seaborn as sns

# Import and read file
df = pd.read_csv(r"C:\Users\LENOVO\Desktop\OnlineRetail.csv",encoding='ISO-8859-1') 
df
df. shape

![image](https://github.com/Jawah1/Exploratory-Data-Analysis-on-Online-Retail/assets/131864852/32b9ece8-8fc3-4309-9027-1687e8f0496f)

Now let's look at the size of our data 
shape of data
df.shape

(541909, 8)

Checking for missing values
df.isnull().sum()

InvoiceNo           0
StockCode           0
Description      1454
Quantity            0
InvoiceDate         0
UnitPrice           0
CustomerID     135080
Country             0
dtype: int64

# Data Cleaning/Wrangling

Here is a summary of the cleaning process

We will handle the missing values for Description and CustomerID by using the imputing with mode method to replace the null values in description, and replace the null values with unknown, respectively.

We will replace negative values in UnitPrice with 0, and replace the negative values in Quantity with the weighted median of Quantity.

We will create an additional column called Sales by multiplying the UnitPrice by Quantity

We will convert the InvoiceDate to a datetime data type

We will convert the CustomerID from float to object/string data type

We will replace the Country RSA and EIRE with South Africa and Ireland, respectively

# Univariate Analysis
Considering the distribution of a variable or feature and its visualization

statistical summary of the data
df.describe()

![image](https://github.com/Jawah1/Exploratory-Data-Analysis-on-Online-Retail/assets/131864852/cb530902-1ad3-449a-bad7-ddf6511052d6)

# Top 5 customers with the most purchases
top5_customer = df['CustomerID'].value_counts().head()
top5_customer

# Top 10 Countries with the most/highest purchases
top10_countries = df['Country'].value_counts().head(10)
top10_countries

![image](https://github.com/Jawah1/Exploratory-Data-Analysis-on-Online-Retail/assets/131864852/ffc2a3a3-ef4e-4a03-985b-92dacbe2bc8d)

# Time of Day Purchases
time_of_purchases = df['TimeOfDay'].value_counts()
time_of_purchases

![image](https://github.com/Jawah1/Exploratory-Data-Analysis-on-Online-Retail/assets/131864852/545958b7-ac27-4caf-9937-241f6d76fd46)

# Top5 Customers

![image](https://github.com/Jawah1/Exploratory-Data-Analysis-on-Online-Retail/assets/131864852/c5cfe268-5427-49b2-809b-c7d549d2b88b)
