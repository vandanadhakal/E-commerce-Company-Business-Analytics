# E-commerce-Company-Business-Analytics
Understand how well an e-commerce company’s website is converting product page views into purchases and the retention rates for each month.

## Objective
To understand how well an e-commerce company’s website is **converting product page views into purchases** and the **retention rates for each month**.

## Summary
➔	Methods/Techniques: Processed data using filters, pivot tables, VLOOKUP, formulas, acquisition cohort formulation and funnel metrics. Conversion rate, retention rate and average retention per cohort age is determined.

➔	Results: Only 29% of users who view the company website added products to the cart and 36% of them made purchases. 7.3% of users who made a purchase initially are coming back next month to make a purchase, which reduces to < 1% by 3rd and 4th month. 

➔	Recommendations: Suggested the company to check their user interface for any difficulty in adding products to the carts and analyze if spending more on marketing/promotional offers could attract more traffic to the website.


### Project Description
**Dataset** in this project contains the following columns:

•	`user_id`: unique customer IDs

•	`event_type`: the type of activity by the user

•	`category_code`: category of the product being viewed or purchased

•	`brand`: company that makes the product

•	`price`: price of the product, in USD

•	`event_date`: date of the user activity, in YYYY-MM-DD format

Each row represents an activity, or event, by a user on the company’s website. Each time a user views a product page, opens their shopping cart, or completes a purchase, the event is captured in the activity logs.

**`Conversion Rate`**

Conversion rate required to see how the customer moved from one stage (event) to another. Total conversion rates and conversion rates to the next step are calculated to see the path customers are taking as they interacted with the business. The users activity (event_type) data and the count of unique users (user_id) who went through these events are used to understand the conversion rate between these events.

**`Retention Rates`**

Retention rate tells how many users from a cohort have remained active compared to the initial number of users. Retention rate calculation required to establish cohorts and the cohort age only for the users who made purchases. Only the purchase event data are taken from raw user activity to make this analysis. The first month a customer made a purchase is used to form user cohort. Cohort age is calculated as the difference in months between the first purchase month and subsequent purchase months.

<Project>


### Data Preparation
The column with information on the users activity (event_type), the date the events occurred (event_date) and the unique id of the user (user_id) are used for analysis and calculation.

1. `Conversion Funnel`: Conversion Funnel – The calculation of conversion funnel required the need to understand the flow of customer events i.e ‘view’ -- ‘shopping_cart’ -- 'purchase'. Pivot table is used to calculate the total count of customers moving from one stage to another. **Total Conversion Rate** at a stage is calculated as the ratio of number of users at the stage to the number of users at ‘view’ stage. **Conversion to Next Stage** at a stage is calculated as the ratio of number of users at the stage to the number of users at the previous stage.

2. `Cohort Analysis`: Acquisition cohorts are developed based on the month of a user’s first purchase. Since the company wants to track cohort metrics month by month the first month a user made a purchase is used to form user cohort. So, only the purchase event data is used to calculate the retention rates. The **cohort age** is chosen as months between the first purchase month and subsequent purchase months.

3. `Retention Rate`: **Retention Rate** for each cohort (cohort age >0) is calculated as the ratio between the number of unique users who made the purchase at the cohort age compared to the first month the users made the purchase. The **Average Retention Rate per Cohort Age** is the average of the retention rates per cohort. Only the first purchase month data is available for 2021-02 cohort, so the retention calculation is skipped for this cohort.


### Conclusion

**`Conversion Funnel`**
   
a.	Only 29% of users who view the company website are adding products to their shopping cart. Maybe users have some issues/difficulty adding products in the cart with the website interface. It will be worthwhile to check the user interface for any issues or inconvenience for the customers.

b.	36% of users who added products to the cart are making purchases. It could benefit to send an email to the users reminding them of products in the cart.

<image>

**`Retention Rates`**
   
a.	On an average 7.3% of users who made a purchase initially are coming back next month to make a purchase.

b.	This percent reduces to less than 1% by 3rd and 4th month after the first purchase month.

c.	It could be worth to check how the user interface is in-terms of how easy it is to make purchase after viewing the products.

d.	Further study should be done to see if spending more on marketing or providing offers could attract more traffic to the website.

<Image>

<Image>

