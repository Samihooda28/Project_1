# Project_1
This repository contains files used to Road Fatalities in Australia 2014-2021. The code for analysis is contained in 3 pandas files called Cleaning_raw_crash_data, Crash Victim Characteristics Code and First_Project. The raw data csv and the cleaned exported csv file are contained in the Data folder called crash_data and cleaned crash data respectively. All graphs created in Crash Victim Data were saved and exported to the Images file. The plots from CLeaning_raw_crash_data was exported and saved into the Images folder within the data folder.  


Cleaning_raw_crash_data Code
First of all, we took Crash Data Australia to figure out the fatal causalities that happened in Australia. After that, we removed all the NaN values and only selected the columns which we will be using in the project.

We also removed the "Other/-9" user from the Road User column and unspecified values from the Speed Limit column. Then, we reset the index and dropped the original index.

After that used a bar chart to figure out which states have the most fatal causalities and found out that NSW and VIC have the most number of crashes as they got the highest number of populations also.

Used the value count function to count the number of crashes in a remote area to figure out whether crashers happen more in the city or regional area. After that use a bar chart for the visualization.

After that, did a bar chart for the crashes in a year and found out that the crashes keep increasing every year.

Used the aggression function to calculate the mean, median, and standard deviation for speed limit vs each state.

Used a line chart to show the number of crashes that happened inside a speed limit.

Crash Victims Characteristics Code 
•	This pandas code analysed the characteristics of the victims of the fatal crashes, their age, gender, and the type of road user they were. 
•	First all the modules required to create visuals and analyse the data were imported into the datafile. 
•	A path was created to the crash data that had been cleaned in a previous pandas file (named cleaned_crash_data) that was stored in the data folder. 
•	The CSV of the cleaned crash data file was read into pandas as a data frame. 

•	The distribution of the types of road users was analyzed by first creating a series that counted the number of fatalities for each type of road user from the “Road User” column of the cleaned data frame. (victim_type_distribution).
•	This data was plotted as a pie chart using pandas. 
•	This victim_type_distribution series was then plotted as a bar chart. 

•	The distribution of the gender of road users was analyzed by first creating a series that counted the number of fatalities for each gender in the “Gender” Column of the cleaned crash data frame (gender_distribution).
•	This data was plotted as a pie chart using pandas. 

•	The age range of the victims was analyzed by first creating a series that counted the number of fatalities per age range from the “Age Group” column of the cleaned data frame  (age range_data).
•	The series was then plotted as a bar chart using pandas. 

•	Next the data was filtered to look at a select number of fatalities only. By selecting rows where the victim was the driver of a car a motorcycle and the crash was a single vehicle only this was selecting for fatalities where the victim was responsible for the crash. This was done via the .loc function and using the “Road User” and “Crash Type” columns with conditionals to create a new data frame (driver_victim_data). 

•	Using the new data frame, driver_victim_data, pie, and bar charts were created for the distribution of gender and age range of the victims vs the number of fatalities for crashes where the driver was the victim and it was a single vehicle collision using the same method that was used for the cleaned crash data. 


•	Then the age range data for all road crash fatalities was compared to the age range data for crashes where the victim was the driver in a single-vehicle collision. To make a fair comparison rather than the number of fatalities, the percentage of fatalities for each age range was compared. 
•	First the total number of fatalities in each data frame was counted using the “Crash ID” column of each data frame. To calculate the percentage each age range series was divided by the total number of fatalities and multiplied by 100. This created a series where the percentage of fatalities for each age range was calculated (age_range_data_percentage, age_driver_data_percentage). These two series were then merged into one data frame called victim_age_percentage_summary. 
•	This series was then plotted as a bar chart using pandas.

•	Next the number of fatalities per discrete age value was analyzed. First, a series was created to count the number of fatalities per age using the .count function on the “Age column” of the cleaned_crash_data data frame  (discrete_age_data). This series was then converted into a data frame and the index was reset (victim_age_summary). Summary statistics for the number of crashes per age were calculated using the aggregation method on the discrete_age_data series to find the mean, median, variance, standard deviation, and SEM of the data.
•	The number of fatalities vs age was then plotted as a scatter plot using matplotlib and iloc from the victim_age_summary data frame. Matplotlib was then used to calculate the correlation coefficient and a linear regression model to show the relationship between the age of the victim and the number of crashes.
•	This process was then repeated for the data frame containing fatalities from single-vehicle crashes only where the driver was the victim. 
•	Some time data was also transformed to be able to get some calculation for bins and created a (Time Frame) 
•	All plots were saved to a file called Images in the project_1 repository. 


