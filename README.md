![Censos](https://github.com/AnaPatSilva/Population-Density-Portugal-Power-BI-Postgraduate-work/blob/main/Images/Censos.jpg)
# POPULATION DENSITY IN PORTUGAL (Postgraduation Assignment)
# _Power BI_

## My Intro
In the module Fundamentals of Business Intelligence and Data Analysis of my postgraduation, I had to do an assignment on the usefulness of Business Intelligence for handling and analyzing data.

I had to choose a dataset and treat the data in Power BI or SQL and Visual Studio.

I chose data from the 2011 and 2021 population censuses in Portugal and decided to use Power BI.

## Summary
Throughout this manuscript, I will reflect on the usefulness of Business Intelligence for handling and analyzing data, in the most diverse environments and topics. Although there are several BI tools, I did my work in Power BI. With this tool I was able to prepare the datasets collected and work with the data in order to present the information in a clear and understandable way. To demonstrate the tool's potential, I chose to do an analysis of Portugal's Population Density, focusing on some key characteristics of the population. This analysis was based on data obtained from the 2011 and 2021 population censuses. This data, after being correctly processed and well presented, allowed me to obtain relevant and interesting information about the Portuguese population in each of the decades, make a comparison between them and extrapolate this comparison to a forecast of the data in 2031. The interpretation of this information could be essential both for the Portuguese government, which is "responsible" for this population, and for a private company wishing to advertise its business, depending on the population of each country.

## Introduction
The aim of this work is to analyze Portugal's Population Density using a Business Intelligence tool. Since Business Intelligence is increasingly essential for analysis and decision-making, I decided to use this process on a topic as multifaceted as the Portuguese population.

In this way, I used the data obtained by the National Statistics Institute from the 2011 and 2021 Censuses. This data was processed in Power BI (one of the BI tools), so that I could create intuitive dashboards, which allow me to visualize some of the characteristics of the population in each of the decades, and to analyse and predict the evolution of these characteristics.

Therefore, the entire process of collecting, processing, analyzing and forecasting the data will be described and justified below.

## TOPIC DEVELOPMENT 
### Data to be analyzed
Among the options provided by the teacher, I chose to analyze the Portuguese population because, being in the area of Human Resources, this is data that particularly interests me.

However, as the Census datasets were unavailable at http://dados.gov.pt/pt/, I decided to go directly to the source. In other words, I took the information I found most interesting from the 2011 and 2021 Censuses from the INE website. This included:
- Age group
- Marital status
- Sex
- Education
- Total Population
- Total Population by Location

To do this, it was necessary to remove 3 Excel files, segmented by information (Age Group, Marital Status and Education), but with data in common ( Location, Location Code).

### Business Intelligence tool
As a Business Intelligence tool, I chose Power BI because it's a tool I've already had contact with professionally and because I can't install SQL and Visual Studio on my current laptop.

### Dataset treatment
Using Power Query, I imported the 3 Excel files (Education, Age Group, Marital Status), but as the format was not being accepted (97-2003), I had to save them in a more recent format (.xlsx). These 3 files were transformed into 3 separate tables.

![Power_Query](https://github.com/AnaPatSilva/Population-Density-Portugal-Power-BI-Postgraduate-work/blob/main/Images/Power_Query.png)

After this first setback, it was time to prepare the 3 tables:
- I deleted the unnecessary rows
- Promoted the column titles to headers
- Changed some columns to whole numbers
- I automatically filled in the Year column with the corresponding year (the year didn't appear in all the rows)
- I added ", Portugal" to the Location column, so that the cities would be identified as being in Portugal

Next, I created the following tables:
- **Calendar:** I limited the column to the years 2011 to 2022, because I wouldn't need a longer period of time;
- **Location:** I used the Excel file "Age Group" as a base, but only kept the columns I was interested in, to link with the other tables (Location and Local Code).

### Relationships between tables
![Relationships](https://github.com/AnaPatSilva/Population-Density-Portugal-Power-BI-Postgraduate-work/blob/main/Images/Relationships.png)

Leaving Power Query and returning to Power BI, I went on to create the relationships between tables, in order to ensure that the data between the tables was linked.
The unifying tables are:
- **Calendar:** relates the "Year" column in this table to the columns with the same name in the Education, Marital Status and Age Group tables;
- **Location:** relates the "Location code" column of this table to the columns with the same name in the Education, Civil Status and Age Group tables.

### Dashboards
After processing the dataset and creating the relationships, I was able to start creating the dashboards to present the information collected. However, this process is not watertight, as during the creation of the dashboard I realized that I needed to make changes to the dataset and/or the relationships.

**1. General 2011 or 2021**

![General_2011_2021](https://github.com/AnaPatSilva/Population-Density-Portugal-Power-BI-Postgraduate-work/blob/main/Images/General_2011_2021.png)

This page shows various pieces of information about the Portuguese population, segmented by year.

**Total Population:** Total population for the selected year;
**Total Men / Women and %:** Total men and women of the selected year; to calculate the percentage I created calculable columns in Power Query;
**Age Group:** Population of the selected year, by age groups;
**Marital status:** Population of the selected year, by marital status;
**Education:** Population of the selected year, by level of education;
**Cities:** Map of bubbles taking into account the population of the selected year, by city; I've added a tooltip, where you can see a table with the city and the total population.

**2.	Comparing 2011 and 2021**

![Comparing_2011_2021](https://github.com/AnaPatSilva/Population-Density-Portugal-Power-BI-Postgraduate-work/blob/main/Images/Comparing_2011_2021.png)

To make it easier to compare figures between 2011 and 2021, this page shows various details about the Portuguese population, segmented by year.

**Total Population:** Total population for the years 2011 and 2021 and the difference between the two (number of population and percentage); for the value of the difference between the years, I had to create measures to calculate this;
**Total Men / Women and %:** Total number of men and women in 2011 and 2021;
**Age Group:** Population in 2011 and 2021, by age group;
**Marital status:** Population of the years 2011 and 2021, by marital status;
**Education:** Population of the years 2011 and 2021, by level of education;
**Cities:** I didn't create this visual, because it wouldn't be possible to visualize this comparison on a map, it would only be possible in a graph or table, but both were filled with too much information, not easy to interpret.

**3.	Forecast 2031**

![Forecast_2031](https://github.com/AnaPatSilva/Population-Density-Portugal-Power-BI-Postgraduate-work/blob/main/Images/Forecast_2031.png)

In order to recreate the predictive capacity that Business Intelligence tools have, I decided to add this page where you can see the forecast values for 2031, taking into account the evolution that took place between 2011 and 2021. To do this, I had to create various measures to calculate the differences between the years and apply this difference to define the value for 2031.

However, I am aware that the time period between 2011 and 2021 is not enough to make predictions, and there are many other external factors that can affect the evolution of population density that are not portrayed here (e.g. economic crisis, war, state support, ...). 

**Total Population:** Forecast of the total population in 2031;
**Total Men / Women and %:** Forecast of total men and women in 2031;
**Age Group:** Population forecast for 2031, by age group;
**Marital Status:** Population forecast for 2031, by marital status;
**Education:** Population forecast for 2031, by level of education;
**Cities:** Map of bubbles taking into account the population forecast for, by city; I added a tooltip, where you can see a table with the city and the total population.


## CONCLUSIONS 
Now that the work in Power BI has been completed, it is easier to visualize and interpret the data collected.

In particular, it is possible to observe some interesting information:
- The total population decreased by 2.06% from 2011 to 2021;
- Although the population has decreased, this has only been in males, as the percentage of females has increased;
- In terms of age, we see a clear ageing of the population;
- In terms of marital status, we can see that the Portuguese are choosing marriage less and less and the number of divorces has increased;
- And finally, we see an increase in the population's level of education, however, we still have a large percentage of people with only basic education, and 1.5 million people with no academic degree.

With the data from 2011 and 2021, a forecast was made for the year 2031. However, as I've already mentioned, data from two decades is not enough to make a reliable forecast, and there are many other factors that can influence the evolution of population density.

In short, during the course of my work I was able to get to grips with some of the potential of Business Intelligence and this tool in particular, as it not only improves the visualization of data, but also its interpretation and prediction, thus allowing decisions to be made based on concrete information. For example, in this specific case, if we were the Portuguese government, we could create measures to encourage the birth rate, to allow better access to higher education, to reduce school drop-outs, ...
Data analysis is more important than data alone!
