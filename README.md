# Social_Media_Ad
This project analyzes social media ad performance using EDA to evaluate customer behavior, conversion rates, cost efficiency, and campaign effectiveness. Insights on user journeys, time to purchase, ad formats, platforms, and ROI support data-driven marketing optimization and budget allocation.

**Project Outline**

_Business Function:_
Retail & Marketing

_Audience/ Stakeholders:_
Marketing Manager, Growth Team, Paid Media Team

_Decisions Supported:_
Budget allocation, campaign optimization, platform prioritization

_Business Problem_
Marketing teams lack visibility into which ads, platforms, and audience interests drive 
conversions, leading to inefficient budget allocation and suboptimal ROI.

_Success Metrics / KPIs_

* Conversion Rate
* Cost per Conversion (CPA)
* Click-Through Rate (CTR) by ad
* Purchase Frequency

_Objective_

* Customer Behavior Analysis 
* Campaign Performance Evaluation
* Cost Efficiency Suggestions

_Dataset:_ Social Media Advertisement Performance
https://www.kaggle.com/datasets/alperenmyung/social-media-advertisement-performance?select=campaigns.csv

_Tools Used:_ Snowflake, Jupyter, SQL, Python

_Methodology	_
* Data cleaning and validation in Snowflake
* Feature engineering (time to purchase, funnel stage)
* Exploratory Data Analysis in Python
* Funnel analysis
* Aggregations and KPI calculations

---------------------------------------

**Business Insights Summary**

This exploratory data analysis evaluates customer behavior across social media campaigns, ad performance by format and platform, and cost efficiency.
Key findings show that purchases cluster later in the funnel (median ~29 days), Stories ads outperform other formats, and campaign ROI varies significantly, which highlights opportunities for budget reallocation.

Success Metrics / KPIs
Conversion Rate
Cost per Conversion (CPA)
Click-Through Rate (CTR) by ad
Purchase Frequency

**Key Findings**

_Customer Behavior_

1. Identify purchase distribution by day of week and time of day
   
Although the impression distribution is even throughout the week, the purchase distribution peaks on Thursdays and Fridays and purchase behavior is the weakest on Tuesdays and Wednesdays. The purchase behaviors are the strongest in the morning and second at night.

2. Analyze the user journey to identify how many touchpoints occur before purchase
   
On average, users experience 0.08 recorded touchpoints prior to purchase, indicating that most conversions occur without multiple tracked interactions. The maximum observed was 2 touchpoints, suggesting a relatively short or under-tracked decision journey.

3. Measure time from impression to purchase
   
The median time to purchase is 29 days, with most purchases occurring between 11 and 43 days after first impression. This suggests that remarketing and longer attribution windows are critical, as conversions often occur weeks after initial exposure.



_Campaign Performance_
1. Compare performance across platforms
   
The dataset contains social media campaigns on Facebook and Instagram. On average, customers purchase from ads on Facebook within 29.018018 days after impression, and 27.565217 days on Instagram. Instagram conversions occur around 1.5 days faster on average than Facebook, suggesting a slightly shorter decision cycle on Instagram, though overall behavior is similar across platforms.


2. Calculate purchase event percentage (conversion rate)

The conversion rate is calculated as the number of purchase events divided by the number of impressions, multiplied by 100 to express the result as a percentage:
Conversion Rate = (Purchase Events / Impressions) × 100
To accurately evaluate individual ad performance, conversion rates are grouped by AD_ID, ensuring that each ad’s effectiveness is measured independently rather than aggregated at the campaign or platform level. This approach allows for more precise comparisons across ad creatives and formats and supports data-driven optimization decisions.
Grouping by ad ensures that high-performing creatives are not diluted by lower-performing ads within the same campaign, enabling more targeted budget reallocation and creative optimization.


3. Identify highest-performing ad types
   
Out of the 200 ads, Stories have the highest conversion rate of 0.53 and image has the lowest conversion rate of 0.47. Stories ads outperform Images by 6%, suggesting short-form, immersive formats drive higher intent.

4. Evaluate effectiveness by user interest segment
   
While overall conversion rates are low across interest segments, News, Fashion, and Art outperform others, indicating higher intent audiences despite similar user volumes. These segments are strong candidates for budget prioritization or tailored creative.

_Cost Efficiency_
1. Calculate cost per conversion and identify high-ROI campaigns
   
Campaign 42 demonstrates strong efficiency, with conversion costs as low as $82.48, while Campaign 46 shows severe inefficiency at $18,804.75 per conversion. This gap suggests immediate opportunities for budget reallocation, creative refresh, or campaign pausing.

_Key Recommendations_

* Reallocate budget toward Stories ads and Campaign 42–like structures
* Extend attribution windows and remarketing efforts beyond 30 days
* Reduce spend or re-optimize high-CPA campaigns.
* Focus targeting on News, Fashion, and Art interest segments
