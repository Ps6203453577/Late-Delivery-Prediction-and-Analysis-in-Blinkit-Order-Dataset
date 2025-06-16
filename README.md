# Late-Delivery-Prediction-and-Analysis-in-Blinkit-Order-Dataset

Overview:
This project explores order-level data from Blinkit to understand the patterns and causes of late
deliveries. The objective was to derive insights and build a predictive model that can forecast
whether an order will be delayed.

Dataset Description:
- Rows: ~15,000+
- Key Columns: order_created_time, order_delivered_time, store_id, payment_method, order_items,
delivery_duration, etc.

Data Preprocessing:
- Converted time-related columns to datetime format
- Created new features like: delivery_delay_minutes, is_late, order_day, order_hour
EDA (Exploratory Data Analysis):

- Identified peak hours for orders (6 PM - 9 PM)
- COD orders showed higher delay rates
- Saturdays had the highest order volume

- Visualizations:
- Distribution of delivery delays
- Orders per hour and weekday
-  Late delivery rates by store and payment method
-  
Machine Learning Model:
Used Random Forest Classifier to predict 'is_late'.
Key features: order_hour, order_day, store_id, payment_method
Performance:
- Accuracy: ~87%
- ROC AUC: ~0.91
- 
Business Insights:
- Orders during peak hours are more likely to be delayed
- COD significantly contributes to delivery inefficiencies
- Stores 1012 and 1043 frequently cause delays
- 
Recommendations:
- Encourage prepaid orders to reduce delay probability
- Optimize delivery slots during peak hours
- Focus operational audits on underperforming stores

- Tech Stack:
- Python
- Pandas, Seaborn, Matplotlib, Scikit-learn
- Google Colab
- GitHub

- Future Scope:
- Integrate geolocation/traffic data for real-time prediction
- Build a dashboard for order delay monitoring
- Deploy model via Streamlit or Flask
