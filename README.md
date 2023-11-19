# machine_learning_project-unsupervised-learning

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
  
These exploratory steps aimed to comprehensively understand the dataset, its characteristics, and variations among groups, providing a solid foundation for subsequent analysis and modeling.

### Feature Engineering/Pre-processing

preprocessor pipeline was created that included a one hot encoder and a log transformer, this was then further combined with a standardscaler. this was then fitted to the data
then a function to replace outliers was then implemented on the data
Based on a heatmap and scatterplots, the 'Grocery' feature was dropped as it had a high correlation to multiple othere features
A variancethreshold was then run in order to remove any low-variance features

### Modeling

#### Kmeans Clustering

an elbow plot was created to decide upon the ideal amount of clusters for kmeans cluster analysis
then a kmeans instance was created based upon the aforementioned elbow plot
cluster labels were then assigned to the original dataframe in order to track cluster grouping
then used PCA to get two features that would aid in visualization in a 2-d space
then created a visualization to see the cluster groups
then ran a silhouette score
based on the elbowplot, visuavlization and silhouette score, 3 clusters was decided upon as the ideal number

#### Heirachical Clustering

an dendrogram was created based on the data
then an agglomerative clustering object was created with the amount of clusters decided upon based on the dendrogram
then plotted the clusters for visualization
ran a silhouette score
based on the dendrogram, visualization and silhouette score 3 clusters was decided upon as the ideal number

#### PCA

Created a PCA object and then looked at the explained variance ratio and found that the first two principal components covered
55% of the information within the data
then plotted the class seperation using the first two principal components

#### Conclusion

The original data, characterized by a heavily right-skewed distribution, required transformation to achieve a more normal distribution.
Across various clustering algorithms, the configuration of 3 clusters demonstrated the optimal balance between cohesion and separation.
An exploration of the explained variance plot indicated that approximately 55% of the information can be elucidated by the first two principal components.
Among the identified clusters, Cluster 2 emerged as the largest, followed by Cluster 0, while Cluster 1 was the smallest and exhibited the lowest spending. Further analysis revealed that Cluster 2, despite being the largest, spent significantly less on milk and Detergents_Paper products compared to Cluster 0, suggesting potential marketing opportunities for these specific products to Cluster 2 customers.