# Unsupervised Learning Wholesale Data

## Project Outcomes
- Unsupervised Learning: perform unsupervised learning techniques on a wholesale data dataset. The project involves four main parts: exploratory data analysis and pre-processing, KMeans clustering, hierarchical clustering, and PCA.
### Duration:
Approximately 4 hours
## Project Description:
In this project, we will apply unsupervised learning techniques to a real-world data set and use data visualization tools to communicate the insights gained from the analysis.

The data set for this project is the "Wholesale Data" dataset containing information about various products sold by a grocery store.
The project will involve the following tasks:

### Exploratory Data Analysis

- **Initial Data Inspection:**
  - Utilized the `.info()` and `.describe()` methods for an overall understanding of the dataset's structure and statistical summaries upon import.
- **Data Integrity Checks:**
  - Conducted essential checks for null values, zeros, and missing data to ensure data integrity.
- **Correlation Analysis:**
  - Generated a correlation heatmap to explore the interrelationships between variables and understand pairwise correlations.
- **Distribution Visualization:**
  - Employed histograms to visualize the data distribution and gain insights into variable frequency.
- **Outlier Identification:**
  - Created boxplots to identify and visualize outliers in each column, offering insights into data spread and value distribution.
  
These exploratory steps aimed to understand the dataset, its characteristics, and variations among groups.

### Feature Engineering/Pre-processing

- **Preprocessing Pipeline:**
  - Created a preprocessing pipeline comprising a one-hot encoder and a log transformer.
  - Combined the pipeline with a StandardScaler for further data transformation.
  - Fitted the combined pipeline to the data.

- **Outlier Replacement Function:**
  - Implemented a function to replace outliers within the dataset.

- **Feature Analysis and Dropping:**
  - Conducted analysis using a heatmap and scatterplots.
  - Identified 'Grocery' as a feature with high correlation to multiple others.
  - Dropped the 'Grocery' feature from the dataset.

- **Variance Thresholding:**
  - Applied a variance threshold to remove low-variance features from the dataset.
  
### Modeling

#### Kmeans Clustering

- **Elbow Plot for Cluster Selection:**
  - Created an elbow plot to determine the optimal number of clusters for KMeans cluster analysis.

- **KMeans Instance Creation:**
  - Generated a KMeans instance based on the identified optimal number of clusters from the elbow plot.

- **Cluster Label Assignment:**
  - Assigned cluster labels to the original dataframe to track cluster grouping.

- **PCA for Dimension Reduction:**
  - Utilized Principal Component Analysis (PCA) to obtain two features for visualization in a 2-dimensional space.

- **Cluster Visualization:**
  - Created a visualization to observe cluster groups in the dataset.

- **Silhouette Score Evaluation:**
  - Calculated a silhouette score to assess the quality of the clustering.

- **Decision on Number of Clusters:**
  - Based on the elbow plot, visualization, and silhouette score, determined that 3 clusters were the optimal choice for the analysis.

#### Heirachical Clustering

- **Dendrogram Creation:**
  - Generated a dendrogram based on the dataset to visualize hierarchical clustering.

- **Agglomerative Clustering Object:**
  - Created an agglomerative clustering object with the determined number of clusters from the dendrogram.

- **Cluster Visualization:**
  - Plotted the clusters for visual representation.

- **Silhouette Score Evaluation:**
  - Calculated a silhouette score to assess the quality of the hierarchical clustering.

- **Decision on Number of Clusters:**
  - Based on the dendrogram, visualization, and silhouette score, concluded that 3 clusters were the optimal choice for the analysis.

#### PCA

- **PCA Object Creation:**
  - Created a Principal Component Analysis (PCA) object.

- **Explained Variance Analysis:**
  - Examined the explained variance ratio to understand the contribution of each principal component.
  - Discovered that the first two principal components covered 55% of the information within the data.

- **Visualization Using Principal Components:**
  - Plotted the class separation using the first two principal components for visual analysis.

#### Conclusion

- The original data, characterized by a heavily right-skewed distribution, required transformation to achieve a more normal distribution.
- Across various clustering algorithms, the configuration of 3 clusters demonstrated the optimal balance between cohesion and separation.
- An exploration of the explained variance plot indicated that approximately 55% of the information can be elucidated by the first two principal components.
- Among the identified clusters, Cluster 2 emerged as the largest, followed by Cluster 0, while Cluster 1 was the smallest and exhibited the lowest spending. Further analysis revealed that Cluster 2, despite being the largest, spent significantly less on milk and Detergents_Paper products compared to Cluster 0, suggesting potential marketing opportunities for these specific products to Cluster 2 customers.
