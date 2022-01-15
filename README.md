**AZ MDEIAN HOUSE PRICE PREDICTION**

**Business Problem**
Predict the median price of home in Arizona in next 12 months based on the historic home price and other pointers available for last 10years

**Data Explanation (Data Prep/Data Dictionary)**
With the real estate market drifting toward a more normalized pace, many industry experts envision the number of existing homes for sale increasing next year, especially as current homeowners look to move.
Redfin provide earliest and most reliable data on the state of the housing market. They publish existing industry data faster, and offer additional data on tours and offers that no one else has.


**Method used:**
Facebook Prophet
ARIMA

**Direction to use this code:**
You can either use the dataset available in the GIT or you can use your own data.
In case you decide to get your own dataset, please ensure following:
1. The input to Prophet is always a dataframe with two columns: ds and y. 
2. The ds (datestamp) column should be of a format expected by Pandas, ideally YYYY-MM-DD for a 1. date or YYYY-MM-DD HH:MM:SS for a timestamp. 
3. The y column must be numeric, and represents the measurement we wish to forecast.

**Use of Prediction adjustments:**
1. In order to counter balance the sudden increase in house price in 2021, we have used a multiplier(value is 1.1). This is hard coded.
2. Please calculate or use your own multiplier for price adjustment.
3. If you don't see any deviation or unexpected trend in the prediction year, you can use 1 as multiplier.
