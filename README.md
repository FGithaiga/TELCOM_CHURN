# PROJECT TITLE : PREDICTING CUSTOMER CHURN FOR SYRIATEL


# PROJECT OVERVIEW
In the highly competitive telecommunications sector, retaining existing customers is just as crucial—if not more—than acquiring new ones. SyriaTel, like many telecom providers, faces significant revenue loss due to customer churn—the rate at which customers discontinue their service. Identifying customers who are likely to leave and understanding the factors driving that decision is key to improving retention strategies and optimizing service delivery.

This project aims to build a predictive machine learning classifier that accurately forecasts whether a customer is likely to churn (i.e., stop doing business with SyriaTel). Using a curated dataset of customer demographics, service usage, billing patterns, and support interactions,I conducted a detailed exploratory data analysis (EDA) and develop predictive models to uncover actionable insights.

By detecting churn early, SyriaTel can proactively engage at-risk customers, implement tailored offers, and improve overall customer satisfaction—ultimately reducing churn rates and protecting long-term revenue.


# BUSINESS UNDERSTANDING
In the telecom industry, customer retention is a critical business priority due to the high cost of acquiring new customers compared to maintaining existing ones. For SyriaTel, a leading telecommunications provider, customer churn—the percentage of users who stop using the service—is a significant challenge impacting revenue and long-term growth.

Understanding why customers churn and being able to predict who is likely to leave offers a major strategic advantage. If SyriaTel can identify at-risk customers early, it can take proactive measures such as:

Offering targeted promotions or personalized plans,

Improving service quality based on user feedback,

Enhancing customer support for high-risk segments.

# PROBLEM STATEMENT
In today’s highly competitive telecommunications sector, customers have a wide array of service providers to choose from, making customer loyalty increasingly fragile. A single poor experience can shape a customer’s perception of an entire brand, highlighting the critical importance of customer satisfaction in retaining users. With communication services deeply embedded in our daily routines, minimizing customer churn has become a strategic priority for telecom companies.

Customer churn, defined as the rate at which subscribers discontinue or fail to renew their services, poses a direct threat to revenue. Since retaining existing customers is significantly more cost-effective than acquiring new ones, understanding the factors driving churn is essential. Through detailed churn analysis, businesses can uncover behavioral patterns, segment at-risk users, improve service offerings, and design more effective customer retention strategies.

By leveraging predictive modeling and generating actionable insights, telecom firms can proactively address churn risks and strengthen customer relationships—ensuring long-term business sustainability and growth.


# DATA UNDERSTANDING
**1. Data Collection and Preparation**
Dataset: Used SyriaTel's dataset containing 3,333 customer records with 21 features including demographics, service usage, call durations, and plan subscriptions.

**Data Cleaning:**

Removed irrelevant columns like phone number.

Converted categorical variables (e.g., international plan, voice mail plan) into numeric values using Label Encoding.

Transformed the target variable churn from boolean to integer format.

**Data Integrity:**

Checked for null values (none found).

Ensured data types were correctly assigned to numeric and categorical features.

**2.Exploratory Data Analysis (EDA)**
**Univariate Analysis:**

Plotted bar charts for categorical features like international plan, voice mail plan, and churn.

Used histograms to show distributions of numerical variables like total day minutes, customer service calls.

**Bivariate Analysis:**

Boxplots: e.g., Total International Charges by Churn.

Countplots: e.g., Churn by International Plan and Churn by Voice Mail Plan.

**Multivariate Analysis:**

Correlation heatmap for all numerical features to observe relationships and redundancy.

Analyzed churn across multiple variables using grouped bar plots and color-coded feature distributions.

**3. Predictive Modeling**

Models Used:

Logistic Regression: Achieved 85.8% accuracy but had low recall for churned customers.

Decision Tree Classifier: Achieved 92.9% accuracy with better balance between precision and recall.


Model Evaluation Metrics:

Confusion Matrix

Accuracy Score

F1 Score

ROC Curve (for visual comparison of model performance)

# DATA INSIGHTS

**1. Customer Churn Distribution**

![alt text](Images/image.png)

The number of customers who did not churn is significantly higher than the number of customers who did churn. 


Business Implication: Though relatively low, this segment represents potential revenue loss if not addressed proactively.

**2. Churn by Number of Customer Service Calls**

![alt text](Images/image-1.png)

Insight: Customers with more customer service calls were significantly more likely to churn.

Business Implication: High support interactions may signal unresolved issues or dissatisfaction. These customers should be flagged for escalation and follow-up.


**3. Churn by International Plan**

![alt text](Images/image-2.png)

Insight: Customers with an international plan showed a higher likelihood of churn compared to those without.

Business Implication: Evaluate pricing or service quality for international plans; dissatisfaction may be driving customers away.

**4. Churn by Voice Mail Plan**

![alt text](Images/image-3.png)

Insight: Customers with a voice mail plan were less likely to churn.

Business Implication: The voice mail plan might contribute to perceived value or satisfaction; upselling this feature could help retention.

**5. Total Day Minutes vs Total Day Charges by Churn Status**

![alt text](Images/image-4.png)


Insight: Churned customers often had higher day-time minutes and charges, possibly indicating dissatisfaction with cost-effectiveness.

Business Implication: Consider personalized billing options or rewards for heavy users to retain them.

**6. International Charges by Churn**

![alt text](Images/image-5.png)

Insight: Churned customers had a higher average of international charges.

Business Implication: Customers may be leaving due to cost concerns related to international calling. Introducing flexible pricing or bundling options could mitigate churn.


**7. Correlation Heatmap**

![alt text](Images/image-6.png)


Insight: Differences in usage behavior (e.g., total day minutes, intl charge, customer service calls) between churned and non-churned customers were clearly visible.

Business Implication: These behavioral indicators are useful for segmenting high-risk customers for targeted retention strategies.


# FINDINGS
1. Customer Churn Is Predictable
Certain behavioral patterns and service features strongly correlate with customer churn.
Like, customers with frequent customer service calls or those subscribed to international plans were more likely to leave.

2. Not All Customers Are Equal
The churners were a minority in the data, but the cost of losing them is disproportionately high, especially if they are high-usage or long-tenure customers.

4. Decision Tree Model Outperformed Others
Compared two models:Logistic Regression had high overall accuracy (86%) but poor performance in identifying actual churners (F1-score: 0.31). Decision Tree achieved better balance (Accuracy: 93%, F1-score: 0.76), making it more suitable for churn detection.
This indicates that churn is not linearly separable, and more complex decision boundaries help.

5. Service-Related Frustrations Drive Churn
Features such as customer service call frequency were among the top predictors.
This shows that dissatisfaction and unresolved issues are early warning signs.

# RECOMMENDATIONS
1. Use Predictive Models in Business Operations
Implement churn prediction systems like the Decision Tree model in CRM workflows.
Enable real-time alerts for customers at high risk of churn, so teams can act proactively.

2. Prioritize At-Risk Customers
Use the model’s output to flag and prioritize high-value customers likely to churn.
Combine predictions with customer lifetime value (CLV) to target interventions cost-effectively.

3. Improve Customer Service Experience
Monitor customers making repeated service calls.
Provide faster resolution, better first-call handling, and possibly assign dedicated agents to high-risk segments.

4. Design Retention Campaigns Based on Data
Offer custom incentives or packages to customers predicted to churn.
Address specific friction points (e.g., billing confusion, limited international features).

5. Track and Re-train the Model
Customer behavior changes over time.
Retrain models quarterly using the most recent data to keep predictions accurate.

6. Test and Measure
A/B test intervention strategies (e.g., proactive calls, loyalty discounts) and measure churn rate reduction over time.
Use the model to test whether personalized retention strategies yield higher ROI than blanket campaigns.