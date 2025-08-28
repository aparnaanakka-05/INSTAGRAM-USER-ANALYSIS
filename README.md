# Instagram User Analytics using SQL

## Overview
This repository contains an analytical study of Instagram user data using SQL.  
The goal of this project was to write and execute queries that transform raw data into actionable insights about users, engagement, hashtags, and platform activity.  

By running a series of carefully designed SQL queries, I was able to uncover user behaviors, platform trends, and patterns that can guide decisions such as scheduling ad campaigns or identifying unusual activity on the platform.  

---

## Objectives
The key objectives of this project were to:
- Identify the five oldest users on Instagram  
- Find users who have never posted a single photo  
- Determine the winner of a contest and provide their details to the team  
- Retrieve the top five most commonly used hashtags on the platform  
- Identify the week when most users registered on Instagram  
- Provide insights on the best time to schedule ad campaigns  
- Calculate the average number of posts per user  
- Compute the ratio of total photos on Instagram to the total number of users  
- Detect potential bot accounts, i.e., users who liked every single photo on the platform  

---

## Tools and Technologies
- SQL for querying and analysis  
- MySQL (or specify the database you used)  
- Dataset simulating Instagram data (tables for users, photos, likes, hashtags, etc.)  

---

## Approach
Each query was designed to answer a specific analytical question:  

1. *Oldest Users* – Sorted registration dates to find the five earliest registered accounts.  
2. *Inactive Users* – Selected accounts that exist but have not posted any photos.  
3. *Contest Winner* – Queried contest-related tables to identify the winner and retrieve details for the team.  
4. *Top Hashtags* – Counted hashtag frequency to find the five most commonly used ones.  
5. *Registration Week Trends* – Aggregated registration data by week to identify the busiest sign-up period.  
6. *Ad Campaign Scheduling* – Analyzed usage patterns to recommend the most effective times for running ads.  
7. *Average Posts per User* – Calculated the mean number of posts across the platform.  
8. *Photo-to-User Ratio* – Computed the total number of photos divided by the total number of users.  
9. *Bot Detection* – Flagged accounts that liked every single post, indicating non-typical user behavior.  

---

## Sample Query
```sql
SELECT hashtags.tag, COUNT(*) AS usage_count
FROM hashtags
GROUP BY hashtags.tag
ORDER BY usage_count DESC
LIMIT 5;
