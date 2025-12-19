# **🚚 Delivery Time Prediction System**

This project addresses two core challenges in the food delivery industry: **Estimated Time of Arrival (ETA)** prediction and **Driver Performance Analysis**. By accurately predicting delivery times and segmenting the driver fleet, businesses can optimize logistics, improve customer transparency, and implement targeted driver management strategies.

# **📦 Dataset**

This project uses a public **Food Delivery Dataset** from Kaggle (45,000+ records) featuring:
- **Order Attributes**: Order time, food type, weather conditions, and road traffic density.
- **Geospatial Data**: Restaurant and delivery coordinates (utilized for Haversine distance calculations).
- **Driver Profiles**: Age and historical performance ratings.

# **🛠 Technical Workflow**
**1. Data Engineering & Preprocessing**
- **Feature Extraction**: Calculated Haversine distance from GPS coordinates to determine the actual travel path.
- **Temporal Engineering**: Derived "Hour of Day," "Day of Week," and "Is Weekend" features to capture peak-hour traffic patterns.
- **Data Cleaning**: Handled missing values and standardized weather/traffic categories for model compatibility.

**2. Predictive Modeling (Regression)**
- **Algorithms**: Benchmarked multiple regressors including **Linear Regression, Decision Tree, and Random Forest**, selecting **XGBoost** as the champion model for its superior handling of non-linear logistics data.
- **Optimization**: Fine-tuned hyperparameters and utilized **StandardScaler** to minimize **MSE**, ensuring the model generalizes well to unseen delivery scenarios.
- **Performance**: The final XGBoost model achieved an **R² score of 0.68**, providing robust ETA estimates even under volatile weather conditions.

**3. Driver Segmentation (Unsupervised Learning)**
- **Approach**: Applied **K-Means Clustering** to categorize drivers based on age, ratings, and delivery speed.
- **Validation**: Used the **Elbow Method and Silhouette Analysis** to determine the optimal number of clusters (**k=5**).
- **Insights**: Discovered a **"High-Efficiency" cluster (Cluster 2)** and an **"Underperforming" cluster (Cluster 1)**, enabling data-driven decisions for targeted driver training and incentive reallocation.

**4. Deployment & Visualization**
- **Interactive Dashboard**: Developed a Power BI report to track fleet performance and delivery bottlenecks.
-> View dashboard: [Tại đây](https://app.powerbi.com/groups/me/reports/9d42876f-00a8-4007-a689-8adac0b61b03?ctid=5b98a1d4-abc3-42cd-896e-2e1b240dc662&pbi_source=linkShare&bookmarkGuid=f564909f-b69a-4940-a7ae-123252a70220)

- **Interactive Deployment**: Streamlit Web App To demonstrate the model's practical utility, I developed a web-based simulation tool using Streamlit:
  + **Dynamic ETA Calculator**: Provides a user-friendly interface where coordinators can input order details (distance, weather, traffic) to receive instant delivery time estimates.
 + **Model-in-the-Loop**: Seamlessly integrates a pre-trained **XGBoost pipeline** to show how real-world variables impact logistics performance.
 
# **🌟 Key outcomes**
- **High-Precision ETA**: Delivered a robust **XGBoost engine** with **68% variance explanation (R²)**, reducing delivery uncertainty for customers.
- **Operational Intelligence**: Provided actionable segmentation of **45,000+ drivers**, identifying a 20% performance gap between top and bottom tiers.
- **Business Integration:** Successfully bridged the gap between raw data and decision-making by deploying interactive visualization via **Power BI** and **Streamlit**.
