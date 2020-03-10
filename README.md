# Weather Analysis on Car Accidents
I wanted to confirm whether its more dangerous to drive when it first rains (after a dry period). I found that dry driving is the most safe, but the danger in different kinds of wet conditions are statistically the same. This conclusion is probably misleading because the weather data was hourly and certain conditions could be more dangerous in smaller time periods. 


Here are some basic stats I found from a data set the city of Seattle put out with accidents starting in the 2000s:

Percentage of drunk driving accidents that result in a death:  0.96% (less than 1 percent)
Percentage of NON-drunk driving accidents that result in a death:  0.12% (less than 1 percent)

Percentage of drunk driving accidents that result in serioius injuries:  4.48%
Percentage of NON-drunk driving accidents that result in serious injuries:  1.42%

Percentage of drunk driving accidents that result in injuries 41.82%
Percentage of NON-drunk driving accidents that result in injuries 30.51%

Percentage of fatalities that involve a pedestrian:  35.06%
Percentage of serious injuries that involve a pedestrian:  28.18%
Percentage of injuries that involve a pedestrian:  11.35%

Using the Dark Sky API, I collected hourly weatherly data and stored that data. I created a script that returned the number of accidents for each condition. 

The conditions were: 1. Dry for 5 or more consecutive hours and on the 6th hour its dry. (5 hours because it allows the ground to become dry just in case there was a heavy rain before.)
                     2. Wet for 3 or more consecutive hours.
                     3. Wet for 3 or more consecutive hours but heavier rain.
                     4. Dry for 7 consecutive hours and on the 8th hour its wet.
                     5. Greater than or equal to .1 inches for 1 hour.


