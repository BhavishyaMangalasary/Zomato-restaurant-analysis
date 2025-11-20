# Zomato-restaurant-analysis

## Overview
This project performs an end-to-end exploratory data analysis (EDA) on Zomato restaurant data to answer critical business questions:
  * What factors influence restaurant ratings?
  * How do dining and delivery experiences compare?
  * What makes menu items bestsellers?
  * Which cuisines and cities offer the best value?
  * How should restaurants optimize their pricing strategy?
The analysis reveals actionable insights for restaurant owners, food delivery platforms, and customers looking for the best dining experiences.

## Key Insights
  * 50,000+ menu items analyzed
  * 800+ unique restaurants
  * 17 cities covered
  * 40+ cuisine styles covered
  * 25+ comprehensive visualizations

## Dataset
### Source
  * Platform : Kaggle ( Zomato Restaurant Dataset : https://www.kaggle.com/datasets/gauravkumar2525/zomato-restaurant-dataset )
  * Size : 123,657 rows, 26 columns
  * Format : CSV

### Key Features
  0 Restaurant_Name           Name of the restaurant listed on Zomato.
  1 Dining_Rating             User rating for the dine-in experience (0.0 to 5.0).
         2   Delivery_Rating           User rating for the delivery experience (0.0 to 5.0)
         3   Dining_Votes              Number of votes received for dine-in service.
         4   Delivery_Votes            Number of votes received for delivery service
         5   Cuisine                   Type of cuisine served
         6   Place_Name                Local area or neighborhood of the restauran
         7   City                      City in which the restaurant is located
         8   Item_Name                 Name of the menu item listed.
         9   Best_Seller               Bestseller status
         10  Votes                     Combined total votes received.
         11  Prices                    Price of the menu item in INR.
         12  Average_Rating            Mean rating calculated from available sources.
         13  Total_Votes               Sum of all types of votes.
         14  Price_per_Vote            Ratio of price to total votes
         15  Log_Price                 Log-transformed price to reduce skewness in analysis.
         16  Is_Bestseller             Binary flag indicating if item is marked as a bestseller.
         17  Restaurant_Popularity     Number of items listed by the restaurant in the dataset.
         18  Avg_Rating_Restaurant     Average rating of all items from the same restaurant.
         19  Avg_Price_Restaurant      Average price of all items from the same restaura
         20  Avg_Rating_Cuisine        Average rating across all restaurants serving the same cuisine.
         21  Avg_Price_Cuisine         Average price across all restaurants serving the same cuisine.
         22  Avg_Rating_City           Average rating across all restaurants in the same city.
         23  Avg_Price_City            Average price of menu items in the same city.
         24  Is_Highly_Rated           Binary flag for ratings ≥ 4.0.
         25  Is_Expensive              Binary flag for prices above city’s average.
