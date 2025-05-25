# customer-segmentation-kmeans
Clustering-based customer segmentation using KMeans and Bank Marketing dataset
# Customer Segmentation using KMeans Clustering (Bank Marketing)

Link to original dataset: https://www.kaggle.com/datasets/henriqueyamahata/bank-marketing

## Library Imports and Setup:

This project uses the following Python libraries:
- `pandas` and `numpy` for data loading and manipulation
- `scikit-learn` for encoding, scaling, and clustering (KMeans)
- `matplotlib` for visualizing the clustering process

## Data Loading:

- The original dataset `bank.csv` is loaded using pandas
- `.info()`, `.describe()`, and `.isnull().sum()` are used to inspect the structure, data types, and any missing values

## Preprocessing:

- Missing values are handled using forward fill (`method='ffill'`)
- Categorical variables are converted to numerical form using `pd.get_dummies()`  
- The dataset is scaled using `StandardScaler` to normalize numeric features

## Feature Extraction:

- The transformed dataset is stored as a NumPy array (`X`)  
- This feature matrix is used as input for clustering

## Clustering Process:

- The **Elbow Method** is used to determine the optimal number of clusters by plotting WCSS (within-cluster sum of squares)
- **KMeans clustering** is applied with 3 clusters (based on the elbow plot)
- A new column `Customer_Segment` is added to the dataset to represent each customer's assigned cluster

## Visualization:

- A 2D scatter plot visualizes the clusters using the first two features
- Data points are colored by their cluster using the `viridis` color map
- This visual helps in understanding customer groupings at a glance

## Prediction and Output:

- The segmented dataset is saved as `bank_marketing_segmented.csv`
- It contains all original fields + a new `Customer_Segment` column indicating the assigned cluster
- This structured output can be used for:
  - Targeted marketing
  - Personalization
  - Customer retention strategies

## Error Handling:

Basic error handling is included for:
- File reading issues
- Invalid values or encoding mismatches
- Clustering execution errors

## Project Summary:

This project demonstrates customer segmentation using KMeans clustering on the Bank Marketing dataset. After encoding and scaling, customers are grouped into segments based on similar behavioral and demographic attributes. The result is a clean, labeled dataset ready for business strategy development or advanced modeling.
