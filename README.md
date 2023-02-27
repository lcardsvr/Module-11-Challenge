# Module-11-Challenge
Module 11 Challenge

This assignment consists of two technical products.

Deliverable 1: Scrape titles and preview text from Mars news articles.

Deliverable 2: Scrape and analyse Mars weather data, which exists in a table.

## Part 1: Scrape Titles and Preview Text from Mars News

### Deliverable 1: Scrape titles and preview text from Mars news articles.

The Jupiter Notebook with the code for this derivable is available under https://github.com/lcardsvr/Module-11-Challenge/blob/main/part_1_mars_news.ipynb

The desired result is displayed below.

| Title and preview Summaries |
|---------------------------------------------------------------------------------|
|{'title': "NASA's MAVEN Observes Martian Light Show Caused by Major Solar Storm",|
|  'preview': 'For the first time in its eight years orbiting Mars, NASA’s MAVEN mission witnessed two different types of ultraviolet aurorae simultaneously, the result of solar storms that began on Aug. 27.'},|
|{'title': "NASA Prepares to Say 'Farewell' to InSight Spacecraft",|
|  'preview': 'A closer look at what goes into wrapping up the mission as the spacecraft’s power supply continues to dwindle.'},|
|{'title': 'NASA and ESA Agree on Next Steps to Return Mars Samples to Earth',
|  'preview': 'The agency’s Perseverance rover will establish the first sample depot on Mars.'},|
|{'title': "NASA's InSight Lander Detects Stunning Meteoroid Impact on Mars",|
|  'preview': 'The agency’s lander felt the ground shake during the impact while cameras aboard the Mars Reconnaissance Orbiter spotted the yawning new crater from space.'},|
|{'title': 'NASA To Host Briefing on InSight, Mars Reconnaissance Orbiter Findings',
|  'preview': 'Scientists from two Mars missions will discuss how they combined images and data for a major finding on the Red Planet.'},|
|{'title': 'Why NASA Is Trying To Crash Land on Mars',
|  'preview': 'Like a car’s crumple zone, the experimental SHIELD lander is designed to absorb a hard impact.'},|
|{'title': 'Curiosity Mars Rover Reaches Long-Awaited Salty Region',
|  'preview': 'After years of climbing, the Mars rover has arrived at a special region believed to have formed as Mars’ climate was drying.'},|
|{'title': 'Mars Mission Shields Up for Tests',
|  'preview': 'Protecting Mars Sample Return spacecraft from micrometeorites requires high-caliber work.'},|
|{'title': "NASA's InSight Waits Out Dust Storm",|
|  'preview': 'InSight’s team is taking steps to help the solar-powered lander continue operating for as long as possible.'},|
|{'title': "NASA's InSight 'Hears' Its First Meteoroid Impacts on Mars",|
|  'preview': 'The Mars lander’s seismometer has picked up vibrations from four separate impacts in the past two years.'},|
|{'title': "NASA's Perseverance Rover Investigates Geologically Rich Mars Terrain",|
|  'preview': 'The latest findings provide greater detail on a region of the Red Planet that has a watery past and is yielding promising samples for the NASA-ESA Mars Sample Return campaign.'},|
|{'title': 'NASA to Host Briefing on Perseverance Mars Rover Mission Operations',
|  'preview': 'Members of the mission will discuss the rover’s activities as it gathers samples in an ancient river delta.'},|
|{'title': "NASA's Perseverance Makes New Discoveries in Mars' Jezero Crater",|
|  'preview': 'The rover found that Jezero Crater’s floor is made up of volcanic rocks that have interacted with water.'},|
|{'title': "10 Years Since Landing, NASA's Curiosity Mars Rover Still Has Drive",|
|  'preview': 'Despite signs of wear, the intrepid spacecraft is about to start an exciting new chapter of its mission as it climbs a Martian mountain.'},|
|{'title': "SAM's Top 5 Discoveries Aboard NASA's Curiosity Rover at Mars",|
|  'preview': '“Selfie” of the Curiosity rover with inset showing the SAM instrument prior to installation on the rover.'}|


  ## Part 2: Scrape and Analyse Mars Weather Data

  ### Deliverable 2: Scrape and analyse Mars weather data, which exists in a table.

The Jupiter Notebook with the code for this derivable is available under https://github.com/lcardsvr/Module-11-Challenge/blob/main/part_2_mars_weather.ipynb


The HTML table was extracted into a Pandas DataFrame with Splinter and Beautiful Soup were used to scrape the data. The columns have the correct headings and data types as requirements. 



| # |  Column |           Non-Null Count | Dtype|         
|--- | ------ |          --------------  | ----- |        
| 0 |  id     |         1867 non-null   |int32 |        
| 1 |  terrestrial_date | 1867 non-null  | datetime64[ns]|
| 2 |  sol              | 1867 non-null  | int32  |       
| 3 |  ls               | 1867 non-null  | int32  |       
| 4 |  month            | 1867 non-null  | int32  |       
| 5 |  min_temp         | 1867 non-null  | float64|       
| 6 |  pressure         | 1867 non-null  | float64|   


The data was analysed to answer the following questions:

#### How many months exist on Mars? 

With the data that is available checking the greatest month number available in the dataset, we obtain 12 months. month is the Martian month according to the instructions (The code used for this was "mars_data_df.month.max()")

Querying in google it is stated that there are 24 martian months of 28 days (https://www.sciencedirect.com/science/article/abs/pii/S0032063397000330#:~:text=A%20common%20year%20would%20have,weeks%20of%207%20days%20each).). 

#### How many Martian days' worth of data are there? 

In Earth times:

1. The earliest date available is 2012-08-16 00:00:00.
2. The latest date available is 2018-02-27 00:00:00. 
3. There are 2021 days worth of data earth data


Taking into account that a martian year being is around 674 days (see results in section below), the total length of Martian data is close to 2021/674 ~ 3 Years of Martian data.



#### Which month, on average, has the lowest temperature? The highest?

![image](/00_Average_Temperature_Month.png)


![image](/00_Average_Temperature_Month_bar_chart.png)

On average, the third month has the coldest minimum temperature on Mars, and the eighth month is the warmest.

|Month|Temperature|
| ---| ----|
|1|-77.160920|
|2|-79.932584|
|3|-83.307292|
|4|-82.747423|
|5|-79.308725|
|6|-75.299320|
|7|-72.281690|
|8|-68.382979|
|9|-69.171642|
|10|-71.982143|
|11|-71.985507|
|12|-74.451807|

#### Which month, on average, has the lowest atmospheric pressure? The highest? 

![image](/02_Average_Pressure_Per_Month.png)

![image](/02_Average_Pressure_Per_Month_bar_chart.png)

Atmospheric pressure is, on average, lowest in the sixth month and highest in the ninth.

|Month|Pressure|
| ---| ----|
|9|913.305970|
|2|889.455056|
|10|887.312500|
|3|877.322917|
|8|873.829787|
|1|862.488506|
|11|857.014493|
|12|842.156627|
|4|806.329897|
|7|795.105634|
|5|748.557047|
|6|745.054422|

#### How many terrestrial days exist in a Martian year? A visual estimate within 25% was made

Plotting the temperature measurements the graph below is obtained.

![image](/03_Temperarure_Measument_day.png)

To avoid the outliers in the maximum values, the lowest temperatures were used for analysis. 

The minimum values per year are below.

|Year|	id	|terrestrial_date	|sol	|ls	|month	|min_temp	|pressure|
| ---| ----| -------            |----  |----| -----| --------- | --------| 							
|2012|2|2012-08-16|10|155|6|-78.0|732.0|
|2013|51|2013-01-01|144|0|1|-87.0|845.0|
|2014|430|2014-01-01|500|70|3|-88.0|732.0|
|2015|795|2015-01-01|855|0|1|-90.0|832.0|
|2016|1140|2016-01-01|1210|88|3|-89.0|732.0|
|2017|1486|2017-01-01|1566|0|1|-87.0|781.0|
|2018|1840|2018-01-01|1922|108|4|-80.0|727.0|

Looking for the date with the minimum temperature in 2014 :

|id|terrestrial_date|sol|ls|month|min_temp|pressure|Year|
| ---| ----| -------            |----  |----| -----| --------- | --------| 	
|452|464|2014-02-03|532|84|3|-88.0|872.0|2014|

Looking for the date with the minimum temperature in 2015 :

|id|terrestrial_date|sol|ls|month|min_temp|pressure|Year|
| ---| ----| -------            |----  |----| -----| --------- | --------| 	
|1093|1119|2015-12-09|1188|79|3|-90.0|881.0|2015|

Substracting the 2 dates a year of approximately 674 days is obtained.

Timedelta('674 days 00:00:00')

#### The DataFrame was exported into a CSV file. 

Generated CSV file available under https://github.com/lcardsvr/Module-11-Challenge/blob/main/Mars_Temperature_Data.csv



## Submission

1. Submitted and available in GitHub under https://github.com/lcardsvr/Module-11-Challenge

2. Derivable 1 Jupyter Notebook available under https://github.com/lcardsvr/Module-11-Challenge/blob/main/part_1_mars_news.ipynb

3. Derivable 2 Jupyter Notebook available under https://github.com/lcardsvr/Module-11-Challenge/blob/main/part_2_mars_weather.ipynb