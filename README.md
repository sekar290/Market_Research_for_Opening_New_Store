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
2. How is the average  amount of  purchases are per store in a given city?
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
 ![GitHub Logo](/images/logo.png)
 
</details>

