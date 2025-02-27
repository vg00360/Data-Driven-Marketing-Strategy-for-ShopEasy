# Data-Driven Marketing Strategy for ShopEasy

## Introduction to Business Problem
ShopEasy, an online retail business, is experiencing a decline in customer engagement and conversion rates despite investing heavily in new online marketing campaigns. This project aims to analyze ShopEasy's marketing data and provide actionable recommendations to improve engagement, conversion rates, and overall marketing efficiency.

### Key Challenges:
1. **Reduced Customer Engagement**: Decline in user interactions with marketing content.
2. **Decreased Conversion Rates**: Fewer visitors converting into paying customers.
3. **High Marketing Expenses**: Marketing campaigns are not yielding expected returns.
4. **Need for Customer Feedback Analysis**: Understanding customer sentiment is crucial to improving engagement and conversions.

## Key Performance Indicators (KPIs)
1. **Conversion Rate**: Percentage of website visitors who make a purchase.
2. **Customer Engagement Rate**: Interactions with marketing content (clicks, likes, comments).
3. **Average Order Value (AOV)**: Average spend per transaction.
4. **Customer Feedback Score**: Average rating from customer reviews.

## Goal
1. **Increase Conversion Rates**: Identify factors affecting conversion and optimize the customer journey.
2. **Enhance Customer Engagement**: Determine content types that drive the highest interaction.
3. **Improve Customer Feedback Scores**: Extract insights from customer reviews to enhance satisfaction.

## Datasets Used
- **Customers (`dim_customers`)**: Customer details (CustomerID, Name, Email, Gender, Age, GeographyID).
- **Geography (`dim_geography`)**: Location data (GeographyID, Country, City).
- **Products (`products`)**: Product details (ProductID, ProductName, Price).
- **Customer Reviews (`customer_reviews`)**: Feedback data (ReviewID, CustomerID, ProductID, ReviewDate, Rating, ReviewText).
- **Engagement Data (`engagement_data`)**: Content interactions (EngagementID, ContentID, CampaignID, ProductID, ContentType, ViewsClicksCombined, Likes, EngagementDate).
- **Customer Journey (`customer_journey`)**: Customer interactions (JourneyID, CustomerID, ProductID, VisitDate, Stage, Action, Duration).

## Methodology
### **SQL Operations Performed**
- Joined `dim_customers` with `dim_geography` to enrich customer data.
- Categorized products into Low, Medium, and High price ranges.
- Cleaned `customer_reviews` text by removing extra spaces.
- Standardized `engagement_data` and split engagement metrics.
- Identified duplicate records in `customer_journey` using `ROW_NUMBER()`.
- Normalized and cleaned `customer_journey` data, handling duplicates and missing values.

### **Python Operations Performed**
- Connected to MySQL and fetched `customer_reviews` data.
- Applied TextBlob sentiment analysis to calculate sentiment polarity scores.
- Categorized sentiment into Positive, Negative, Neutral, and Mixed.
- Bucketed sentiment scores for better insights.
- Saved enriched dataset to CSV for visualization.

## Power BI Dashboard
### **Dashboard Pages & Insights**

### **1. Overview**
- Displays key KPIs such as conversion rate, engagement rate, and customer feedback score.
- Shows trends over time to identify peak and low-performing months.

![Overview Dashboard](Dashboard%20Screenshots/Overview.png)

### **2. Conversion Details**
- Highlights conversion trends across different months and product categories.
- Identifies drop-off stages in the customer journey.
- Provides insights into seasonal patterns.

📌 ![Overview Dashboard](Dashboard%20Screenshots/Conversion%20Details.png)

### **3. Social Media Details**
- Analyzes engagement levels for different content types.
- Compares views, clicks, and likes across social platforms.
- Suggests content strategies for better engagement.

📌 ![Overview Dashboard](Dashboard%20Screenshots/Social%20Media%20Details.png)


### **4. Customer Review Details**
- Displays sentiment analysis results from customer feedback.
- Highlights top positive and negative themes in reviews.
- Suggests improvement areas for better customer satisfaction.

📌 ![Overview Dashboard](Dashboard%20Screenshots/Customer%20Review%20Details.png)

## Insights & Actionable Recommendations
### **1. Increase Conversion Rates**
- **Observation:** Conversion rates fluctuated throughout the year, with peaks in January (18.5%) and lows in May (4.3%).
- **Action:** Focus on high-converting product categories (e.g., Ski Boots with 150% conversion) and run targeted seasonal promotions.

### **2. Enhance Customer Engagement**
- **Observation:** Engagement rates declined from August onward, with blog content performing best.
- **Action:** Optimize content strategies with interactive videos and stronger call-to-action placements.

### **3. Improve Customer Feedback Scores**
- **Observation:** The average rating is 3.7, below the target of 4.0.
- **Action:** Address negative and mixed feedback by following up with dissatisfied customers and improving customer support.

## Conclusion
This analysis provides data-driven insights into ShopEasy's marketing performance. By implementing targeted interventions, ShopEasy can enhance customer engagement, increase conversion rates, and improve overall customer satisfaction.

