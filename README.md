# Customer Segmentation Project using KMeans Clustering

This project applies clustering techniques to segment customers based on transaction data. The dataset used is **Online Retail II**, which contains information about transactions from an e-commerce website. The main goal is to segment customers using the RFM (Recency, Frequency, Monetary) model and perform KMeans clustering to identify different customer groups.

## Project Structure

- **Data Cleaning**: 
  - Removed invalid transactions and irrelevant data.
  - Filtered transactions to ensure valid `Invoice` and `StockCode` formats.
  - Removed records with missing `Customer ID` or zero values for `Price`.

- **RFM Model**:
  - Computed **MonetaryValue**, **Frequency**, and **Recency** for each customer based on their transaction history.

- **Visualization**:
  - Histograms and boxplots were created to visualize the distribution of RFM values.
  - A 3D scatter plot was used to visualize customer segments in RFM dimensions.

- **Outlier Detection**:
  - Outliers were identified for `MonetaryValue` and `Frequency` using Interquartile Range (IQR).
  - Separate visualizations for outliers were created.

- **Clustering**:
  - Applied **KMeans Clustering** on the scaled RFM data.
  - Used **Silhouette Score** to evaluate the clustering performance.
  - Chose an optimal number of clusters based on the Silhouette Score and Inertia plots.
  - Visualized the clustered data using violin plots and 3D scatter plots.

## Requirements

This project requires the following Python libraries:

- `pandas`
- `matplotlib`
- `seaborn`
- `sklearn`

You can install the required libraries by running:

```bash
pip install -r requirements.txt
