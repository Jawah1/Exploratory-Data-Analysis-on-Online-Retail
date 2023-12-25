# Exploratory-Data-Analysis-on-Online-Retail
Performing exploratory data analysis of the features of the Unicorn Companies dataset to draw insights and provide recommendations to help Unicorn Companies create good business models and make decisions that will lead companies with high growth potential, diversify investment portfolios, and prioritize companies with experienced leadership teams.

# Problem Statement
Perform customer behavioural analysis to enhance customer retention and satisfaction of the online retail, geared toward business improvement.
#Data Preprocessing/Wrangling
We will handle the missing values for Description and CustomerID by using the imputing with mode method to replace the null values in description, and replace the null values with unknown, respectively.

We will replace negative values in UnitPrice with 0, and replace the negative values in Quantity with the weighted median of Quantity.

We will create additional column called Sales by multiplying the UnitPrice by Quantity

We will convert the InvoiceDate to a datetime data type

We will convert the CustomerID from float to object/string data type

We will replace the Country RSA and EIRE with South Africa and Ireland, respectively.

