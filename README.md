# Customer Segmentation Using K-Means Clustering

This project demonstrates customer segmentation using the RFM (Recency, Frequency, Monetary) analysis framework combined with K-Means clustering. The goal is to identify distinct customer groups based on their purchasing behavior from an online retail dataset.

## Project Overview
Customer segmentation is a crucial marketing strategy that helps businesses understand customer behavior, personalize marketing efforts, and improve customer retention. This project utilizes the RFM model to quantify customer value and then applies K-Means clustering to group customers into meaningful segments.

## Dataset
The analysis is performed on the [Online Retail Dataset](https://archive.ics.uci.edu/dataset/352/online+retail), which contains transactional data from a UK-based online retail store from 01/12/2010 to 09/12/2011.

Key features of the dataset include:
*   `InvoiceNo`: Transaction identifier.
*   `StockCode`: Product identifier.
*   `Description`: Product name.
*   `Quantity`: Number of units purchased.
*   `InvoiceDate`: Date and time of transaction.
*   `UnitPrice`: Price per unit.
*   `CustomerID`: Unique customer identifier.
*   `Country`: Customer's country of residence.

## Methodology
1.  **Data Loading and Cleaning**: Initial data loading, handling missing `CustomerID` values, removing cancelled orders, and filtering out invalid quantities or unit prices.
2.  **RFM Feature Engineering**: Calculating Recency, Frequency, and Monetary values for each customer:
    *   **Recency**: Days since the last purchase.
    *   **Frequency**: Total number of unique purchases.
    *   **Monetary**: Total amount spent.
3.  **Outlier Handling and Scaling**: Applying `log1p` transformation to RFM values to reduce skewness and scaling the features using `StandardScaler` to ensure all features contribute equally to the clustering process.
4.  **K-Means Clustering**: Using the Elbow method to determine the optimal number of clusters (typically `k=4` for this dataset), followed by applying K-Means to segment customers.
5.  **Cluster Interpretation**: Analyzing the average RFM values for each cluster to assign descriptive labels such as:
    *   **Champions / Best Customers**
    *   **Loyal Customers / Active Buyers**
    *   **At Risk / Needs Attention**
    *   **Lost Customers / Churners**

## Results
The project identifies distinct customer segments, providing actionable insights for targeted marketing campaigns and customer relationship management strategies.

## Libraries Used
*   `pandas`
*   `numpy`
*   `matplotlib`
*   `seaborn`
*   `sklearn`
