# Zeotap Data Science Assignment
 

This repository contains the Exploratory Data Analysis (EDA), Customer Clustering, and a Lookalike Model implementation for identifying potential high-value customers based on existing data. The aim is to extract actionable insights and enhance business strategies through data-driven segmentation and predictive modeling.


## **Repository Structure**

### **Files**

1. **EDA and Clustering Outputs**
     - Transactions by region.
     - Top 10 products.
     - Sales distribution by category.
     - Scatter plot of customer clusters based on purchasing patterns.

2. **Lookalike Model**
   - `Snwha_P_Pratap_lookalike.ipynb`: Python script implementing the lookalike model to identify potential high-value customers.
   - `Sneha_P_Pratap_lookalike.csv`: Output file containing the predicted lookalike customers with their respective scores.

3. **Merged Dataset**
   - `merged.csv`: The consolidated dataset containing customer, product, and transaction details used for clustering and lookalike modeling.

---

## **Contents**

### **1. Exploratory Data Analysis (EDA)**

The EDA phase provides insights into transaction trends, product performance, and customer behavior:
- **Regional Performance**: South America leads in transactions, followed by Europe and Asia.
- **Top Products**: The top 10 products are identified based on transaction volume.
- **Sales by Category**: Electronics contributes the most to total sales, followed by Clothing and Books.

The visualizations include:
- Bar chart: Transactions by region.
- Bar chart: Top 10 products.
- Pie chart: Sales by category.

### **2. Customer Clustering**

Clustering analysis segments customers into distinct groups using the **K-Means algorithm**. Features such as transaction value, product categories, and regional behavior were used. The key clusters identified include:
- **Cluster 1**: High spenders.
- **Cluster 2**: Occasional buyers.
- **Cluster 3**: Region-specific buyers.
- **Cluster 4**: Moderate buyers.

**Evaluation**: The clustering quality is assessed using the **Davies-Bouldin Index (DBI)**, with a score of **1.63**, indicating well-separated clusters.

### **3. Lookalike Model**

The Lookalike Model is designed to predict potential high-value customers based on the characteristics of existing high-spending customers. This is achieved using a **classification model**:
- **Model Used**: Gradient Boosting Classifier for its efficiency and high accuracy.
- **Training Data**: Customers are labeled as high-value (1) or others (0) based on spending thresholds.
- **Features**: Region, total transaction value, transaction frequency, signup date, and product preferences.

**Output**:
- `Sneha_P_Pratap_lookalike.csv` contains a ranked list of potential customers with their lookalike scores. Higher scores indicate a higher likelihood of being high-value customers.


## **Insights and Recommendations**

### **EDA Insights**:
1. Focus on South America for scaling operations as it has the highest transaction volume.
2. Develop promotional campaigns for the top 10 products and underperforming categories.
3. Target Electronics and Clothing for future promotions due to their significant contributions.

### **Clustering Insights**:
1. **Cluster-Specific Strategies**:
   - High spenders: Exclusive offers and loyalty programs.
   - Occasional buyers: Incentivize repeat purchases with discounts.
   - Regional buyers: Localized campaigns tailored to specific regions.

### **Lookalike Model Insights**:
1. Use the lookalike predictions to design targeted campaigns aimed at converting potential high-value customers.
2. Cross-sell high-margin products to predicted high-value customers.
3. Continuously refine the model with additional customer data and interactions.



## **Technical Details**

### **Technologies Used**:
- **Python Libraries**: `pandas`, `matplotlib`, `seaborn`, `scikit-learn`, `numpy`, `xgboost`.
- **Clustering Algorithm**: K-Means (optimized with silhouette analysis and Davies-Bouldin Index).
- **Lookalike Model**: Gradient Boosting Classifier.



## **Future Scope**

1. **Improved Lookalike Model**:
   - Incorporate more features such as demographics and web activity logs.
   - Experiment with deep learning models for better accuracy.

2. **Enhanced Clustering**:
   - Test hierarchical or DBSCAN clustering for more robust segmentation.
   - Analyze seasonal trends for time-based segmentation.

3. **Real-Time Insights**:
   - Build a pipeline to update the clustering and lookalike predictions in real time as new data arrives.
