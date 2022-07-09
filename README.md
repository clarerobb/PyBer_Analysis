
# PyBer Data Visualizations with Matplotlib 

## Overview
This analysis is for PyBer, a ride-sharing app, to summarize and visualize fares based on the city types (urban, suburban, rural) to determine trends and provide PyBer leadership with necessary information about the company's footprint. 

## Data
- city_data.csv
- ride_data.csv

## Method
After merging the data sources, I ran the code below to calculate PyBer summary by city type. I then resampled the data to display weekly summaries by city type.

'''
total_rides = pyber_data_df.groupby(['type']).count()['ride_id']
total_drivers = city_data_df.groupby(['type']).sum()['driver_count']
total_fares = pyber_data_df.groupby(['type']).sum()['fare']
average_fare_per_ride = total_fares/total_rides
average_fare_per_driver = total_fares/total_drivers
'''

## Results

#### Total Rides

#### Total drivers

#### Total fares

#### Average fare per ride

#### Average fare per driver

#### Total fare by city type
