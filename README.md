# Payment Funnel Analysis

## Executive Summary
A significant number of subscriptions remain unpaid, indicating potential friction in the online payment process and negatively impacting revenue. This analysis identifies pain points within the payment portal and provides actionable recommendations to improve successful payment conversion using SQL and a data science notebook to build a product funnel analysis.

## Business Problem
The finance team has noticed that many subscriptions haven’t been paid for, so they reached out to the product team to understand whether there are friction points in the online payment portal and how these may be impacting the conversion rate (the percentage of subscriptions that successfully convert to a paid subscription).

![Payment Funnel Distribution by Order Year](payment_funnel_by_year.png)

![Year-over-Year Trends](yoy_funnel_trends.png)

---

## Methodology
- Exploratory Data Analysis (EDA)
- Product Funnel Analysis
- Data Visualization

## Skills
- SQL (CTEs, CASE statements, subqueries, window functions)
- Data Visualization
- Data Wrangling
- Data Cleaning
- Data Science Notebook
- Snowflake Data Warehouse

---

## Results & Business Recommendations

### Results

#### Payment Funnel Distribution by Order Year
This chart shows how subscriptions are distributed across payment funnel stages by order year, highlighting where users drop off and how engagement with the payment flow has evolved over time.

In 2019, all subscriptions remain in Payment Not Started, indicating no interaction with the payment portal. From 2022 onward, subscriptions are more evenly distributed across funnel stages, suggesting increased adoption of the payment workflow.

Despite this improvement, top-of-funnel drop-off remains significant each year, with many users failing to initiate payment. Only a minority of subscriptions reach the Complete stage, pointing to friction or abandonment within the payment journey. Both user-side and vendor-side errors persist, highlighting opportunities to improve checkout reliability and the overall payment experience.

![Payment Funnel Distribution by Order Year](payment_funnel_by_year.png)

#### Year-over-Year Trends in Payment Funnel Stages
This visualization tracks how subscriptions progress through the payment funnel over time, normalized by year to enable comparison independent of total subscription volume.

User engagement with the payment flow improves after 2019, with a declining share of subscriptions that never initiate payment. Participation in downstream funnel stages increases over time, indicating broader adoption of the payment process.

Payment completion rates show a steady upward trend, reflecting gradual improvements in conversion efficiency. Despite these gains, early-stage drop-off remains the largest friction point, with many users still failing to start the payment process. Error-related stages remain relatively small but persistent, highlighting opportunities to improve payment submission accuracy and third-party processing reliability.

![Year-over-Year Trends](yoy_funnel_trends.png)

#### Payment Error Distribution
This visualization shows the distribution of subscriptions with and without payment errors. While the majority of subscriptions do not encounter errors, a meaningful share experience at least one payment issue during the checkout process.

The presence of payment errors indicates opportunities to improve checkout reliability, including clearer validation during payment submission and more robust handling of third-party payment processing failures. Although errors are not the primary driver of funnel drop-off, reducing them could contribute to incremental gains in payment completion and overall user experience.

![Payment Error Distribution](payment_error_distribution.png)
---

## Business Recommendations
- Reduce friction on the payment entry page by supporting Apple Pay, Google Pay, or other alternative payment methods that minimize manual credit card entry and reduce user submission errors.
- Partner with the third-party payment processor to investigate vendor-side errors and define a plan to reduce payment failures.
- Work with the product team to increase the number of subscriptions that initiate the payment process. Since the largest drop-off occurs before users enter the payment portal, payment reminders, notifications, or proactive customer support outreach could significantly improve top-of-funnel conversion.
- Implement monitoring and alerting for payment errors and funnel drop-offs to track improvements over time and quickly detect regressions following product or vendor changes.

## Next Steps
- Investigate the error breakdown further to determine which errors are most common (user errors or vendor errors)
- Investigate why subscriptions aren't even starting the payment process. Is it a process issue on our side? Are customers forgetting?
