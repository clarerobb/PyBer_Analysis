
# PyBer Data Visualizations with Matplotlib 

## Overview
This analysis is for PyBer, a ride-sharing app, to summarize and visualize fares based on the city types (urban, suburban, rural) to determine trends and provide PyBer leadership with necessary information about the company's footprint. 

## Data
- city_data.csv
- ride_data.csv

## Method
After merging the data sources, I ran the code below to calculate PyBer summary by city type. I then resampled the data to display weekly fares by city type.

~~~~
total_rides = pyber_data_df.groupby(['type']).count()['ride_id']
total_drivers = city_data_df.groupby(['type']).sum()['driver_count']
total_fares = pyber_data_df.groupby(['type']).sum()['fare']
average_fare_per_ride = total_fares/total_rides
average_fare_per_driver = total_fares/total_drivers
~~~~

## Results
Between January 2019 and May 2019, 68.4% of PyBer's rides and 80.9% of drivers were in urban areas. Additionally, over 62.7% of PyBer's fares were collected in urban cities. <br>
![Screen Shot 2022-07-09 at 3 32 01 PM](https://user-images.githubusercontent.com/106405775/178121683-51ce25ab-fbf6-4541-8f57-0ac6bea7ac07.png)

#### Total Rides
There were 1,625 rides in urban cities, 625 rides in suburban cities, and 125 rides in rural cities. 
![total rides by city type](/analysis/Fig6.png)

#### Total Drivers
Similarly, there was also more drivers in urban cities compared to suburban and rural cities. There were 2,405 drivers in urban cities, 490 drivers in suburban cities, and 78 drivers in rural cities.
![total drivers by city type](/analysis/Fig7.png)

#### Total Fares
Due to higher usage in urban areas, PyBer's total fares are also higher in urban cities when compared with suburban and rural cities. In the five month period, PyBer's transactions in urban cities totaled nearly $40,000 while transactions in suburban cities and rural cities totaled just over $19,000 and $4,000, respectively. 
![fares by City Type](/analysis/Fig5.png)

#### Average fare per ride and driver
In terms of user cost, riders in rural areas pay about $35 per ride which is almost $10 more than riders in urban cities who pay almost $25 per ride. The average fare in suburban areas falls between urban and rural cities at $31. 

Because riders in rural areas pay more per ride, it is a better market for drivers. The average fare per driver is about $55 in rural cities, about $40 in the suburbs, and $17 in urban cities.

#### Weekly breakdown of total fare by city type
The weekly breakdown of PyBer's total fares from January 1, 2019 through April 28, 2019 echos the above summary and demonstrates that urban cities consistently make up a larger potion of total fares. There is a peak in total fares in all city types that occurred the last week of February 2019. There is also a noteworthy drop the second week of April for urban and suburban cities. 
![total fare by city line chart](/analysis/PyBer_fare_summary.png)

## Summary
1. Riders in rural areas are paying significantly more per ride than those in urban cities which could discourage use. Adjusting fares in rural areas may help increase usage in those areas.
2. Similarly, most drivers are not in rural areas. There may not be availble drivers when a rider would like to take a trip which would make PyBer unreliable for rural riders. Thus, it may help to encourage drivers to travel to rural areas. Drivers in rural areas make significantly more in rural areas, so that could be a selling point. 
3. Overall, more research is needed determine the factors that are contributing to the high ride costs in rural areas. High total fares and limited drivers contribute to the disparity, but factors like total population in each city and distance traveled may also be factors. 
