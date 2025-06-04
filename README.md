# PROJECT TITLE : PREDICTING CUSTOMER CHURN FOR SYRIATEL

# PROJECT OVERVIEW


# INSTALLATION AND SETUP












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