# CoolTShirts Attribution 

CoolTShirts, an innovative apparel shop, is running a bunch of marketing campaigns.CoolTShirts sells shirts of all kinds, as long as they are T-shaped and cool. 
Recently, CTS started a few marketing campaigns to increase website visits and purchases. Using touch attribution, they’d like to map their customers’ journey: from initial visit to purchase. They can use that information to optimize their marketing campaigns. In this project, I have answered the following questions about their campaigns:

1. Getting familiar with the company.
    - How many campaigns and sources does CoolTShirts use and how are they related? 
    - What pages are on their website?
2. What is the user journey?
    - How many first touches is each campaign responsible for?
    - How many last touches is each campaign responsible for?
    - How many visitors make a purchase?
    - How many last touches on the purchase page is each campaign responsible for?
    - What is the typical user journey?
3. Optimized the campaign budget.
    - CoolTShirts can re-invest in 5 campaigns. Which should they pick and why?

Additionally, I have prepared a [PPT](https://github.com/Gonnuru/CoolTShirts_Attribution_queries/blob/master/CoolTShirts.pptx) which showcases the queries and outputs along with a summary of findings.  
# Schema
![](https://github.com/Gonnuru/CoolTShirts_Attribution_queries/blob/master/schema.png)

# Parameters
- **UTM parameters** are a way of tracking visits to a website. Developers, marketers, and analysts use them to capture information like the time, attribution source, and attribution medium for each user visit.
- **First-touch** attribution only considers the first source for each customer. This is a good way of knowing how visitors initially discover a website.
- **Last-touch** attribution only considers the last source for each customer. This is a good way of knowing how visitors are drawn back to a website, especially for making a final purchase.
first and last touches can be found by grouping page_visits by user_id and finding the MIN and MAX of timestamp.
- **To find first- and last-touch attribution**, join that table back with the original page_visits table on user_id and timestamp.
