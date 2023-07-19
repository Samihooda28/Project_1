# Project_1
Crash Victims Characteristics Code 
•	This pandas code was analysis the characteristics of the victims of the fatal crashes, their age, gender and the type of road user they were. 
•	First all the modules required to create visuals and analyse the data were imported into the datafile. 
•	A path was created to the crash data that had been cleaned in a previous pandas file (named cleaned_crash_data) that was stored in the data folder. 
•	The CSV of the cleaned crash datafile was read into pandas as a dataframe. 

•	The distribution of the types of road user was analysed by first creating a series that counted the number of fatalities for each type of road user from the “Road User” column of the cleaned dataframe. (victim_type_distribution).
•	This data was plotted as a pie chart using pandas. 
•	This victim_type_distribution series was then plotted as a bar chart. 

•	The distribution of the gender of road user was analysed by first creating a series that counted the number of fatalities for each gender in the “Gender” Column of the cleaned crash dataframe (gender_distribution).
•	This data was plotted as a pie chart using pandas. 

•	The age range of the victims was analysed by first creating a series that counted the number of fatalities per age range from the “Age Group” column of the cleaned dataframe  (age range_data).
•	The series was then plotted as a bar chart using pandas. 

•	Next the data was filtered to look at a select number of fatalities only. By selecting rows where the victim was the driver of a car a motorcycle and the crash was a single vehicle only this was selecting for fatalities where the victim was responsible for the crash. This was done via the .loc function and using the “Road User” and “Crash Type” columns with conditionals to create a new dataframe (driver_victim_data). 

•	Using the new dataframe, driver_victim_data, pie and bar charts were created for the distribution of gender and age range of the victims vs the number of fatalities for crashes where the driver was the victim and it was a single vehicle collision using the same method that was used for the cleaned crash data. 


•	Then the age range data for all road crash fatalities was compared to the age range data for crashes where the victim was the driver in a single vehicle collision. To make a fair comparison rather than the number of fatalities, the percentage of fatalities for each age range was compared. 
•	First the total number of fatalities in each dataframe was counted using the “Crash ID” column of each dataframe. To calculate the percentage each age range series was divided by the total number of fatalities and multiplied by 100. This created a series where the percentage of fatalities for each age range was calculated (age_range_data_percentage , age_driver_data_percentage). These two series were then merged into one dataframe called victim_age_percentage_summary. 
•	This series was then plotted as a bar chart using pandas.

•	Next the number of fatalities per discrete age values was analysed. First a series was created to count the number of fatalities per age using the .count function on the “Age column” of the cleaned_crash_data dataframe  (discrete_age_data). This series was then converted into a dataframe and the index was reset (victim_age_summary). Summary statistics for the number of crashes per age were calculated using the aggregation method on the discrete_age_data series to find the mean, median, variance, standard deviation and SEM of the data.
•	The number of fatalities vs age was then plotted as a scatter plot using matplotlib and iloc from the victim_age_summary dataframe. Matplotlib was then used to calculate the correlation coefficient and a linear regression model to show the relationship between age of the victim and the number of crashes.
•	This process was then repeated for the dataframe containing fatalities from single vehicle crashes only where the driver was the victim. 
•	All plots were saved to a file called Images in the project_1 repository. 
