# Customer Segmentation Analysis Project Summary

## Introduction
This project aims to perform customer segmentation using transactional data from an online retail dataset. The goal is to identify distinct customer groups based on their purchasing behavior and provide targeted marketing strategies for each group. The data is obtained from Kaggle: (https://www.kaggle.com/datasets/mashlyn/online-retail-ii-uci)

## Data Loading and Preparation
- **Data Sources**: Two Excel sheets containing transactional data for the years 2009-2010 and 2010-2011.
- **Data Concatenation**: Combined the two datasets into a single DataFrame.
- **Country Filtering**: Focused on customers from the United Kingdom, as they form the majority of the dataset.

## Data Cleaning
- **Handling Missing Values**: Removed rows with missing Customer IDs.
- **Removing Invalid Entries**: Excluded transactions with non-positive prices and quantities.

## Feature Engineering
- **Revenue Calculation**: Added a new column for revenue by multiplying quantity and price.
- **Aggregated Metrics**: Calculated total purchase, frequency of transactions, and recency (days since the last purchase) for each customer.

## Exploratory Data Analysis
- **Distributions**: Visualized the distributions of total purchase, frequency, and recency using histograms and boxplots.
- **Outlier Removal**: Removed extreme outliers using the Interquartile Range (IQR) method.
- **Winsorization**: Applied winsorization to limit extreme values in the total purchase data.

## Data Scaling
- **Standardization**: Scaled the features (total purchase, frequency, recency) using StandardScaler to ensure they have a mean of 0 and a standard deviation of 1.

## Clustering
- **K-Means Clustering**: Applied K-Means clustering to segment customers into distinct groups.
- **Optimal K Selection**: Determined the optimal number of clusters using the elbow method and silhouette scores.
- **Cluster Assignment**: Assigned each customer to a cluster and visualized the clusters using 3D scatter plots and violin plots.

## Cluster Analysis
### Cluster 0: Mid Total Purchase, Mid Frequency, Low Recency
- **Characteristics**: Moderate spending and shopping frequency, but haven't made recent purchases.
- **Recommendations**:
  - Re-engagement campaigns
  - Special offers
  - Loyalty programs
  - Product recommendations

### Cluster 1: Low Total Purchase, Low Frequency, High Recency
- **Characteristics**: Low spending and infrequent shopping, but recent purchases.
- **Recommendations**:
  - Upselling and cross-selling
  - Incentivize repeat purchases
  - Personalized communication
  - Engagement content

### Cluster 2: High Total Purchase, High Frequency, Low Recency
- **Characteristics**: High spending and frequent shopping, but haven't made recent purchases.
- **Recommendations**:
  - VIP treatment
  - Reactivation campaigns
  - Loyalty rewards
  - Feedback requests

## Conclusion
The project successfully segmented customers into three distinct clusters based on their purchasing behavior. Each cluster has specific characteristics and tailored marketing strategies to enhance customer engagement and increase sales.
