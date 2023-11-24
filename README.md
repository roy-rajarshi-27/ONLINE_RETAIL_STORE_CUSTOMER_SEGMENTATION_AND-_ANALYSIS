# ONLINE_RETAIL_STORE_CUSTOMER_SEGMENTATION_PROJECT

To Identify Major Customer Segments On Transnational Dataset Using Unsupervised ML Clustering Algorithms. In this project, our task is to identify major customer segments on a transnational dataset which contains all the transactions occurring between 01/12/2010 and 09/12/2011for a UK-based and registered non-store online retail. The company mainly sells unique all-occasion gifts. Many customers of the company are wholesalers. The dataset provided contains information about Invoice No, Stock Code, Description, Quantity, Invoice Date, Unit Price, Customer ID and Country for each transaction.

## To achieve our goal of segmentation, we followed the following sequence of steps.

* Understanding the dataset, doing some basic inspection on the raw data to check the number of columns, understanding distribution of data and checking statistics of the data in each variable. Checking for and handling missing values, Cleaning the data.
* Feature engineering: After getting some insights from the dataset we created some new features, altered the existing features to understand the hidden patterns in the data.
* EDA & Data insight on original data: we put out interesting inferences from the data to derive some meaningful results by visualizing some plots and distributions.
* After having understood the original data, we moved ahead to generate a new dataset based on Recency, Frequency and Monetary values of all the unique customers in order to do a behavioral customer segmentation. We did some feature engineering and EDA on this new dataset as well. We also made some transformations in this dataset to make it ready to be passed to different clustering algorithms.
* We started with a simple binning and quantile based simple segmentation model first then moved to more complex models because simple implementation helps having a first glance at the data and know where/how to exploit it better.
* Then we moved to k-means clustering and visualized the results with different number of clusters. As we know there is no assurance that k-means will lead to the global best solution. We moved forward and tried Hierarchical Clustering and DBSCAN clusterer as well.
* Obtained the optimal number of clusters using silhouette analysis, Elbow method and dendrogram to majorly identify 4 segments for marketing, churn prediction, to define their value, loyalty, profitability etc for the business on the basis of their behavioral attributes. 

## Analysis Approach
### 1. Data Quality Assessment and Data Cleaning

In the data cleaning step the data quality of the following datasets were first assesed. After a data quality assessment the following data quality issues was observed and the necessary process to mitigate the issue was followed :

  - 24.93% of items purchases are not assigned to any customer,Because we can't form clusters without CustomerID so we will delete them from dataset.
  - InvoiceNo starting with 'C' represents cancellation,So we dropped the cancelled product items.
  - The InvoiceDate column was transformed to create a new feature column 'Year','Month','Date','Hour'.
  - Created a new feature 'TotalAmount' by multiplying Quantity and UnitPrice.
  - Creating a new feature 'TimeType' based on hours to define whether its Morning,Afternoon or Evening
  - Checked whether there are duplicate records present in the dataset. In this dataset there were no duplicate records.



