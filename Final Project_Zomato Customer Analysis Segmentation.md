# **Final Project: Zomato Customer Analysis Segmentation**

**Focus on Customer Analysis**

https://public.tableau.com/views/FinalProject_17223692660750/Story1?:language=en-US&publish=yes&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link

Version 1 

Submitted by: Lourna Jane Reyes

Submitted on: July 19th, 2024

**Introduction:**

As part of our curriculum at TripleTen, Business Analytics students are tasked to showcase self-progress on Business Analytics through the final project. This would cover acquired knowledge on the whole process of business data analytics which includes but is not limited to data cleaning and processing, analysis and visualization. The final project will be a simulation of a real-world process of project assignment. Through the task, tools and knowledge acquired from the whole bootcamp shall be creatively utilized with the freedom of tool selection under the supervision of a Team Lead that mimics the analytics organizational field. 

**Problem Description**: (*source:* [*TripleTen module*](https://tripleten.com/trainer/bi-analyst/lesson/3d4c5ff8-01b8-4f46-a9a1-f284028127d5/)*)*

*You've been hired as a junior analyst for Zomato. Zomato is a multinational restaurant aggregator and food delivery company. As your first assignment in the onboarding process you’re given several test datasets to analyze the business performance of restaurants and customers registered in the service.*

*BI-Analytics Team in Zomato usually performs 3 types of analysis:*

- *Customer Analysis Segmentation: who are Zomato’s customers? What segments can we split them into? What is their purchasing behavior?…*
- *Restaurant Analysis: What restaurants are popular? What restaurants generate the highest revenue? Why?…*
- *Sales Analysis: Dynamics of sales/revenue overtime, main KPIs, change in distribution of sales and so on…*

*Your Team Lead expects you to perform one type of the analysis as well. Choose 1 out of the 3 areas to focus on and build your research plan. At the end of your onboarding process, you should present the dashboard related to the area as well as the main key points of your analysis in the format of report or presentation.*

*Data*

[*Zomato data.zip*](https://practicum-content.s3.us-west-1.amazonaws.com/data-eng/BIA/Dataset/Zomato data.zip)

*Download the archive with the test data given by your Team Lead. You’ll find 5 tables there:*

- *food*
- *menu*
- *orders*
- *restaurant*
- *users*

*It should be more than enough for you to complete your onboarding assignment, there is no need to use additional information. You may use one or several tables from the database, depending on your goal. You may join the data as you wish.*

**Research Plan:**

Your decomposition should include a detailed and structured research plan. What questions do you want to answer with your dashboard? What hypotheses do you have? What visualizations will be used? How do you need to work with the data prior to assembling the dashboard?

Process:

1. Analyzed the project agenda. 
2. Downloaded data from TripleTen website. Processed the zip file.
3. Explore the tables.
   1. Data clean up.
   2. Data on the *orders* table had to be converted to the correct currency used. Converting two (2) data entry from usd to inr using an estimated 1:84 exchange rate.
   3. Eliminating the zero “0” on the order ID for *orders* table to presumptively eliminate any issues.
4. Decide on study focus: 
   1. Due to the interesting volatility of consumer behavior, this analysis will focus on Customer Analysis in order to come up with a set of recommendations in pursuing the market and potentially inducing business growth that is data based.
5. Create analysis guide
   1. Questions to answer
   2. Hypothesis 
      1. Research on hypotheses through different online articles and publications to support this study. 
      2. Revised hypotheses based on research outcome. 
6. Analysis and Visualization
7. Recommendation

Agenda and Questions to be answered:

1. Customer demographics
   - Age group 
   - Gender
   - Marital Status
   - Occupation
   - Monthly Income
   - Educational Qualifications
   - Family Size
2. Spending habits/Purchasing Behavior
   - Average spending per order 
   - Type of cuisine mostly ordered 
   - Do customers order food only or with beverages? 
   - Which city did the customers spend the most on? (both qualitative and quantitative)
   - Peak day for orders 
   - Correlation of high ratings with order count
   - Correlation of cost with order count



Data Description:

Link to data: https://drive.google.com/drive/folders/1I7j7BnWCElOudNgc1aLObn1RhCEDBYR7?usp=sharing

​	For the purpose of Customer Analysis, this study will utilize the following tables in order to test our hypothesis. 



​	*users* Table - data on Zomato users



​	*User_id* - unique user identifier

​	*Name* - name of user

​	*Email* - email address of user

​	*Password* - user’s Zomato password

​	*Age* - user’s age

​	*Gender* - user’s gender

​	*Marital status* - user’s marital status

​	*Occupation* - user’s occupation

​	*Monthly income* - user’s monthly income

​	*Educational qualifications* - user’s educational attainment/status

​	*Family size* - user’s family size





​	*orders* Table - data on Zomato orders



​	*order_id* - unique identification of each order

​	*order_date* - date of order

​	**weekday_num* - **extracted data** from *order_date* to retrieve weekday number

​	*sales_qty* - quantity of items per order

​	*sales_amount* - total cost of order

**sales_amount_inr* - **extracted data** from *sales_amount* to fix data error and align currency on all sales amount 

*currency* - currency of transaction/payment

*user_id* - unique user identifier of the customer who placed the order

*r_id* - unique restaurant identifier of the restaurant where the order was placed





​	*restaurants* Table - data on Zomato restaurants



*id* - unique restaurant identifier

*name* - name of restaurant

*city* - city where the restaurant is located

*rating* - current customer given rating of the restaurant

*rating_count* - categorical amount of ratings the restaurant was given

**cost_curr* - **process data** that shows the currency of the average cost of food of the restaurant

**cost_num* - **processed data** that shows the amount of the average cost of food of the restaurant

*cuisine* - type of cuisine the restaurant serves

*lic_no* - license number of the restaurant

*link* - link to restaurant’s Swiggy website

*address* - restaurant’s complete address

*menu* - restaurants menu file but unlinked to the source



Remarkable notes:

1. Whole project and general data:
   - No description of the data was provided. 
   - Context of data was not fully disclosed. (ie. location is in India, currency is in Rupees.
   - Seems like users are non-Indians by the names but restaurants are in India
2. Users Table:
   - Monthly Income is categorical
   - No data on area of residency or nationality
   - There’s data on family size but no data whether head of family
3. Orders Table:
   - An outlier of USD in the data
   - No data on time of the day of order. 
4. Restaurants Table:
   - Restaurant websites are from Swiggy– Zomato’s competitor
   - Link to menu seems to be unlinked access



Hypotheses:

1. There would be more female, single, lower income bracket, higher education and smaller family size individuals who use Zomato.

According to Statista’s [Gender Distribution of quick service restaurant delivery app users in the United States study](https://www.statista.com/statistics/1246881/gender-of-restaurant-delivery-app-users-by-company-us/#:~:text=Gender of QSR delivery app users in the U.S. 2021%2C by company&text=In January 2021%2C the gender,even across all seven companies.) by January 2021, 4 out of 7 of the delivery apps have at least 50-50 distribution of female to male distribution. The highest is Instacart with 66% female users compared to 34% of male users. The age group 18-29 make up most of the users that order food from delivery apps according to a [research conducted by Zion & Zion](https://www.zionandzion.com/research/food-delivery-apps-usage-and-demographics-winners-losers-and-laggards/). This also supports the hypothesis that most users are single. However, the same study shows that the lower income level actually uses food delivery platforms and makes up 51.6% of the users. Meanwhile, a [comprehensive analysis](https://www.linkedin.com/pulse/unveiling-insights-comprehensive-analysis-food-delivery-harry-chang-x937c/) published on LinkedIn found that users with higher income tend to spend more than lower income groups. It also found that spending of users without kids is significantly higher than users with kids, which may be a fundamental basis that smaller family size individuals use delivery apps more. Equitable distribution was found in the educational attainment among users was found in a study conducted in [The new normal: the adoption of food delivery apps](https://www.emerald.com/insight/content/doi/10.1108/EJMS-03-2023-0021/full/html#:~:text=There was an equitable distribution,of other food delivery apps.). 



2. Average spending would be around INR 500*.

According to a study performed in India, 34% of the sample spends less than INR500 while 29% spends between INR500 and INR1000 when they dine out. 



3. Indian food would be the most sellable cuisine.

As staple food would commonly sell best at any local area, [Deccan Herald](https://www.deccanherald.com/lifestyle/food-and-drink/how-india-ordered-on-swiggy-zomato-2023-2825386) announced that Biryani is declared to be the most ordered dish in Zomato for 202

4. Food would comprise most of the orders, less beverage.	

5. Highest spending will be in the Mumbai or Delhi area. 

According to Ken Research’s study published in 2020, Bengaluru, Delhi NCR, Hyderabad, Mumbai and Pune have the highest revenue for the food delivery apps industry.



6. Peak day would be on weekdays.

It appears that the lunch and dinner time is the peak time for online food delivery app orders according to a [study conducted by DoorDash](https://about.doordash.com/en-us/news/doordash-unveils-what-and-how-consumers-have-been-eating-and-drinking-in-2023), but alcohol peaks orders during Friday and Saturday!

​	

7. The higher the rating the more customers would prefer the restaurant.

In the same study above, what DoorDash found is that users in 2023 prefer low cost over good experience when choosing a restaurant to order from.



Analysis and Visualization:	

Collected data shows that customers range from 18-33 years old and the most users in this data set is **23-year-olds**. Early 20s to Mid 20s are where most of the users are coming from. Contrary to the hypothesis, Zomato users are mostly **male** making 57.22% of the users. 53.36% are **students** (who are mostly no income earners) and is significantly more than the 30.41% employee. This study shows that most users are **single** encompassing almost 60% of users and they have **high educational qualifications** who hold a college degree at 45.61% and post-graduate degree at 44.85%. Most users belong to a **family size of 3**, but there is no data on whether they are the head of the family and whether they are living with the family. Almost half or 48.20% of the customers in this data set declared **no income**. 



![img](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcGoaPTHaoB6aIiaxLXk55ALkn-CmKBpS_k_PVKjFb653oBxqhUNT8cq8F7aBn0LCrdPlTPPpV78f2pEKpnuj5q2hbmY53aiQ8MfR9vX2HqDULdFmYU-gv53Bodutb2tfYsLwWAjifKgLlAOKFklgNj0hk?key=1EuDfGecDDglfbxOmH_CcA)



Customer’s average spending per order is more than **INR 6,000**. This average spending is beyond what typically a person would spend on one meal (INR 500), which is something interesting but only proves the fact that customers who go on food delivery apps have more buying power or prefer convenience. This could also mean that the user is feeding more than himself or consolidating orders. 91.19% of orders consist of **food only,** but Beverages runs to be second (2nd) in the most ordered cuisine where **Indian food** tops on the list! Based on the hypothesis, local food sells best! However, there is some confusing categorization on the data collection. There is a mix up of some subcategories with the categories. According to one of our references, alcohol peaks on weekends, but this dataset does not show subcategories on Beverages and Juices was used as a main category. It is also important to note the huge difference of orders without drinks compared to those with drinks, which raises a huge potential to be utilized in marketing beverages as well. **Saturday** has the highest average amount of items ordered at 29 units, but **Friday** seems to be the highest earner with an average of INR 7,000 generated sales weekly. **Electronic City** tops with the highest average quantity order, but **Sirsi** brings in the highest average sales. According to [mygate.com](https://mygate.com/blog/neighbourhood/electronic-city/), Electronic City is the home to the largest tech companies and has been developed to house the electronics industry. Meanwhile, Sisri is a tourist destination that offers scenic views, nature experiences and temple visits according to the [Travel Triangle website](https://traveltriangle.com/blog/places-to-visit-in-sirsi/#:~:text=Sirsi%2C a blissful town in,beautiful streams%2C and thundering waterfalls.). This could be a good indication that the steady amount of orders and average sales do come from the working class, utilizing the convenience served by Zomato. The theory of consolidated orders may be a significant area of interest. Compared to weekday orders, Saturday orders could be non-expensive small items orders. 



![img](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeBlpcgF7FdfYmWV5mZtb6bDFkAglg6ogfUJWjSiDzAUkeoRTeMAvnAUHAYw-YK2qSXYhDXkQDQ2wAVyXmF7r6eOANdBBYoBUjfb3FsQbXY0MOuUjfl8gQAyBZOqedd_HnRIvqY4Sh23jRcLL3ayLANzgsw?key=1EuDfGecDDglfbxOmH_CcA)





​	The table below shows that based on this dataset, there is positive correlation between high ratings and order volume. It was believed that the higher the rating a restaurant has, the more customers will place orders from it. However, in this sample set, customers didn’t mind if the restaurant had the highest rating. Most of the customers picked 4-rating restaurants. However, there are some limitations to this study as customers do not utilize the feature of rating restaurants. This study also found that there is also a positive correlation between the average cost of food in the restaurant and the amount of orders. Restaurants with INR 200-cost food are far more preferred. This could mean that a customer’s budget per order falls at this range.This may very well support the theory of consolidated orders. 



![img](https://lh7-rt.googleusercontent.com/docsz/AD_4nXdwCynFH3RRMRi9ASOHFHDcdHWdCzWEMB5Xi3102XManIK1FsKfBRLhvzKGFBHRNGh-rpEjqjQjp17_lKtA9gZAeLHZBlpvQyCzeDCGfNSpK3LDASvmJyFX6E_OFiJzjQ1MWDvHLKYtRXkiiJdrfEOCmaU?key=1EuDfGecDDglfbxOmH_CcA)





​	Unfortunately, based on this dataset, there has been a declining amount of active users, which is something that should be looked into and take necessary actions for. Data doesn’t show significant decline but more a steady rhythmic decline, which could also be because of rising market competition and other delivery apps alternatives. 



Our highest average spending came from Eric Henry IV amounting to almost INR 725,000!

![img](https://lh7-rt.googleusercontent.com/docsz/AD_4nXeXWIC_qABpcXgiK4OMWx-ZS3CJUMHIsANCOsgU_S78z3FBYKVm9swO2C036ArZMkCtqWvKuKntr-lktpeLrXakj17M3n6WjSR4Jse-UZgFlQc504afHM8o5l86idWW_L-QLUvpumePhlFjIB_23fU4qOgz?key=1EuDfGecDDglfbxOmH_CcA)



In conclusion, this dataset shows that Zomato has made a significant mark on the younger demographics with no income but are tech-savvy and prefer convenience. They do not prefer luxury but rather smart spending balancing convenience and cost efficiency. The steady activity on weekdays generates more income than the weekend orders, but not enough to keep a growing number of customers. 







Recommendations:

1. Improve data collection
   1. Categories should be precise. Do not mix categories with sub-categories
   2. Retrieve city of residency for users, whether they are the head of the family or whether they are living alone or with family or others.
   3. Encourage full utilization of delivery apps like rating the restaurants.
   4. Time stamp on user activity and order placements should be part of dataset
2. Internal Recommendations
   1. Ensure that the interface is easy to use to encourage older users.
   2. Create a feature where customers can schedule orders or create recurring orders. Since weekdays could get busy, this would sustain activities and orders during the week. 
3. Marketing Recommendations
   1. Create a campaign that emphasizes the quality of food and service to encourage high income earners and those with family. 
   2. Create a rewards program that earns higher points from higher spending on weekends to encourage higher sales-generating orders.
   3. Create food and beverage combos to increase sales on beverages which will also incur higher sales in total. 
   4. Create a campaign that uses students as a bridge to the older demographics. (ie. Student family-packs-to-share for the weekends, co-working packages)
   5. Increase multimedia presence for older demographics.
   6. Offer non-Indian cuisine restaurants ad-placement offers and extra marketing perks to create awareness. 
4. Potential area of exploration
   1. Customers demographic of users with higher spending, but with low order quantity, in order to understand this market niche and how to gain traction on this type of consumer. 
   2. Customer demographics of users with high order quantity but low spending, in order to understand this market and encourage higher spending. 





Resources:

*Average spending on meals per person when dining out for dinner in India as of December 2022

https://www.statista.com/statistics/1367594/india-average-spending-for-dinner-when-eating-out/



*Gender distribution of quick service restaurant delivery app users in the United States as of January 2021, by company

​	[https://www.statista.com/statistics/1246881/gender-of-restaurant-delivery-app-users-by-company-us/#:~:text=Gender%20of%20QSR%20delivery%20app%20users%20in%20the%20U.S.%202021%2C%20by%20company&text=In%20January%202021%2C%20the%20gender,even%20across%20all%20seven%20companies.](https://www.statista.com/statistics/1246881/gender-of-restaurant-delivery-app-users-by-company-us/#:~:text=Gender of QSR delivery app users in the U.S. 2021%2C by company&text=In January 2021%2C the gender,even across all seven companies)



*Food delivery apps: Usage and Demographics – Winners, Losers and Laggars

https://www.zionandzion.com/research/food-delivery-apps-usage-and-demographics-winners-losers-and-laggards/



 *Unveiling Insights: A Comprehensive Analysis of Food Delivery App Users

https://www.linkedin.com/pulse/unveiling-insights-comprehensive-analysis-food-delivery-harry-chang-x937c/



*Infographic | How India ordered on Swiggy and Zomato in 2023

https://www.deccanherald.com/lifestyle/food-and-drink/how-india-ordered-on-swiggy-zomato-2023-2825386

*DoorDash Unveils What and How Conusmers Have Been Eating and Drinking in 2023

https://about.doordash.com/en-us/news/doordash-unveils-what-and-how-consumers-have-been-eating-and-drinking-in-2023



*Everything you need to know about Electronic City, Bangalore

https://mygate.com/blog/neighbourhood/electronic-city/



*10 Places to Visit in Sirsi for an Offbeat Holiday Experience in Karnataka in 2024 [https://traveltriangle.com/blog/places-to-visit-in-sirsi/#:~:text=Sirsi%2C%20a%20blissful%20town%20in,beautiful%20streams%2C%20and%20thundering%20waterfalls.](https://traveltriangle.com/blog/places-to-visit-in-sirsi/#:~:text=Sirsi%2C a blissful town in,beautiful streams%2C and thundering waterfalls)