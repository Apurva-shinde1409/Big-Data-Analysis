# Big-Data-Analysis
**#Introduction**

**#Problem Statement**
The real estate market is inherently volatile, influenced by economic, demographic, and market factors. Identifying high-risk regions is critical for mitigating financial losses, improving investment decisions, and maintaining market stability.
**Objectives**
Develop a scalable machine learning model for classifying high-risk and low-risk regions.
Analyze the impact of key market and economic indicators on real estate risks.
Provide actionable insights to support data-driven decision-making for stakeholders.

**#Literature Review**

Economic Indicators in Real Estate Analysis:
Studies highlight the importance of income growth and supply-demand balance in predicting market risks. For example, high months of supply often indicate a buyer’s market, increasing financial risks for sellers.
Machine Learning in Risk Assessment:
Research emphasizes the effectiveness of Random Forest and Decision Tree models for classification tasks due to their robustness and interpretability.
PySpark for Big Data Processing:
PySpark is widely recognized for its efficiency in handling large datasets, making it ideal for real estate data with regional and temporal dimensions.

**#Methodology**

**1. Data Collection**
Datasets Used:
Market Data: Metrics like median_sale_price, months_of_supply, and inventory.
Income Data: Yearly income_value and income_growth for various regions.
**2. Data Preprocessing**
Removed null values and standardized region names for consistency.
Merged datasets on year and region (state/GeoName).
Created the risk_level variable:
High Risk (1): income_growth < 5% and months_of_supply > 3.
Low Risk (0): All other regions.
**3. Feature Engineering**
Assembled key features (income_growth, months_of_supply, etc.) into a features column using PySpark’s VectorAssembler.
**4. Model Development**
Models Used:
Random Forest Classifier (Primary Model)
Logistic Regression (Comparison Model)
Evaluation Metrics:
Accuracy: Percentage of correct predictions.
ROC-AUC: Measures the model’s ability to distinguish between high-risk and low-risk regions.
