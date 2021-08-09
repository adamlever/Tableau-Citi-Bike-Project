![Citi_Bike_Logo](https://github.com/adamlever/Tableau-Citi-Bike-Project/blob/main/Images/Citi_Bike_Logo.png)

# Tableau-Citi-Bike-Project

Link to Citi Bike 2014 and 2019 Tableau Public Project;
https://public.tableau.com/app/profile/adam.lever/viz/CitiBike20142019Investigation/Dashboard1

## Investigation Rationale

Data from Citi Bike trips were downloaded for 2014 and 2019 for comaprison. The rationale for this was 2014 was the first full completed year of the Citi Bike project
and with the impact of the Covid pandemic affecting the amount of rides in 2020, it was decided to investigate the data accumalated from 2019 for the purpose of understanding
the extent of the growth of the program between 2014 and 2019.


## Data Extraction

- Data for Citi Bike trips in 2014 and 2019 was downloaded in .csv format by month of each year from the Citi Bike Data page (https://s3.amazonaws.com/tripdata/index.html).
- These files were then read using a 'for loop' within a 'for loop' and 'if' statements in Jupyter Notebook.
- It was then placed into separate 2014 and 2019 dataframes using Python Code. These were then concatenated together before being exported back into .csv format ready to load into Tableau.


## Data Transformation

- As the number of rows in our combined downlaoded data from 2014 and 2019 totalled 27,696,033 a heavy filtering process was needed to reduce this data to below the 15,000,000 of rows 
permitted by Tableau Public. 
- Only rides with a trip duration of greater than 600 seconds (10 minutes) and lower than 172,800 seconds (2 days) were considered with lower and higher duration trips removed.
- Data with 'Null' as its year in 'Starttime' were removed as were 'Birth Years' designated as 'Null' and '\N'.
- This filtering process resulted in 12,829,163 rows (individual trips) of data being used in the analysis.
- Birth Years in the data were given in two formats, one to a significant figure (eg. 1990) and one with a decimal point (eg. 1990.0). Where this occurred these two formats were grouped.


## Calculations

- Age was calculated by subtracting 2019 from the Birth Year of the rider. Due to time constraints on the project this age was used for the analysis of both 2014 and 2019 data. 
It should be noted that there are accuracy issues with this method with the age of the riders being analysed in 2014 being 5 years higher than they were at the time of the ride. However,
this calculated age, while not accurate was successful in being able to ascertain unexpected phenomena while assessing the chosen data.


## Data Anomalies

- There appears to be an excessive amount of people entering Birth Year as 1969 leading to a unusual amount of 50 year olds using the Citi Bike system in 2019. This can be attributed to the innuendo implied by the number 69 leading to riders entering an incorrect Birth Year as a joke.

![Citi_Bike_Birth_Year](https://github.com/adamlever/Tableau-Citi-Bike-Project/blob/main/Images/Citi_Bike_Birth_Year.png)


- The data indicates that the oldest riders that made a trip using Citi Bikes in 2019 was born in 1857, with four trips being made by a rider with this birth year. This would indicate that this person was 162 years old, an impossible age. There are also impossible ages and enteres Birth Years, so it is hard to determine what is the oldest rider on the Citi Bike system. It could be surmised that these incorrect dates may be due to a typing mistake or that the rider wished to remain annonymous.

![Citi_Bike_Age](https://github.com/adamlever/Tableau-Citi-Bike-Project/blob/main/Images/Citi_Bike_Age.png)

![Citi_Bike_Age_Binned](https://github.com/adamlever/Tableau-Citi-Bike-Project/blob/main/Images/Citi_Bike_Age_Binned.png)


## Other Findings

- During the working week (Monday to Friday), the most popular times of usage of the Citi Bike program is between 7am and 10am, and between 3pm and 7pm, it is surmised that a signficant amount of the rides during these times are for the purpose of commuting to work.

- This week day pattern is not present during the weekend, however there is an increase in usage of the program between 11am and 7pm on both Saturday and Sunday. A reason for this busier period is likely to be due to riders using the bikes for leisure time. 

![Citi_Bike_Time_of_Rides](https://github.com/adamlever/Tableau-Citi-Bike-Project/blob/main/Images/Citi_Bike_Time_of_Rides.png)


- Total number of trips in the data analysed increased from 1,903,864 taken in 2014 to 10,524,780 in 2019. An increase of 452.8%.

![Citi_Bike_Number_of_Trips](https://github.com/adamlever/Tableau-Citi-Bike-Project/blob/main/Images/Citi_Bike_Number_of_Trips.png)


- In 2014 the Citi Bike program was only available to Subscribers, by 2019 a casual customer option had been introduced.

![Citi_Bike_Trips_by_User](https://github.com/adamlever/Tableau-Citi-Bike-Project/blob/main/Images/Citi_Bike_Trips_by_User.png)

![Citi_Bike_Top_10_Start_Stations](https://github.com/adamlever/Tableau-Citi-Bike-Project/blob/main/Images/Citi_Bike_Top_10_Start_Stations.png)
![Citi_Bike_Top_10_End_Stations](https://github.com/adamlever/Tableau-Citi-Bike-Project/blob/main/Images/Citi_Bike_Top_10_End_Stations.png)



