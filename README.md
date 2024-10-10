![intro-image](https://github.com/user-attachments/assets/65444574-fdfe-46fb-bab2-47af716f1658)

You can read the article for this analysis [here](https://medium.com/@melodyphyo/analysis-of-uber-requests-trip-status-between-airport-and-city-on-weekdays-796ab7337906)

# Introduction
I selected the Uber request dataset from Kaggle to analyze for my portfolio. The dataset focuses on trips between the city and the airport during weekdays, providing insights into travel patterns and demand fluctuations.

# Purpose of This Analysis
To express and highlight the rate of trip status
# Data
Data was pulled from a dataset on Kaggle

# Data Wrangling

* I removed unnecessary columns, such as driver_id and drop_timestamp, as they were not relevant to this analysis.
* Before altering the data type of Request timestamp, I first cleaned and modified it using a lambda function.
* I then created three new columns — Day, Hour, and Time Slot — based on the transformed Request timestamp to better analyze time-based trends.

  Refer [here](Data-Wrangling_ss) for data wrangling process

# Data Analysing and Visualizing:
## Percentage of the Order Status

![Percentage_of_the_Order_Status](https://github.com/user-attachments/assets/7cf10a9b-1099-4630-ab0a-633c02032ef0)


**Key Takeaways:**

* Completed trips at 42% demonstrate a moderate success rate but leave room for increasing efficiency and reliability.
* No Cars Available, Making up 39% of requests, this high percentage suggests a notable issue with car availability.
* Cancelled, At 19%, this segment shows the fraction of rides that were cancelled by users.

## Frequency of Status at Pickup Points

![frequency-of-status-at-pickup](https://github.com/user-attachments/assets/62a8184e-e1ca-4002-bb9e-1cfe18b10a06)


The bar chart highlights distinct patterns at the two pickup points. At the Airport, car availability is a significant issue, leading to a high number of “No Cars Available” requests, whereas the City experiences better completion rates but also a higher rate of user cancellations. These insights can help in addressing service challenges and improving customer satisfaction at both pickup points.

## Peak number of requests on a particular day (in % and in values)

![two-subplot-Peak-number-of-requests-on-particular-day](https://github.com/user-attachments/assets/223eb7a1-05c8-4c2b-980d-fcb652bacefc)


**Insights:**

Overall, the data suggests that the peak number of requests is relatively consistent throughout the week, with only minor variations.

## Counts of “Cancelled Rides and No car available” by Days

![two-subplot-count-of-cancell-ride-and-no-car-available-by-days](https://github.com/user-attachments/assets/83fedd46-86be-4b81-946b-d2273d6e2675)


**Top Bar Chart: Count of Cancelled Rides by Day**
**Bottom Bar Chart: Count of No Cars Available by Day**
**Insights:**

* Car Availability Issues: There is a significant challenge in car availability at the beginning of the week, particularly on Mondays and Wednesdays, which could indicate a supply issue or higher demand on these days.
* Consistency in Cancellations: The number of cancellations does not vary much, suggesting that cancellations might not be directly influenced by car availability issues. Instead, other factors like customer behavior or external conditions could play a role.
* Targeted Improvements: Efforts to enhance car availability might focus on early in the week to reduce the high counts of no cars available instances. Addressing these issues could potentially improve overall service reliability and customer satisfaction.

## Trip Status Distribution by Pickup Point and Time Slot

![catplot](https://github.com/user-attachments/assets/127c0b60-73e8-43af-a1a1-7b9fe456f17a)


**Insights:**

**Trip Completed:**

* Airport Pickup Point: The highest number of completed trips occurs in the Morning time slot, followed by Evening and Late Night.
City Pickup Point: The highest number of completed trips occurs in the Evening time slot, followed by Morning and Late Night.
Cancelled:

* Airport Pickup Point: The highest number of cancellations occurs in the Morning time slot, with very few cancellations in other time slots.
City Pickup Point: The highest number of cancellations occurs in the Evening time slot, followed by Late Night.

**No Cars Available:**

* Airport Pickup Point: The highest number of instances where no cars were available occurs at Night, followed by Late Night and Early Morning.
* City Pickup Point: The highest number of instances where no cars were available occurs in the Evening, followed by Late Night and Morning.
  
**Summary**

* Morning: High number of completed trips and cancellations at the Airport.
* Evening: High number of completed trips and cancellations in the City, and high instances of no cars available.
* Night: High instances of no cars available at the Airport.
* Late Night: Consistently high across all statuses, especially for no cars available at both the Airport and City.

# Insights
**Cancellation Insights:**

* Day-wise Analysis: Cancellations are relatively consistent across the week, with a slight increase on Tuesdays and Fridays. The lowest cancellations occur on Mondays and Thursdays.
* Time Slot Impact: Morning cancellations are high at the Airport, while Evening cancellations dominate in the City. This suggests peak times when users might find themselves canceling due to possibly unfulfilled expectations or delays.
**Car Availability Insights:**

* Day-wise Analysis: Mondays and Wednesdays face the highest instances of cars being unavailable, indicating a potential gap between demand and supply. Fridays show the least instances of unavailability, suggesting either lower demand or better management of resources.
* Time Slot Impact: The Night and Late Night slots face significant car unavailability, particularly at the Airport. In the City, the Evening slot is most affected. This may indicate higher demand during these times or insufficient car supply management.
  
# Conclusion
The mornings and late nights at the Airport, along with the evenings in the City, are particularly problematic. These insights suggest that addressing car availability during these peak times could greatly improve service efficiency.

