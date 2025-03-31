# Insights for a Strategic Merger in the OTT Domain

### Domain: Telecom & Streaming Services
#

#### Problem Statement

Lio, a leading telecommunications provider in India, is planning a strategic merger with Jotstar, one of the country’s most prominent streaming platforms. 

As part of the merger preparation, the management team at Lio wants to analyse the performance and user behavior of both platforms—LioCinema and Jotstar—over the past one year (January to November 2024). 

The management expects detailed insights into the following:

- Content Librery Analysis
- Subscriber Analysis
- Inactivity Analysis
- Upgrade and Downgrade Patterns
- Content Consumption Behaviour

The insights derived from this study will help the management make informed decisions and optimize content strategies post-merger, with the ultimate goal of establishing Lio-Jotstar as the leading OTT platform in India.
#
### Data Source: 
MySQL Database Files
#
### Action Taken

Step 1: Creating database with the SQL Text file on using MySQL Workbench. 

Step 2: Loading data in the Power BI Desktop environment using MySQL Database. 

Step 3: Checking the validity of the data, data type and exploring the dataset using Power Query's Data Preview option. 

The observation from this step was that the dataset has been cleaned previously and can be used for further transformation as required. 

Step 4: Updating the naming structure of the given tables to make the process of writing DAX functions easier. 

Step 5: Adding additional columns to the susbscriber table 'user_status', 'upgrade_status', 'changed_subscription_plan' and 'upgrade_transition' to prepare it for creating DAX Measurements in the next steps.

Step 6: Creating a table for susbscription plans and price, which was not provided in the initial data source. 

Step 7: Creating a date table that can be mapped to the date fields of the fact table in a later stage. 

Step 8: Creating relationships between the tables unders Model View tab using the Manage Relationship option.

![Image](https://github.com/user-attachments/assets/ed96b80c-8157-48b7-acc8-9fe8ed3e1268)


Step 9: Creating the DAX measures for both Lio Cinemas & Jotstar supporting further analysis.

#### DAX Measures

- Number of Subscribers
- Total Watch Time
- Average Watch Time
- Total Revenue
- Total Number of Content
- Percentage of Subscribers of Paid / Unpaid
- Percentage of Free Users
- Percentage of Subscribers Upgraded / Downgraded
- Percentage of Users Didn't Change Subscription 
- Percentage of Aactive / Inactive Users
- Month over Month Upgrade / Downgrade Change
- Month over Mont User Change 
- Month over Month Active / Inactive Change

The DAX measures have been stored in a separate Measure Table for each of the platforms. 

![Image](https://github.com/user-attachments/assets/c5d5534a-f335-4a8c-8271-de91764d38dc)

Step 10: Adding Calculated Columns to the Subscribers table for each of the platforms on the Table View tab, 

#### Calculated Columns

- Number of months before subscription changed & total amount spent by the user during this time period.

![Image](https://github.com/user-attachments/assets/04280b7b-4220-45e9-bd3c-1ed4cbe16827)

![Image](https://github.com/user-attachments/assets/0eba78bc-c783-46b3-a2dc-fb2e049c6331)

- Number of months since plan changed till end of observation date & total amount spent by the user during this time period.

![Image](https://github.com/user-attachments/assets/796c2290-2045-4f33-b942-6ddc75527368)

![Image](https://github.com/user-attachments/assets/fa80119b-2363-42af-ace4-b66e722f27d0)

- Number of month for active users who never chanhged the plan & total amount spent by the user during this time period.

![Image](https://github.com/user-attachments/assets/a9edb638-75e7-4c63-b5a5-004c5aad8eab)

![Image](https://github.com/user-attachments/assets/871b4129-81a9-4082-93f8-a7fcbfc0b7bb)


- Total amount spent by a subscriber during the observation period.

Step 11: Creating report visualisation at the Report View tab,

### Home Page Content

- Jotstar vs Lio Cinemas KPIs,
Total Revenue | Number of Users | Total Paid Users | Total Watch Time 

![Image](https://github.com/user-attachments/assets/3fb219cd-acea-4135-8ab6-46898a599b98)

- Percentage of Active vs Inactive users for both the platforms, 

![Image](https://github.com/user-attachments/assets/457745ec-46d8-4711-b347-5200b9ea97df)

- Number of users Upgraded vs Downgraded for both the platforms, 

![Image](https://github.com/user-attachments/assets/5731fe08-0a6c-441a-b2b2-c563329325f1)

- The Home Page has a header menu that redirects the report user to the following pages, 

##### - User Dempgraphy
##### - User Activity 
##### - Subscription Trend
##### - Watch Time Trend
##### - Platform Content 
#

There is a special menu button that redirects to a page that shows the relation between Watch Time and Upgrade and Downgrade trend. 

This would be discussed later under Special Page section.
#
![Image](https://github.com/user-attachments/assets/afbd58ff-790e-47b6-97cd-55adcaab582b)
#

#### User Dempgraphy ( Jotstar vs Lio Cinemas)

- Section 1:
An Area Chart that shows the user trend over months. 

- Section 2: 

A Bar Chart shows the user distribution in Tier 1, Tier 2 and Tier 3 cities. 

- Section 3: 

A Column Chart shows the user distribution by their age group, 18 - 24, 25 - 34, 35 - 45 and 45+.

![Image](https://github.com/user-attachments/assets/9c7e95ba-9d17-4eb3-8fe5-9868a48f7a66)

#

#### User Activity ( Jotstar vs Lio Cinemas)

- Section 1:
A Stacked Column Chart shows the active vs inactive user distribution by their age group, 18 - 24, 25 - 34, 35 - 45 and 45+.

- Section 2:
A Stacked Bar Chart shows the active vs inactive user distribution over Tier 1, Tier 2 and Tier 3 cities. 

- Section 3:
A Stacked Column Chart shows the active vs inactive user distribution by subscription plans.

![Image](https://github.com/user-attachments/assets/22db4cef-e56d-45b1-abed-20aef60538c3)
#

#### Subscription Trend ( Jotstar vs Lio Cinemas)

- Section 1:
A Column Chart shows the distribution of users by different subscription plans. 

##### Jotstar - Free, VIP & Premium
##### Lio Cinemas - Free, Basic & Premium

- Section 2: 
A Tree Map shows the paid user distribution by age groups, 18 - 24, 25 - 34, 35 - 44 & 45+.

- Section 3: 
A Bar Chart shows the paid user distribution by city, Tier 1, Tier 2 & Tier 3. 

![Image](https://github.com/user-attachments/assets/a476b745-499f-4e00-9315-64e92f9c8e07)
# 

#### Watch Time Trend ( Jotstar vs Lio Cinemas)

- Section 1: 
A Tree Map showing the average watch time of each of the polatfrom for all the users. 

- Section 2: 
A Tree Map showing the watch time distribution as per the age group, 18 - 24, 25 - 34, 35 - 44 & 45+.

- Section 3: 
A Dougnut Chart showing the percentage wise distribution of watch time among Tier 1, Tier 2 and Tier 3 cities. 

- Section 4: 
A bar chart shows watch time distribution by the device used by the user, Mobile, Laptop & TV. 

![Image](https://github.com/user-attachments/assets/d9073faf-a86d-449d-97a7-0eacdfc34aec)
#

#### Platform Content ( Jotstar vs Lio Cinemas)

- Section 1: 
A Tree Map shows the number of content for each of platforms.

- Section 2: 
The platfrom content can be divided between 2 categories, Content Type and Language. 

A Column Chart have been used to show the content distribution among types, Movie, Series and Sports. 

A Bar Chart have been used for showing the content distribution among multiple languages. 

Both the charts have been stored using Bookmarks as 2 different views and there are 2 buttons on the page to switch the views.

#### By Content Type,
![Image](https://github.com/user-attachments/assets/d6a82235-2eb8-4b5d-9c8e-c7dd2aca6242)

#### By Language,
![Image](https://github.com/user-attachments/assets/f1028abf-4943-4afa-a0d8-37459d052fdb)
#

### Drill Down Pages
In order to give a more granular insights, the folloing drill-down pages have been used,

##### - Subscription Trend
##### - Revenue Trend
#

#### Subscription Trend
This drill-down page can be redirected to by right clikcing on the Tree Map on the home page.

There 2 pages for each of the platforms. Each of the pages have the following sections, 

Section 1: 
A Bar Chart shows the upgrade patterns based on the plans switched. 

For Jotstar,
- Free - VIP
- Free - Premium
- VIP - Prime

For Lio Cinemas, 
- Free - Basic 
- Free - Premium
- Basic - Premium

Section 2:
A line chart shows the downgrade trend over the time. 

![Image](https://github.com/user-attachments/assets/77d4062d-b56b-45bd-9032-59fe1e6fae3f)

![Image](https://github.com/user-attachments/assets/51414ca5-bb53-48f8-b3cb-b518d95a7a83)
#

#### Revenue Trend
This drill-down page can be redirected to by right clikcing on the Revenue KPI card. 

This page has the following sections, 

Section 1: 
A Tree Map shows the total revenue for each of the platforms. 

Section 2:
2 Line Charts show the Revenue Trend over the observation time for each of the platforms. 

![Image](https://github.com/user-attachments/assets/bb44e272-da6d-472c-9308-3160876dded3)
#

### Special Page ( Jotstar vs Lio Cinemas)

As mentioned earlier, on the Home Page there is a button that redirects to this page, 

![Image](https://github.com/user-attachments/assets/ad2d5bfd-29f8-4272-9a8a-92794233d862)

This page has to sections, 

Section 1: A Column Chart, shows the watch time trend over the time. To understand the change in the number of active users over the same time period, a trend line has been drawn.

Section 1: A Column Chart, shows the watch time trend over the time. To understand the change in the number of inactive users over the same time period, a trend line has been drawn.

![Image](https://github.com/user-attachments/assets/594df19f-7eff-4075-962f-65a641534e64)
#

Step 12: Tooltips has been used throughout the report for better granular data insights.

Step 13: The report was then published to the Power BI Service. 

### Insights

#### Insight 1,
- The total revenue of Jotstar is 161% higher than Lio Cinema.
- The total number of users of Jotstar is 76% lower than Lio Cinema.
- Jot star has 60% less paid user than Lio Cinemas. 

From the above 3 observation the insight we can get is, although the total number of user and paid user is higher for Lio Cinema, Jotstar has much larger volume of revenue. 

Jotstar's premium pricing is one of key matrix here. 

#### Insight 2,

- For Jotstar 9.74 % of the users upgraded to a highr value subscription plan. For Lio Cinema the number is 2.26%. 

- For Jotstar 6.15% user downgraded their subscription, the number is 11.37% for Lio Cinema. 

From the above 2 points we can observe that more of the Jotsar users upgraded to a higher valued plan despite the cost of susbscription is higher than that of Lio Cinema. 

This is another contributing factor for Jotstar's higher revenue. 

#### Insight 3,

- 55% of Jotstar's users are from Tier 1 cities. Where are for Lio Cinemas 42% of the users are from Tier 3 cities. 

- 68% users of Jotstar are from the age range 25 to 44. For Lio Cinemas 72% of the user are from the age range 18 to 34. 

So, from the chart we can safely say that Jotstar has more users on the highr side of the income level. Also, these users are either has started getting sufficient disposable income or already are established professionals.  

#### Insight 4,

- For Jotstar 85% of the users are active on the platform, where as the number is 55% for Lio Cinemas. 

- For Lio Cinema the Free users are more active than the paid users. For Jotstar the trend is opposit, the higher is the subscription package the highr is the activity. 

Most of these active users are from Tier 1 city of the age range 25 to 44 for Jotstar. For Lio Cinema the active users are from Tier 3 and Tier 2 cities and of the age range 18 to 34. 


#### Insight 5,

The subscription trend for the users follow the same pattern as the active users or all over user base of both the platforms. 

This is the primary reason for Jotstar to have better revenue that Lio Cinema. 

#### Insight 6,

- For Jotstar total 3.33% free users moved to paid plan where as 6.26% paid user moved to even highr value subscription plan. 

- For Lio Cinema 1.5% free users moved to paid plan whare as 0.74% paid user moved to even highr value subscription plan. 

- Over the observation period the downgrade trend reduced by 74% for Jotstar. For the same time period for Lio Cinema the downgrade trend increased by 53%

#### Insight 7,

The watch time trend says the same story as the user activity or the subscription trend. 

So, from User Activity, Subscription Trend and Watch Time Pattern we can salfely say that the content on Jotstar are engaging for the young urban population. 

On the other hand the content of Lio Cinema is engaging for the younger generation of Tier 3 and Tier 2 cities. 

#### Insight 8,

- All over number of content is higher in Jotstar by 89%. 
- Both the platforms have similar number of movies. 
- Jotstar has 175% more series type content than Lio Cinema. 
- Jotstar also hs 600% more sports content than Lio Cinema. 

- Jotstar has content in 9 regional languages and Lio Cinema has 6. 
- Most of the Jotstar content are in English and for Lio Cinema it's Hindi. 

#### Insight 9,

- For both Jotstar and Lio Cinema, the average watch time reduced from January to November. 

- For Jotstar the number of active user increased and inactive user decreased from January to November. 

We can say for Jotstar although the overall watch time decreased the number of active user increased. 

- For Lio Cinema, both active and inactive users increase from January to November. 

We can say that the over all activity of Lio Cinema remain almost same throughout the year.

#### Insight 10,

- Although Jotstar made better revenue than Lio Cinema, the total revenue saw a constant decline over the time period. 

- For Lio Cinema from January till September the revenue saw a constant growth and then a significant decline from October and Novmber.


#### Note: 
- As I don't have a paid subscription to Power BI Service, I couldn't share the report here at GitHub. 
- I am uploading the pbix file, for your ease of understanding. 
