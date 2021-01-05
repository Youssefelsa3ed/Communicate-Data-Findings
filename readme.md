# 2019 Bay Wheels Ride Data Exploration and Visualization
## by Youssef Farahat


## Dataset

[Bay Wheels]This dataset includes information about individual rides made in a bike-sharing system covering the greater San Francisco
Bay area, with nearly 180,000 rides. The dataset used for this exploratory analysis consists of [daily individual trip data](https://www.lyft.com/bikes/bay-wheels/system-data) at February 2019 in CSV format, also available [here](https://video.udacity-data.com/topher/2020/October/5f91cf38_201902-fordgobike-tripdata/201902-fordgobike-tripdata.csv).



##### Data wrangling process:
- fix multiple fields that are not in the correct dtype, i.e. `user_type` and `member_gender` should be categorical data type, etc
- add new columns for trip duration in minute, trip day of week
- add a new column calculating riders' age from 'member_birth_year'
- filter out outlier ages from visual examination of the member age distribution and statistical percentile
- cast 'member_age' to integer instead of float type
- cast 'weekday' to category dtype for easy plotting
- filter out outlier trip records where the duration was very long


## Summary of Findings

The average duration of trips 12 minutes, and compared to weekends there were more trips on other weekdays (Mon-Fri).

The short period of trips for subscribers corresponds to their high concentration on rush hours Monday through Friday, indicating the use is primarily for work commute.

Most riders were males, yet female riders tend to have longer trips compared to males.

The average age of the riders was around 35 years old, and as the age gets older, bike usage dropped.

A lot of older users are subscribes, and the trip duration is also high for older age. which may indicates that they're taking advantage of the bike sharing system quite differently from younger users, heavily over weekends for city tours or entertainment purpose.