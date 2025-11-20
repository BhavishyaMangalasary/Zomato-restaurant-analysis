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
  1. Restaurant_Name           Name of the restaurant listed on Zomato.
  2. Dining_Rating             User rating for the dine-in experience (0.0 to 5.0).
  3. Delivery_Rating           User rating for the delivery experience (0.0 to 5.0)
  4. Dining_Votes              Number of votes received for dine-in service.
  5. Delivery_Votes            Number of votes received for delivery service
  6. Cuisine                   Type of cuisine served
  7. Place_Name                Local area or neighborhood of the restauran
  8. City                      City in which the restaurant is located
  9. Item_Name                 Name of the menu item listed.
  10. Best_Seller               Bestseller status
  11. Votes                     Combined total votes received.
  12. Prices                    Price of the menu item in INR.
  13. Average_Rating            Mean rating calculated from available sources.
  14. Total_Votes               Sum of all types of votes.
  15. Price_per_Vote            Ratio of price to total votes
  16. Log_Price                 Log-transformed price to reduce skewness in analysis.
  17. Is_Bestseller             Binary flag indicating if item is marked as a bestseller.
  18. Restaurant_Popularity     Number of items listed by the restaurant in the dataset.
  19. Avg_Rating_Restaurant     Average rating of all items from the same restaurant.
  20. Avg_Price_Restaurant      Average price of all items from the same restaura
  21. Avg_Rating_Cuisine        Average rating across all restaurants serving the same cuisine.
  22. Avg_Price_Cuisine         Average price across all restaurants serving the same cuisine.
  23. Avg_Rating_City           Average rating across all restaurants in the same city.
  24. Avg_Price_City            Average price of menu items in the same city.
  25. Is_Highly_Rated           Binary flag for ratings ≥ 4.0.
  26. Is_Expensive              Binary flag for prices above city’s average.

## Project Structure
```
zomato-restaurant-analysis/
|
├── README.MD
|
├── images/
|    ├── Rating_analysis.png
|    ├── Price_analysis.png
|    ├── Category_analysis.png
|    ├── Delivery_vs_Dining.png
|    ├── Price_vs_Rating.png
|    ├── Cuisine_analysis.png
|    ├── Geographic_analysis.png
|    ├── Restaurant_analysis.png
|    ├── Value_segmentation.png
|    ├──Bestseller_patterns.png
|
└── restaurant.ipynb
```

## Technologies Used

### Core Libraries
- **Python 3.8** - Programming language
- **Pandas 2.3.2** - Data manipulation and analysis
- **NumPy 2.3.3** - Numerical computing
- **Matplotlib 3.10.6+** - Data visualization
- **Seaborn 0.13.2** - Statistical visualizations
- **SciPy 1.16.3** - Statistical testing

### Analysis Techniques
- Exploratory Data Analysis (EDA)
- Statistical hypothesis testing (t-tests)
- Correlation analysis
- Segmentation analysis
- Distribution analysis

## Analysis Sections

The project is structured into 12 comprehensive sections:

### Section 1: Data Foundation
- Load and explore dataset
- Data quality checks
- Missing value analysis
- Data cleaning and preparation

### Section 2: Rating Analysis
- Distribution of dining, delivery, and average ratings
- Statistical measures (mean, median, mode, std)
- Skewness analysis
- Outlier detection

### Section 3: Price Analysis
- Price distribution and percentiles
- Skewness identification
- Price range segmentation
- Outlier analysis

### Section 4: Categorical Breakdown
- Top cities by item count
- Most common cuisines
- Bestseller vs regular item distribution

### Section 5: Dining vs Delivery Comparison
- Rating correlation analysis
- Service quality gaps
- Statistical significance testing
- Restaurant-specific performance

### Section 6: Price-Rating Relationship
- Correlation analysis
- Scatter plot visualization
- Price range performance
- Value assessment

### Section 7: Cuisine Deep Dive
- Top-rated cuisines (with minimum vote filter)
- Most expensive cuisines
- Bestseller ratios by cuisine
- Cuisine characteristics

### Section 8: Geographic Analysis
- Top-rated cities
- Most expensive cities
- Restaurant density by location
- City-level price-quality analysis

### Section 9: Restaurant Performance
- Top restaurants by rating
- Menu size optimization
- Bestseller concentration
- Restaurant strategies

### Section 10: Value Segmentation
- 4-quadrant analysis (Premium, Great Value, Overpriced, Budget)
- Median-based segmentation
- Segment characteristics
- Value identification

### Section 11: Bestseller Pattern Analysis
- Characteristic comparison (ratings, prices, votes)
- Statistical significance testing
- Success factor identification
- Pattern recognition

### Section 12: Executive Summary
- Key findings synthesis
- Business recommendations
- Strategic insights
- Actionable takeaways

## Findings & Recommendations

### **FINDING #1: The Delivery Advantage** 

**Data:**
- Delivery ratings: 3.96
- Dining ratings: 3.82
- Gap: +0.14 (delivery higher)
- Correlation: 0.257 (weak)

**Insight:**
Opposite of typical patterns. Restaurants have optimized for delivery better than dine-in, or platform attracts delivery-focused establishments.

**Recommendations:**
 * **For Restaurants:** Maintain delivery excellence; invest in packaging, temperature control
 * **For Platforms:** Market "Optimized for Delivery" as competitive advantage
 * **For Customers:** Trust delivery ratings on this platform

---

### **FINDING #2: Price-Quality Independence** 💰

**Data:**
```
₹0-100:    3.86 rating (19,925 items)
₹100-200:  3.87 rating (41,175 items)
₹200-300:  3.91 rating (33,801 items)
₹300-500:  3.92 rating (21,739 items)
₹500-1000: 3.95 rating (6,039 items)
₹1000+:    3.90 rating (978 items)

Range: Only 0.09 points across 10x price difference
```

**Insight:**
Price has minimal predictive power for quality. A ₹100 item rates nearly as high as ₹1,000 item.

**Recommendations:**
 * **For Restaurants:** Compete on execution, not premium pricing
 * **For Platforms:** Highlight "Great Value" segment (high rating, low price)
 * **For Customers:** Don't assume expensive = better quality

---

### **FINDING #3: Market Concentration in Mid-Range** 📊

**Data:**
```
Price Distribution:
₹100-200:  33.3% ← Largest segment
₹200-300:  27.3% ← 2nd largest
₹300-500:  17.6%

Cumulative ₹100-500: 77% of market
Premium ₹500+: Only 5.7%
```

**Insight:**
Market dominated by affordable to mid-range pricing. Premium is niche.

**Recommendations:**
 * **For Restaurants:** Target ₹100-300 to access 60% of market
 * **For Platforms:** Optimize discovery for mid-range segment
 * **For Investors:** Volume opportunity in ₹100-300 range

---

### **FINDING #4: Cuisine Quality-Volume Trade-off** 🍽️

**Data:**
```
Quality Leaders:
Bakery:      4.15 (659 items,  ₹268)
Turkish:     4.10 (22 items,   ₹244)
Salad:       4.06 (75 items,   ₹270)

Volume Leaders:
Beverages:   3.93 (39,441 items - 31.9%!)
Pizza:       --- (15,044 items - 12.2%)
Desserts:    3.94 (11,773 items - 9.5%)

Best Balance:
North Indian: 4.01 (2,086 items, ₹196)
```

**Insight:**
Can't optimize for all three (rating, volume, price). North Indian achieves best balance.

**Recommendations:**
 * **For New Entrants:** Choose lane: Quality (Bakery, Turkish) vs Volume (Beverages, Pizza)
 * **For Established:** North Indian model offers sustainable growth
 * **For Investors:** Niche cuisines (Turkish, Salad) offer differentiation

---

### **FINDING #5: Geographic Value Arbitrage** 📍

**Data:**
```
Value Champions:
Malleshwaram: 4.00 rating, ₹197 avg
Jaipur:       3.90 rating, ₹205 avg
Hyderabad:    3.92 rating, ₹236 avg

Premium Markets:
Mumbai:       3.88 rating, ₹293 avg (+48% vs Malleshwaram!)
Chennai:      3.90 rating, ₹262 avg (+33% vs Malleshwaram)

Key: Mumbai charges 48% more for 0.12 LOWER rating
```

**Insight:**
Geography determines pricing power, not quality. Tier-2 cities offer better value.

**Recommendations:**
 * **For Expansion:** Prioritize Jaipur, Lucknow, Hyderabad (better economics)
 * **For Metro Operations:** Justify premium through brand, not quality alone
 * **For Customers:** Explore tier-2 cities for better value

---

### **FINDING #6: Restaurant Scale Strategies** 🏆

**Data:**
```
Top Independents (Rating 4.30-4.45):
- Menu size: 34-387 items
- Sweet spot: 100-200 items (9 of top 20)

Chains (100% Bestseller Status):
- McDonald's: 1,493 items
- Burger King: 1,352 items
- Domino's: 885 items
```

**Insight:**
Quality peaks at 100-200 items. Chains win on volume/marketing, not ratings.

**Recommendations:**
 * **For Independents:** Target 100-200 items for quality leadership
 * **For Chains:** Leverage brand + volume; ratings aren't your advantage
 * **For Startups:** Start with 50-100 items, grow to 100-200

---

### **FINDING #7: Value Segmentation Opportunities** 💎

**Data:**
```
Premium:      27.9% (4.08 rating, ₹351)
Great Value:  22.4% (4.06 rating, ₹124) ← Same rating, 65% cheaper!
Overpriced:   23.4% (3.70 rating, ₹334) ← Problem
Budget:       26.3% (3.70 rating, ₹123)
```

**Insight:**
22% of market achieves premium ratings at budget prices. 23% is overpriced.

**Recommendations:**
 * **For Platforms:** Create "Great Value" discovery feature
 * **For Restaurants:** Move from "Overpriced" to "Premium" (improve quality) or "Great Value" (reduce price)
 * **For Customers:** Actively seek "Great Value" segment (4.0+ rating, <₹150)

---

### **FINDING #8: Success-Only Dataset** 🎯

**Data:**
```
After 50+ vote filter:
- 100% bestsellers (82,091 items)
- 0% regular items
- Avg: 3.89 rating, ₹236 price, 400 votes
```

**Insight:**
Dataset shows only survivors (survivorship bias). Represents proven success formulas.

**Success Benchmarks Identified:**
 * **Minimum:** 3.0 rating (nothing below survives)
 * **Competitive:** 3.9 rating (dataset average)
 * **Excellence:** 4.0+ rating (top quartile)
 * **Engagement:** 400+ votes (established presence)

---
