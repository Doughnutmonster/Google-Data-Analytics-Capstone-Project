# Google-Data-Analytics-Capstone-Project
Case Study 1: How does a bike-share navigate speedy success?

By: Whitney Okenwa

# Scenario

You are a junior data analyst working on the marketing analytics team at Cyclistic, a bike-share company in Chicago. The director of marketing believes the company’s future success depends on maximizing the number of annual memberships. Therefore, your team wants to understand how casual riders and annual riders use Cyclistic bikes differently.

From these insights, your team will design a new marketing strategy to convert casual riders into annual members. But first, Cyclistic executives must approve your recommendations, so they must be backed up with compelling insights and professional data visualizations.

# Expectations and Deliverables
A clear statement of the business task.

A description of all data sources used.

Documentation of any cleaning or manipulation of data.

A summary of your analysis.

Supporting visualizations and key findings.

Your top three recommendations based on your analysis.


# Analysis Process
## Ask
How do annual riders differ from casual riders in their use of the service?

Why would casual riders buy a Cyclistic annual membership?

How can Cyclistic use digital media to influence casual riders to convert?

## A clear statement of the business task
The business task is to develop a strategy for converting casual riders into annual members by first identifying the key factors that can motivate casual riders to upgrade to an annual membership, and then using digital media to effectively implement this strategy.


## Prepare

Data source: https://divvy-tripdata.s3.amazonaws.com/index.html

The data is organized by month and year from 2020 til date.
Data is also organized quarterly from 2013 to 2020. 
Data is made available by Motivate International Inc., whose license can be viewed here: https://divvybikes.com/data-license-agreement

For relevance, the data utilized in this analysis process was drawn from the period of January 2025 to December 2025.

## Process

The 12 tables from January 2025 to December 2025 were combined into one table containing **5,552,944** rows.


The table contains 13 fields, which are included in the table below;

| No. | Field Name | Type | Description |
| :--- | :---: | :---: | ---: |
| 1 | ride_id | STRING | ID assigned to each ride |
| 2 | rideable_type | STRING | Type of bike (Electric or Classic) |
| 3 | started_at | TIMESTAMP | Date and time when the trip starts |
| 4 | ended_at | TIMESTAMP | Date and time when the trip ends |
| 5 | start_station_name | STRING | Name of bike pick-up station |
| 6 | start_station_id | STRING | ID of bike pick-up station |
| 7 | end_station_name | STRING | Name of bike drop-off station |
| 8 | end_station_id | STRING | ID of bike drop-off station |
| 9 | start_lat | FLOAT | Latitude of pick-up station |
| 10 | start_lng | FLOAT | Longitude of pick-up station |
| 11 | end_lat | FLOAT | Latitude of drop-off station |
| 12 | end_lng | FLOAT | Longitude of drop-off station |
| 13 | member_casual | STRING | Type of membership per rider |



To ensure data quality, I conducted comprehensive queries on each column to identify inconsistencies, including null values and outliers. I then cleansed the dataset by removing trips with missing values, excluding rides lasting less than one minute or more than one day, and adding three new columns: **"month"**, **"day_of_week"**, and **"ride_length_in_mins."** As a result, **1,961,696** rows were removed.

## Analyze

To gain deeper insights into rider behavior, I conducted SQL queries to uncover key averages and frequencies that reveal usage patterns across different user types. Here are the results:


Average ride duration in minutes: **15.80**

Average ride duration for annual members: **12.18**

Average ride duration for casual riders: **22.21**


Average ride duration per day: 

<img width="381" height="216" alt="Avg ride length per day of week" src="https://github.com/user-attachments/assets/b1856bc3-00f0-47a4-ba67-763c74f6211f" />


Notably, Sunday emerges as the peak day for ride duration across both user groups. Casual riders, in particular, extend their journeys to an average of **25.74** minutes, while annual members also see their longest rides, averaging **13.64** minutes.

Total Number of rides per Day:

The highest number of rides for annual members is on Tuesdays, with 372,026 total rides, and the highest number of rides for casual riders is on Saturdays, with 269,198 total rides.

Casual vs Member rider activity per Month:

The highest rider activity for casual riders is in the month of August with a total of 216,515 rides, while the highest rider activity for annual members falls in the month of September with a total of 286,850 rides.

Key Takeaways
Annual members ride more frequently than casual riders.
Casual riders ride for longer durations than annual members.
Annual members ride more often on Weekdays, while casual riders ride more on the weekends.
Riding activity for both annual members and casual riders peaks during the Summer Months.
August had the highest average of riding activity for both groups.

Analysis Summary
The analysis explored key behavioral differences between annual members and casual riders using targeted SQL queries to examine ride frequency, average duration, and usage patterns by day and month. Findings revealed that annual members ride more often—2,296,802 rides compared to 1,294,446 for casual riders—while casual riders take longer trips on average (22.21 minutes vs. 12.18 minutes). Members are most active on weekdays, especially Tuesdays, whereas casual riders favor weekends, particularly Saturdays. Summer months drive increased ridership in both groups, with August as the overall peak, highlighting the seasonal influence on cycling behavior.

Share
Visualizations were created in Tableau to support key findings from the analysis stage.
The visualizations are as follows;

Total Number of rides in 2025 (Member vs Casual):



Total Number of rides per Month (Member vs Casual):


Total Number of rides per Day (Member vs Casual):




Average ride duration (Member vs Casual):


Average ride duration per Month (Member vs Casual):


Average ride duration per Day (Member vs Casual):







Act

Recommendations
Launch weekend membership campaigns specifically designed to engage casual riders, leveraging their peak weekend activity to drive conversions. Casual riders are most active on Saturdays, while annual members ride more frequently on weekdays. Since casual riders also have longer average rides (22.21 minutes vs. 12.18 minutes), Cyclistic could promote the value of an annual membership specifically during weekend riding periods. For example, digital ads and in-app promotions could target casual riders on Saturdays with messaging emphasizing the benefits and potential value of switching to an annual membership.
 
Increased digital marketing during the Summer months. Casual riders are most active in August, likely capitalizing on peak summer conditions, while annual members reach their highest engagement in September. This staggered seasonality suggests opportunities for targeted campaigns, such as summer promotions for casual riders and early autumn incentives for annual members, to maximize ridership and support conversion efforts.

Promote the value and convenience of annual memberships to longer-duration riders. Casual riders consistently take longer trips, averaging 22.21 minutes compared to 12.18 minutes for annual members, indicating a preference for leisure or extended journeys. This behavior presents a clear opportunity: position annual membership as the ideal choice for those who seek flexibility and value on longer rides. Tailored campaigns can emphasize how “the more you ride, the more you save”, making membership a compelling upgrade for frequent, long-distance riders. 


Conclusion
This analysis demonstrates clear differences in how Cyclistic’s casual riders and annual members use the bike-share service. Annual members ride more frequently and primarily use the service on weekdays, while casual riders take longer trips and are more active on weekends. Both groups experience their highest levels of activity during the summer months, with August showing particularly high riding activity. These patterns present an opportunity for Cyclistic to target casual riders when they are most engaged with the service. By implementing weekend-focused promotions, increasing digital marketing during the summer, and highlighting the value of annual memberships for longer rides, Cyclistic can develop a more targeted strategy to encourage casual riders to become annual members and support the company’s long-term growth. 
