# Udacity Project - Bikesharing Dataset

## Data Wrangling and Data Visualisation

## by Lilla Szulyovszky


## Dataset

This data set includes information about individual rides made in a bike-sharing system covering the greater Boston area. 

Table of Contents
- Introduction of the dataset and Analysis Plan
- Data Wrangling
- Explonatory Data Analysis
- Explanatory Data Analysis

**Structure of the dataset**

- I have 12 csv's, for the 12 months of 2020. Ideally, I would like to see all 12 in one dataset, so I can have a wider range in time to draw conclusions from.

- Most of the cvs's have 15 columns with a few having only 14. 
- Need to make sure I'm not missing data so will reduce the ones with 15 rows to 14 before I merge them together. 
- Different months have different amount of entries, but that's normal and I will not manipulate that.

- I will look at the datasets' statistics, datatypes, missing and duplicated values as well as visually assess them to see if there is any need for cleaning.

**Columns**
- **tripduration**: trip duration in seconds
- **starttime**: the time the rental started
- **stoptime**: the time teh rental ended
- **start station id**: where the rental started
- **end station id**: where the rental ended
- **start station latitude**: gps coordinates of start station
- **start station longitude**: gps coordinates of start station
- **end station latitude**: gps coordinates of end station
- **end station longitude**: gps coordinates of end station
- **bikeid**: identificator of the bike used
- **usertype**: if the user has subscription or not
 Added:
- **type**: weekday or weekend
- **month**: month of the year
- **timeoftheday**: time by hour
- **weekday**: day of the week

**Insights to explore**

- How long does the average trip takes?
- Which are the most used start and end stations?
- When are the most trips taken in terms of time of day, day of the week, or month of the year?
- Which season is the most popular to ride a bike?
- Does these depend on if a user is a subscriber or customer?

**Features in the dataset the will help support the investigation?**

Trip duration, Start time, End time, Start station, End Station, Usertype


### Summary of Visual and Programmatic Assessment

### Quality Issues
*All datasets*
- `starttime` and `stopttime` column is in object format, it should be datetime

### Tidiness Issues

- merge datasets (concat)
- remove birthyear, postcalcode and gender columns as it only has partial month's data coverage, not the full year

Plus, there is no way to see
- which day of the week the data was recorded
- if the day is a weekday or a weekend
- which months of the year the data was recorded
- which time of the day the data was recorded

## Summary of Findings

1. The average trip takes 1831 seconds, which is approx. 30 minutes. I would like to see how the most frequent trip durations and the min and max value compare to the average.

2. The most frequent trip duration shows values between 1847 and 1897 seconds which is around 30 minutes as well.

3. It seems like both minimum and maximum values are mistakes done by the users, either they didn't ride the bike just started the rental (minimum duration is around 1 minute) or they left the bike without closing the rental (maximum duration is 64655 minutes).

4. The most frequently used start stations are: Central Square, Charles Circle, MIT, Christian Science Plaza, Annes St, Boylston St, MIT Pacific St, Cross St, Harward Square, Beacon St, MIT Stata Center, MIT Vassar St.

5. The most frequently used end stations are: Central Square, Charles Circle, MIT, Christian Science Plaza, Annes St - and until here, the most frequent start and end stations are identitical- Boylston St, Harward Square, Cross St, Nashua Street, Longwood Ave, Beacon St, MIT Pacific St, Beacon St.

6. The most popular days of the week for the riders are Saturday, Frdiay, Sunday, Wednesday, Tuesday, Thursday and not surprisingly, Monday comes the last.

7. The most popular months of the year to ride a bike are: September, August, July, October, June, November

8. The least popular ones are: April, December, March, May, January, February

9. There is a clear difference in number of rentals between weekdays and weekends and we can also see that the names of the stations differ on the most popular start and end stations, which likely means there are certain areas where people go to work from and to. To prove this however, I would need to visualise it on a map but that's out of the scope for this project.

10. The average trip duration on weekdays is around 1600 seconds and on weekends it's above 2300. This lets us conclude that people use the bikes on weekends for longer rides, perhaps not for the daily commute but for sport purposes.

11. We can see that the average usage for a single ride customer is almost tripled compared to the subscribers. This could easily happen due to the number of subscribers versus single ride customers. Let's investigate that.

12. It seems like there are a lot more subscribers than single ride customers, so looking at our plot let's conclude that single ride customers use the bikes for longer rides, while subscribers probably only use it for daily commute, which makes sense.

13. This plot clearly shows that
1, single ride customers are using the bikes for a longer duration than subscribers
2, single ride customers are using the bikes more often than subscribers
3, both user types are using the bikes more often and for a longer time in the months of summer.

14. On weekdays, we can see the frequency of usage goes up around rush hours, which makes a lot of sense.
On the other hand, weekends show a very balanced and gradually increasing and decreasing usage as people start to wake up, maybe go for a longer ride during the day and go home around the end of the afternoon.


15. By the plot above we can conclude that 
1, Customers use the bikes for longer trips than Subscribers on both type of weekdays, but more on the weekends
2, Subscribers also use the bikes for longer trips on weekends, but considerebly shorter rides than single ride customers

## Key Insights for Presentation

> Select one or two main threads from your exploration to polish up for your presentation. Note any changes in design from your exploration step here.