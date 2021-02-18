# Market_Research_for_Opening_New_Store
Market research for opening new store in Iowa State using public dataset of Iowa Liquor Retail Sales

### Iowa Liquor Retail Sales
This dataset contains every wholesale purchase of liquor in the State of Iowa by retailers for sale to individuals. The State of Iowa controls the  wholesale distribution of liquor intended for retail sale, which means this  dataset offers a complete view of retail liquor sales in the entire state. The  dataset contains every wholesale order of liquor by all grocery stores,  liquor stores, convenience stores, etc., with details about the store and  location, the exact liquor brand and size, and the number of bottles  ordered.
This Dataset could be access through Google BigQuery [here](https://console.cloud.google.com/marketplace/product/iowa-department-of-commerce/iowa-liquor-sales?filter=category:analytics&filter=price:free&filter=solution-type:dataset&authuser=1&project=groovy-legacy-304712&folder=&organizationId=)

### Problem Statement
Opening a new store could becoming one of  lifelong dream for many. But, opening new store  doesn't come without risk. This risk should  become concern to prevent from lost.
Location is the important one when it come to  business. The best location for the product is the  one that match with the people needed. So,  figuring out the potential location will help the  store settle well.

### Goals
1. Exsploratory Data Analysis (EDA) of the features 
2. Recommend potential location to business owner for opening new store

### LIMITATION
This limitation is used for better focus analysis :
1. Filtering data based on  'Polk' county because it has  highest number of liquor  bottles sold
2. Using the newest year (2018-2019) because it  more represent the new  condition in Iowa State

### Some Business Question
1. Which city in Polk  that have high liquor bottles sold ?
2. How is daily bottle sold of liquor?
3. How is location  affecting the sold  bottles in city?
4. Where potential location to open  new store?

### Workflow of The Analysis
1.	Sample Data from Google BigQuery using SQL
2.	Data Cleaning
    This Data Cleaning Includes below:
      - Dropping and Imputasi missing value
      - Checking Outlier
      - Checking for double transaction
      - Cleaning for store_location feature
3.	Feature Engineering
      1)	Binning in feature bottle_volume_ml into four group:
          -	small volume
          -	medium volume
          -	large volume 
          -	very large volume
          This binning based on this source: https://en.wikipedia.org/wiki/Alcohol_measurements
      2)	Create delta_cost between 'state_bottle_cost' and 'state_bottle_retail' to know the revenue for each bottle
      3)	Converting date feature to year, week and day
      4)	Binning Bottles sold into low and high sold
4.	Data Analysis and Visualization
5.	Conclusion and Recommendation

<details>
  <summary>Data Analysis and Visualization</summary>
  
 #### Which city in Polk that have high liquor bottles sold ?
 ![images](/Images/city.png)
 **Des Moines** have high total bottles sold. This one due to high population around 215,636 (2019) and wide area 234.8 km² 
 
 #### How is daily bottle sold of liquor?
 ![images](/Images/daily_sold.png)
 - From the heatmap it shows that for all months in **Saturday and Sunday**, mostly there wasn't bottles sold
 - In fact, **Thursday** have highest bottles sold for all over month especially in **March, May and August**
 
 #### How is location  affecting the sold  bottles in city?
 ![images](/Images/map.png)
 - City around the capital city (Des Moines) seem have high bottle sold.
 - Ankeny is City that has highest sold bottle of liquor around 7046

 #### Where potential location to open  new store?
 ![images](/Images/recomend_city.png)
 **Ankeny** is City that located in near of capital and have high demand 
 </details>
 
<details> 
    <summary>Conclusin and Recommendation</summary>
    
#### Gereral Conclusion
1. **American Vodkas** have high bottles sold reach 2 million, followed by Whiskey Liqueur with bottle sold reach 1 million.
2. **Single Malt Scotch** have expensive median price reach 44.99 usd.
3. **Diageo Americas**  is vendor name that have high bottles sold reach more than 1.5 million
4. **Fetzer Vineyards** is vendor name that have high median price reach 69.96 usd
5. Store tend to buy **Large Volume** with total transactions reach 400.000
6. The price of varian bottle volume linier with the volume. **The large the volume, the high the price**
7. Total cost of liquor order is fluctuative for every month. The highest one is in **October**

#### Potential Location to Open Store
1. **Windsor Heights** is City with high median amount that store should pay. So, opening new store in this location would need fund more.
2. **American Vodkas** is category name of liquor that popular and have high demand
3. City that have high bottles sold is **Ankeny**. This city located near the capital of Iowa state.

#### Recommendation for Alcoholic Beverages Divison
1. **American Vodkas** is category name of liquor that have high demand, so there must always be a supply. The division could use vendor name Diageo Americas to supply it.  
2. Since **Thursday** is day that have highest bottles sold for all over month especially in **March, May and August** so in this day and month, the division could stock more liquor to prevent from shortage of stock

#### Recommendation for Opening New Store
1. Since **Windsor Heights**  is city with high median  amount purchases for store, also the population itself lower than other city so opening new store in this city isn’t recommend
2. Recommend City to opening New Store is **Ankeny**, here are the reason:
    - Ankeny is city with highest sold bottle of liquor around 7046, 
    - For the population itself, Ankeny have high population around 61,938 (2019)
    - Ankeny located near the capital of Iowa State, so it have high demand
   
</details>
