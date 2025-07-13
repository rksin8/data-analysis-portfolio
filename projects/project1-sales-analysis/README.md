# 📊 Sales Analysis & Customer Segmentation Project

## 🚀 Project Overview
Performed customer segmentation using **Recency–Frequency–Monetary (RFM)** analysis on retail sales data. Enhanced segmentation with machine learning, explainability, and deployment-ready outputs.

---

## 🧼 Data Cleaning & Optimization
- Removed missing or invalid entries (null CustomerIDs, negative Quantity/Price, canceled invoices).
- Optimized memory usage via downcasting and category conversion.
- Filtered out outliers (IQR method) to improve clustering reliability.

---

## 🔍 RFM Feature Engineering
- **Recency**: Days since last purchase.
- **Frequency**: Count of distinct invoices per customer.
- **Monetary**: Total spend by each customer.
- Scaled RFM features before clustering.

---

## 📊 Clustering & Explainability
- **KMeans Clustering** with `k=4` (determined via Elbow Method based on WCSS).
- Comparative clustering using **Hierarchical Clustering**.
- Evaluated segmentation quality using **Silhouette Scores**.
- Trained a **Decision Tree Classifier** to generate explainable rules (e.g., "If Recency > 200 → At‑Risk Customers").

---

## 🧠 Cluster Segments & Insights

| Segment                     | Avg Recency | Avg Frequency | Avg Monetary | Segment Behavior            | Business Strategy                          |
|----------------------------|-------------|----------------|---------------|-----------------------------|-------------------------------------------|
| **Best Customers**         | ~32 days    | ~6.7           | ~$1,530       | Frequent and high-value recent buyers | Focus on VIP programs and retention        |
| **Loyal Mid-Spenders**     | ~47 days    | ~3.7           | ~$850         | Regular repeat buyers with solid spend | Upsell with premium offers and bundles    |
| **Low Engagement Buyers**  | ~52 days    | ~1.6           | ~$296         | Infrequent buyers, moderate recency     | Encourage repeat purchases via incentives |
| **At-Risk / Churned**      | ~230 days   | ~1.5           | ~$293         | Dormant customers – haven’t purchased recently | Launch win-back campaigns                |

---

## 📈 Visualizations & Insights
- **Missing values heatmap**, **boxplots for outlier detection**, **Pareto revenue analysis**.
- 2D PCA-based cluster scatter plot and interactive 3D plot for cluster differentiation.
- Heatmap showing average RFM values per cluster (useful for quick comparisons).
- Extractable cluster rules via Decision Tree for stakeholder-friendly insights.

---

## 🛠 Tools & Outputs
- **Notebook**: `sales_analysis.ipynb` – includes full code and EDA.
- **Exports**:
  - `Retail_RFM_Segments.csv`: Cleaned RFM data with cluster and segment labels.
  - `RFM_Customer_Segment_Summary.csv`: Summary statistics for each segment.
- **Power BI Dashboard** (template available separately).

---

## 🎯 Business Impact
- Identifies high-value customers for retention and loyalty programs.
- Pinpoints at-risk segments for marketing reactivation campaigns.
- Supports data products and CRM teams with explainable rules and filters.

---

## ✅ Next Steps
1. Load the CSV exports into Power BI to build interactive dashboards.
2. Engage with marketing / CRM teams using segment-specific strategies.
3. Track segment migration over time and measure campaign effectiveness.



## Data

The dataset is a sample sales CSV file located in the `data/` folder.

## How to Run

1. Set up environment using `requirements.txt`.
2. Open and run the Jupyter notebook `notebooks/sales_analysis.ipynb`.
3. Follow the notebook steps for analysis and visualization.

## Tools

- Python 3.x
- Pandas
- Matplotlib
- Seaborn
- Jupyter Notebook

---

For questions or feedback, please contact me at ranjeet.iitb@hotmail.com.
