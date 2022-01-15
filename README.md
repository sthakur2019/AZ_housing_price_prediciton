#AZ MDEIAN HOUSE PRICE PREDICTION
##Business Problem
Predict the median price of home in Arizona in next 12 months based on the historic home price and other pointers available for last 10years

##Data Explanation (Data Prep/Data Dictionary)
With the real estate market drifting toward a more normalized pace, many industry experts envision the number of existing homes for sale increasing next year, especially as current homeowners look to move.
Redfin provide earliest and most reliable data on the state of the housing market. They publish existing industry data faster, and offer additional data on tours and offers that no one else has.

Below are the attributes I am getting from Redfin housing data:
Attribute name	Description
period_begin	Month start date
period_end	Month End date
period_duration	Period duration
region_type	Is region a state or city etc.
is_seasonally_adjusted	is_seasonally_adjusted
region	Region name
city	City name
state	State name
state_code	State code
property_type	Type of Property
median_sale_price	Median sale Price
median_sale_price_mom	Median sale Price month over month
median_sale_price_yoy	Median sale Price year over year
median_list_price	Median list price
median_list_price_mom	Median list price Month over month
median_list_price_yoy	Median list price  year over year
median_ppsf	Median price per squre foot
median_ppsf_mom	Median price per squre foot month over month
median_ppsf_yoy	Median price per squre foot year over year
median_list_ppsf	Medan list price per square foot
median_list_ppsf_mom	Medan list price per square foot month over month
median_list_ppsf_yoy	Medan list price per square foot year over year
homes_sold	Number of home sold
homes_sold_mom	Number of home sold month over month
homes_sold_yoy	Number of home sold year over year
pending_sales	Pending sales
pending_sales_mom	Pending sales month over month
pending_sales_yoy	Pending sales year over year
new_listings	number of  new listing
new_listings_mom	number of  new listing month over month
new_listings_yoy	number of  new listing year over year
inventory	number of inventory
inventory_mom	number of inventory month over month
inventory_yoy	number of inventoryyear over year
months_of_supply	Month of supply
months_of_supply_mom	Change in number of months in supply month over month
months_of_supply_yoy	Change in number of months in supply year over year
median_dom	median days of month in market
median_dom_mom	Median days of month in market month over month
median_dom_yoy	Median days of month in market year over year
avg_sale_to_list	average sales to list price
avg_sale_to_list_mom	Change in average sales price to list proce month over month
avg_sale_to_list_yoy	Change in average sales price to list proce year over year
sold_above_list	Fraction of houses sold over list price
sold_above_list_mom	Change in fraction of house sold over list price month over month
sold_above_list_yoy	Change in fraction of house sold over list price year over year
price_drops	Price drop
price_drops_mom	Change in Price drop month over month
price_drops_yoy	Change in Price drop year over year
off_market_in_two_weeks	Fraction of house moving off market in two weeks
off_market_in_two_weeks_mom	Change in fraction of house moving off market in two weeks month over month
off_market_in_two_weeks_yoy	Change in fraction of house moving off market in two weeks year over year
parent_metro_region	Parent metro region
parent_metro_region_metro_code	Parent metro region metro code
last_updated	Last update tiemstamp

Method used:
Facebook Prophet
ARIMA

Direction to use this code:
You can either use the dataset available in the GIT or you can use your own data.
In case you decide to get your own dataset, please ensure following:
1. The input to Prophet is always a dataframe with two columns: ds and y. 
2. The ds (datestamp) column should be of a format expected by Pandas, ideally YYYY-MM-DD for a 1. date or YYYY-MM-DD HH:MM:SS for a timestamp. 
3. The y column must be numeric, and represents the measurement we wish to forecast.

Use of Prediction adjustments:
1. In order to counter balance the sudden increase in house price in 2021, we have used a multiplier(value is 1.1). This is hard coded.
2. Please calculate or use your own multiplier for price adjustment.
3. If you don't see any deviation or unexpected trend in the prediction year, you can use 1 as multiplier.
