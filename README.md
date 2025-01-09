# Customer Analysis and Segmentation Using K-Means

## Overview

This project involves analyzing and segmenting customers of a UK-based online giftware store. The analysis focuses on feature engineering, K-Means clustering, and visualization techniques to derive insights into customer behavior.

## Technologies Used

- Python
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn

## Data Source

The dataset for this analysis can be found at: [UCI Machine Learning Repository - Online Retail II](https://archive.ics.uci.edu/dataset/502/online+retail+ii).

## Project Structure

- **Data Exploration**: Initial exploration of the dataset, including checking for missing values and data types.
- **Data Cleaning**: Processes to clean the dataset by removing invalid entries and handling missing values.
- **Feature Engineering**: Creating new features that help in understanding customer behavior.
- **K-Means Clustering**: Implementing K-Means clustering to segment customers based on their purchasing patterns.
- **Visualization**: Creating visual representations of the clustered data for better understanding.

## Analysis Steps

### Data Exploration

- Loaded the dataset and performed preliminary checks.
- Noted the presence of null values in the `Customer ID` column and negative values in the `Quantity` and `Price` columns.
- Observed that some invoices and stock codes did not conform to expected formats.

### Data Cleaning

- Removed rows with null `Customer ID` values and negative quantities.
- Dropped transactions with zero or negative prices.
- Filtered the dataset to retain only valid invoices (6-digit numbers).

### Feature Engineering

- Calculated `SalesLineTotal` as the product of `Quantity` and `Price`.
- Aggregated data by `Customer ID` to compute:
  - **Monetary Value**: Total spending per customer.
  - **Frequency**: Number of unique invoices per customer.
  - **Last Invoice Date**: The most recent transaction date per customer.
  
### K-Means Clustering

- Applied K-Means clustering using the features of `Monetary Value`, `Frequency`, and `Recency` (derived from `Last Invoice Date`).
- Evaluated the clustering results using silhouette scores to determine the optimal number of clusters.

### Visualization

- Created visualizations to depict clusters and customer segments.
- Utilized seaborn and matplotlib for effective data representation.

## Notes

- The dataset had significant missing values in the `Customer ID` column, which required careful handling.
- Negative quantities and prices indicated potential data entry errors or cancellations, which were filtered out during data cleaning.
- The analysis revealed distinct customer segments that could be targeted with tailored marketing strategies.

## Conclusion

The project successfully segmented customers of the giftware store, providing valuable insights into purchasing behavior. These insights can guide marketing efforts and improve customer relationship management.

## Future Work

- Further refining the clustering algorithm to enhance segmentation accuracy.
- Incorporating additional features like customer demographics for deeper analysis.
- Developing a predictive model to forecast future customer behavior.

## Acknowledgements

Thanks to the UCI Machine Learning Repository for providing the dataset used in this analysis.
