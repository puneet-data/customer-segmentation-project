# Customer Segmentation using RFM Analysis & Clustering

This project focuses on segmenting customers of a UK-based e-commerce business using **RFM analysis** and **unsupervised machine learning algorithms** (KMeans & DBSCAN). The goal is to identify valuable customer groups to inform marketing strategies and improve customer retention.

---

##  Dataset

- **Source**: [UCI Online Retail Dataset](https://www.kaggle.com/datasets/carrie1/ecommerce-data/data)
- **Time Period**: December 2010 to December 2011
- **Contains**:
  - Transactions from a UK-based online retailer
  - 541,909 rows | 8 features
  - Columns: InvoiceNo, StockCode, Description, Quantity, InvoiceDate, UnitPrice, CustomerID, Country

---

## Project Objectives

- Clean and preprocess e-commerce transactional data
- Engineer **RFM features (Recency, Frequency, Monetary)** for each customer
- Apply **KMeans** clustering to segment customers based on RFM behavior
- Use **DBSCAN** to identify noise and density-based clusters
- Visualize and interpret clusters to extract business insights

---

##  Methodology

### 1. Data Cleaning
- Removed canceled orders (`InvoiceNo` starting with 'C')
- Removed missing Customer IDs
- Removed rows with non-positive Quantity or UnitPrice

### 2. RFM Feature Engineering
- **Recency**: Days since last purchase
- **Frequency**: Number of unique invoices
- **Monetary**: Total spend by customer
- Applied quantile-based filters to remove outliers

### 3. Clustering Models
- **KMeans Clustering**:
  - Standardized RFM features
  - Used Elbow Method and Silhouette Score to determine optimal `k`
  - Segmented customers into 3 main clusters

- **DBSCAN Clustering**:
  - Captured noise/outliers
  - Detected density-based customer groupings

### 4. Visualization
- RFM Distribution by Cluster
- PCA-based cluster projections
- DBSCAN vs KMeans cluster comparison table
- Revenue by Country
- Customer share by segment

---

## Key Insights

- **Cluster 0**: Moderate frequency and spend →  *Growth Potential*
- **Cluster 1**:Low frequency, high recency →  *At-Risk Customers*
- **Cluster 2**: High-frequency, high-monetary, low-recency →  *Loyal High-Value Customers*
- DBSCAN identified several **noise points**, helping separate outliers from core groups.
- The **United Kingdom** accounted for over 90% of total revenue, suggesting market concentration.

---

## Business Recommendations

- **Reward loyal customers** in Cluster 2 with VIP campaigns and retention incentives.
- **Target Cluster 0** with upsell campaigns and personalized promotions.
- **Re-engage Cluster 1** with win-back offers or churn-prevention discounts.
- **Use DBSCAN noise detection** to flag potential fraudulent or irregular customers.

---

##  Tools & Technologies Used

- Python (Pandas, NumPy, Scikit-learn, Seaborn, Matplotlib)
- Power BI (for dashboard visualizations)
- Jupyter Notebook
- Git & GitHub

---

##  Dashboard Preview

>  See: `customer_segmentation.pdf`  
This dashboard presents KPIs, RFM-based segment visuals, geographic revenue breakdown, and DBSCAN vs KMeans comparison.

---

##  Author

**Puneet Singh**  
Aspiring Data Analyst | Python, SQL, Power BI | Machine Learning & Business Intelligence Enthusiast  
[LinkedIn](https://www.linkedin.com/in/puneet471/) | [Portfolio](https://github.com/Puneet0123/Data_project/tree/main)

---

## License

This project is for educational and portfolio purposes.

