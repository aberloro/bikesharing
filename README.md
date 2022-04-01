# Bikesharing in NYC vs Des Moines

## Overview
 
### Background
Client has requested Tableau visualizations of NYC CitiBike bikeshare trip data to pitch to investors on a similar product for Des Moines, Iowa.

### Purpose
The purpose of these visulaizations is to share information with stakeholders to empower their decision to invest in the Des Moines bikesharing project.  This will be a deeper dive than the [Phase1](https://public.tableau.com/views/CitiBikeNYC_Phase1/NYCCitiBikeStoryPhase1?:language=en-US&publish=yes&:display_count=n&:origin=viz_share_link) report. 

The visualized data should tell the story of the NYC bikeshare business: how many users there are, who they are and what type of customer they are, when and where they ride, and what type of useage each bike sees. Also, stakeholders have requested specifics on the bike trips including duration of checkout, trips by gender by hour, and trips by user type and gender by day of the week. 

### Deliverables
 - Convert trip duration data to datetime format via Python
 - Create at least 7 visualizations for trip analysis
 - Create a Tableau Story and report for a presentation to stakeholders
 
### Resources
 - Data Sources: [citibike System Data](https://ride.citibikenyc.com/system-data)
 - Technology: [Tableau](https://public.tableau.com/s/), Python, Jupyter Notebook

## Results

### Overview of Code
 - Trip duration data in the [citibike resource](https://ride.citibikenyc.com/system-data) was converted to datetime format shown [here](https://github.com/aberloro/bikesharing/blob/main/NYC_CitiBike_Challenge.ipynb).
 - Visualizations for [Phase1](https://public.tableau.com/views/CitiBikeNYC_Phase1/NYCCitiBikeStoryPhase1?:language=en-US&publish=yes&:display_count=n&:origin=viz_share_link) and [Phase2](https://public.tableau.com/views/CitiBikeNYC_Phase2/NYCStory?:language=en-US&publish=yes&:display_count=n&:origin=viz_share_link) were done in Tableau Public. 

### [Story Point 1](https://public.tableau.com/app/profile/aurora.christensen/viz/CitiBikeNYC_Phase2/WhoRidesWhen?publish=yes): Who are the users?

![who](https://user-images.githubusercontent.com/93740725/161343097-6fa21d90-72fc-4de4-b45c-f9959942f827.png)

Users can be segmented by two purchase patterns: annual subscribers and per-use customers.  Both types of users reperesent an important part of overall bike rentals.  Annual subscribers are likely locals who use the bikes to commute as an excellent alternative to owning a car or storing and maintaining their own equipment.  Customers are likely tourists who are sight-seeing or locals who may be considering a subscription.  Over 80% of NYC users are subscribers, though use by customers during tourist season should also be planned for. 

Users can also be segmented by gender and by age to look at usage patterns.  By far, the largest user segment is male-subscribers, with the smallest segment being non-binary subscribers.  It is noteworthy that while the male and female user segments both tend to prefer subscriptions over per-use rides, the non-binary user segment prefers per-use rentals.  Looking at age, male and female ridership both peak around 30 years of age where non-binary users have a strong spike in ridership around 50 years old.  

Understanding these customer segments and the differences in their prefered style of bikesharing will help inform successful marketing and logistics planning when evaluating the proposed business in Iowa.  

 ### [Story Point 2](https://public.tableau.com/app/profile/aurora.christensen/viz/CitiBikeNYC_Phase2/WhoRidesWhen?publish=yes): Where do users ride?

![where](https://user-images.githubusercontent.com/93740725/161343112-203356e2-0a46-4400-b9ae-06d7b4e3eafc.png)

The most used citibike station for both pick-ups and drop-offs is Pershing Square North, better known as Grand Central Station.  This is the hub of NYC, access to this point gives access to all other parts of the city. 

The main transportation agency in Des Moines is DART, and their central station is located down town(1).  This will be an important stop for Des Moines bike share users. A new 33M railport represents a huge investment in the Des Moines transit infrastructure(2), and bikesharing would synergize with that budding tranisit ecosystem. 

Another important observation from these maps shows that there is close alignment between pick-ups and drops-offs at major stations in NYC, though it is not exact alignment. If this trend can be expected in Des Moines, bikes will have to be moved between stations during non-peak hours to ensure supply meets demand at high performing stations.  

### [Story Point 3](https://public.tableau.com/app/profile/aurora.christensen/viz/CitiBikeNYC_Phase2/WhoRidesWhen?publish=yes): When do users ride?

![when1](https://user-images.githubusercontent.com/93740725/161343144-bce70aae-3027-4381-994d-ef2fcb348671.png)

These visualizations show daily peak hours, as well as weekly.  Overall, most rides are booked during standard commute hours, with users favoring the afternoon commute for bike rentals.  While weekday rides are most prominant during cummute hours, weekend rentals are concentrated in the mid-mornings through 6-7pm.  The least popular times to rent are 3:00 and 4:00am, and maintenace and supply re-alignment should occur during these times. 

### [Story Point 4](https://public.tableau.com/app/profile/aurora.christensen/viz/CitiBikeNYC_Phase2/WhoRidesWhen?publish=yes): A closer look at who is out and when.

![when2](https://user-images.githubusercontent.com/93740725/161343173-c5a10a22-cf37-404a-8ca6-1258833c4c1a.png)

These heatmaps show usage per weekday/hour for customers segmented by gender and user type.  

Users segmented by gender show similar ridership patterns per weekday hour, with  most Monday-Friday rides being focused around standard commute times.  Most weeked rides being focused between brunch and dinner.  

Ther are two observations when looking at ridership based on user type and gender.  Non-binary riders are more active as customers than as subscribers.  Male and female riders are more active as subscribers than as customers. 

### [Story Point 5](https://public.tableau.com/app/profile/aurora.christensen/viz/CitiBikeNYC_Phase2/WhoRidesWhen?publish=yes): How long are the rentals?

![rideTimes](https://user-images.githubusercontent.com/93740725/161343202-7337bf60-eccc-4a1f-aa0f-45c099720cf2.png)

A look at checkout times shows us the amount of time for which a bike is rented, presented for all users, for users segmented by gender, and finally segmented by user type. 

Overall most rides were within 20 minutes and there were more quick 5 minute rentals than any other duration of checkout: nearly 150K rides were only 5 minutes. For most riders, this is one mile(3). The Des Moines team should look at what attractions and services are within one mile of their stations. Ten minute rides (2 miles) totaled just over 100k, 20 minute rides (4 miles) dipped to 45k rentals.  60 minutes rides dove off a cliff at less than 1k.  This tells us that emphasis should be placed on shorter rides in terms of marketing and station locations. 

The rental duration trendlines are similar when segmented by gender.  Male ridership peaks at 5 minutes, 7 for females, and 10 minutes for non-binary.  The trendlines change when you segment by user type.  Subscribers, as expected based on previous visualizations, have more total rides than customers.  Going a step further and filtering usertype by gender we see than the non-binary segment has far more customers than subscribers and their rides last 4x times longer.

### [Story Point 6](https://public.tableau.com/app/profile/aurora.christensen/viz/CitiBikeNYC_Phase2/WhoRidesWhen?publish=yes): How much use does each bike get?

![bikeUse](https://user-images.githubusercontent.com/93740725/161343386-a6582478-84b0-4ccb-952f-2bf6aafe05d9.png)

This final story point takes a look at how many rides each bike has seen. Presumably, bikes that have tallied up more rides will require maintenance sooner.  Total bike trips range from just below 500 to one.  The top 10 most frequently riden bikes are identified, as are the least used bikes.  

Looking at the bar chart tallying rides for each bike, the slope is generally gentle. This means most bikes are being rotated (either by users or by the citibike team), which keep usage relatively consistent per bike and improve maintenacne timelines.  The bikes with a higher trip count can be serviced during the off-peak hours identified earlier. 
 
## Summary
Most users are male subscribers riding during commute hours for short 5 minute trips (around a mile long.)  Overall, subscribers make up 81% of the user base, though customers purcahse longer rentals.  Drop off locations are closely matched with pick up locations, though they are not exactly matched so bikes will need to be transported from low-use to high-use stations and maintianed during the off-peak hours of 3-4am. 

### Limitations
This data has not been inspected for outliers. Looking at story point 1, there is a sharp spike in ridership for non-binary users born in 1969 which does not follow the other trendlines.  It bears investigation: can it be explained by a data collection issue or a local event that caused this spike in ridership for this user segment? Something else?

Another limitation of this data is the scope: only August.  August is a warm summer month where we could expect more folks to want a bike ride than take a taxi or train trip.  A look at data across a few years would illuminate any seasonal ridership patterns.    

### Additional Analysis 

The below visualizations were not part of the original project scope, but are needed to tell a complete story of the bikeshare business in NYC:
 - Users by type and gender (Story Point 1)
 - Trip count by age and gender (Story Point 1)
 - Checkout time by user type with age, gender and duration filters (Story Point 5)
 - Rides per bike bar chart (Story point 6)
 
Additional visualizations would provide more context to any similarities and differences between the NYC and Des Moines bikeshare buisness:

 - A look at routes, not just stations, would inform on user behavior with the bikes. By looking at the number of rides on the same route (same starting and ending location) we could see the split between rides for commuting vs tourism. This should be done for all users as well as with a breakdown into user types: subscribers vs customers. 
- A comparison of tourism economy between NYC and Des Moines.
- A comparison of car ownership, access to public transit, and commuting preferences across age groups in NYC and Des Moines.
- A camparison of annual weather patterns between the two cities.
- A look at ridership per month over a number of years to spot annual usage trends. An overlay of the annual tourism economy and annual weather patterns in each city would be helpful here too.  

#### References
(1) [https://www.ridedart.com/dart-central-station-transit-hub](https://www.ridedart.com/dart-central-station-transit-hub)

(2) [New railport set to make des moines a major train hub](https://www.kcci.com/article/iowa-new-railport-set-to-make-des-moines-a-major-train-hub/39139078)

(3) [How Long does it take to bike a mile](https://www.bikethesites.com/how-long-does-it-take-to-bike-a-mile/) 
