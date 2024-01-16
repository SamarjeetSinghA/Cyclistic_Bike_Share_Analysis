# Cyclistic Bike Share Analysis - Using SQL and Tableau

I am excited to present to you my first case study as a Data Analyst, where I worked with a realistic dataset and gained some valuable insights about the business and its customers. 

### Related Links
* [Tableau]() for Data Visualization Dashboard
* [Powerpoint Presentation]() for Analysis Summary
* [LinkedIn Profile]() 
* [Full Portfolio]()

## Table of Contents
1. Introduction
2. Objective
3. Preparation
4. Process
5. Analysis 
6. Conclusion

## Introduction

The Cyclistic Bike Share case study is part of a Google Data Analytics Certification Hosted on Coursera. I completed this Case study as a Capstone Project for the Certification. 

The data used in this project is publicly available [here](https://divvy-tripdata.s3.amazonaws.com/index.html) under this [license](https://www.divvybikes.com/data-license-agreement) from Divvy Bikes. I used the latest available datasets of the past 12 months, which were from December 2022 to November 2023. The data consists of more than 5 Million rows and 13 Columns. I have the Ride ID, Type of bike, the start/end station names, their latitude, longitude and IDs and the Member Type (Casual or Annual)

## Objective
Cyclistic is a Bike Share service in Chicago. As a Junior Data Analyst, working in a Bike Sharing Company, my objective was to find how the Casual members and the Annual members use the Bike Share service differently and provide 3 recommendations on how we can covert Casual members to Annual members as Annual members are more profitable for the company.

### Tools Used
1. PostgreSQL
2. DBeaver
3. Tableau

## Preparation
The first thing I did was to download the datasets of the past 12 months, which were available in CSV format. I imported all the files into Dbeaver.

After analyzing all the columns and selecting appropriate data types for them, I created a table using PostgreSQL and merged all the downloaded datasets to the new table that I called "Cyclistic_2023_Bikeshare_Data". 

## Process
* To process the data, I first thought about the insights I wanted to gather and what data I needed to use for that. I realized that I did not need the Start/End station ID, so I deleted those columns.

* I also did not need the Start/End Station Latitudes and Longitudes for this case study but I still kept it because it can later help us visualize the data through geographical maps. 

* I checked the data for any inconsistencies, so I checked the data for Duplicate Records and null and Empty Values. I found that out of 5.6M rows, 1.3M rows had missing start or end station names, so I deleted those records. 

* I checked the unique values of other columns for Inconsistencies and found nothing.

* I checked for any logical errors in the data and found that in 262 records, the end time of the ride was less than the start time, so I removed those records. 

* I tried sorting the data through different columns to find the outliers. 

* After checking for Inconsistencies, I created a new column named "Ride_length" with INTERVAL data type where I stored the ride duration by calculating the difference of the ride start and end time. 

* I deleted 87,141 Rows of data where the Ride Length was less than 60 seconds as this data might contain errors or there might be user errors while using the service that caused these records. 

* For data visualization, I explored this processed data set and uploaded it to Tableau Public. 



## Analysis
Here are the findings I derived from the processed data:

* The Average Ride Duration was 16.28 Minutes and the Average Ride Duration for Casual Members (23.32 Minutes) was almost double of Annual Members (12.38 Minutes)

* 64% of the Cyclistic users are Annual Members

* The most popular bike between both member types is the classic bike, followed by the electric bike.

* Annual members do not use the docked bikes. 

* Annual members use the bikes mostly around 8 am and 5 pm and on weekdays, signifying that they probably use the bikes to travel to their workplace or college.

* Casual members use the bikes mostly around 5 pm and on weekends, suggesting that they use the bikes for recreation in the evenings.

* Both members use the bike service highest in the months of summer (June-August) and least in the winter.

* The busiest station of all was Streeter Dr & Grand Ave, followed by Dusable Lake Shore & Monroe St and Michigan Ave & Oak St.

## Recommendations

Below are the 3 Recommendations that can help to convert Casual Riders into Annual members:

* As we can extract from the data our current set of annual members are mosty those who use the service to commute to work or college. The upcoming marketing campaigns should focus on the other set of people who use the bikes for recreation (Casual Members). The recreational rides are often social where friends or family join together, so there can be a referral bonus if they make their friends and family sign up or a family plan for 2 or more people. 

* A Targeted marketing campaign focusing on Casual members during the early summers, especially in the top 5 busiest stations. The joy of riding and suitable weather can be highlighted. A sense of urgency can also be created by offering early bird discounts or an extra month of subscription to attract members. 

* Bringing a Seasonal Pass can also greatly help with converting casual members into subscribers. The bikes are mostly used in summer and casual users might hesitate to commit to the annual membership as they use the bikes less in the winter. 

## Conclusion
Cyclistic Bike Share was my first Data Analytics Case Study and I feel very confident after completing it as well as the Google Data Analytics Certification.

During the case study, I watched a lot of YouTube tutorials and did many Google searches to gather additional knowledge and to make sure I had a comprehensive understanding of the tools and techniques needed.

Starting from raw data of over 5 Million Rows and processing it to finally gain key insights about consumer behaviour was a valuable experience in solidifying my understanding of data analytics. 