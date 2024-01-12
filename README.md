Mental Illness Service Availability and Its Affect on Crime Rate


--------------------
Hypothesis
--------------------

If there is a relationship between mental health facilities in NYC boroughs and their respective crime rates, then the number of mental health facilities within NYC boroughs should have an impact on crime rates.

--------------------
Project Questions to Answer
--------------------
What is the crime rate for each of NYC’s boroughs? Is the crime rate higher in certain boroughs?
Does the number of mental health facilities affect the crime rate?
Are certain crimes higher in certain areas? How does that correlate with available services?


--------------------
Q1: What is the crime rate for each of NYC’s boroughs? Is the crime rate higher in certain boroughs?
--------------------

![NYC Borough Arrests Overview Map](Resources\Geo_Maps\NYC Boroughs.png)


-- Bronx
![Bronx Arrest Data](Resources\Geo_Maps\bronx_map.PNG)

9 Mental Health Facilities

1,472,654 Population


-- Manhattan
![Manhattan Arrest Data](Resources\Geo_Maps\Manhattan_map.PNG)

33 Mental Facilities

1,694,251 Population


-- Staten Island
![Staten Island Arrest Data](Resources\Geo_Maps\staten_island_map.PNG)

3 Mental Facilities

495,747 Population


-- Brooklyn
![Brooklyn Arrest Data](Resources\Geo_Maps\brooklyn_map.PNG)

19 Mental Facilities

2,736,074 Population


-- Queens
![Queens Arrest Data](Resources\Geo_Maps\queens_map.PNG)

14 Mental Facilities

2,405,464 Population




![NYC Borough Arrest Count](Resources\NYC_arrest_bar.png)

After grouping all of the arrest records by borough and finding the sum for each, we see that Brooklyn, Manhattan, and the Bronx have the highest arrest counts with Staten Island with the lowest.

Based on our hypothesis, we can guess that Brooklyn, Manhattan, and the Bronx have the least amount of mental health facilities while Staten Island has the most.


![NYC Mental Health Facility Count](Resources\NYC_facility_bar.png)

By getting the number of facilities for each borough, we actually find our guess to be incorrect. Manhattan, the borough with the second most arrests actually had the most mental health facilities while Staten Island, the borough with the lowest amount of arrests, had the least amount of mental health facilities.

After reviewing this new data, it begins to make sense why our guess was wrong. The city is more likely to provide more mental health facilities in areas where they see the most amount of crime.



--------------------
Q2: Does the number of mental health facilities affect the crime rate?
--------------------

![Crime Rate per Facility](Resources\NYC_crime_bar.png)

Our analysis of crime rate per borough facility does reveal a correlation between lower and mental health facilities across the different NYC boroughs.

Areas with fewer mental health facilities tend to experience increased crime rates, which highlights a potential connection between mental health resources and community safety.



-- Chi Squared Test 1

Hypothesis: If there is a relationship between mental health facilities in NYC boroughs and their respective crime rates, then the number of mental health facilities within NYC boroughs should have an impact on crime rates.

Null Hypothesis: There is no significant relationship between the number of mental health facilities and crime in NYC boroughs.

For the observed column, we collected the sum of all arrests within each borough.

For the expected column, we took the number of facilities in each borough divided by the total number of facilities to get facility percentage and then multiplied the borough’s arrest count by the facility percentage.

Critical value = 9.487729036781154

Power_divergenceResult(statistic=37456.18135041619, pvalue=0.0)

The statistic is significantly higher than our critical value and the p-value is very close to zero so we will be rejecting our null hypothesis.

These results suggest that there is a significant association between arrest counts and number of facilities.
Out of curiosity, we ran the chi-squared test with the expected value evenly distributed across all boroughs just to see if there was any significant change.



-- Chi Squared Test 2

Out of curiosity, we ran the chi-squared test with the expected value evenly distributed across all boroughs just to see if there was any significant change.

Power_divergenceResult(statistic=27740.865810282492, pvalue=0.0)

This second test had similar results and re-confirmed our hypothesis.



--------------------
Q3: Are certain crimes higher in certain areas? How does that correlate with available services?
--------------------

![Crime Distribution in Boroughs](Resources\NYC_Crime_dist.png)

We categorized each criminal offense into one of six categories and then got the sum for each category within a borough.

As you can see by the bar chart, there really isn’t much difference between the boroughs in terms of which type of crime is higher. Crimes against a person (robbery, murder, assault, etc) is the highest category in each borough followed by crimes against a property (vandalism, burglary, arson, etc) and statutory crimes (public intoxication, drug possession, etc).


![Relationship Between Number of Crimes and Number of Mental Health Facilities](Resources\arrest_fac_corr.png)

The r-squared is: 0.05473956549922081

So how does amount of arrests correlate with number of facilities within the boroughs?

Based on the r-squared value, we can conclude that the linear relationship between arrests and number of facilities is weak. However, there still might be some association, it’s just not well-captured by our linear model. 

As our chi-squared test proves, there is a relationship between crimes and number of mental health facilities.
