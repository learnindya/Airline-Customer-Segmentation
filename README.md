# Airline-Customer-Segmentation
Dataset contains historical customer data of an airline company. The company wants to optimize its marketing strategies. The CMO has no starting point to create customer profile and wants your advice to create it based on data.

## Data Preprocessing
- Replace missing values
- Remove outliers outside upper Q3 and lower Q1 limits
- Feature selection is based on RFM model, spending habit, and Frequent Flyer Program engagement: LAST_TO_END,	FLIGHT_COUNT,	SEG_KM_SUM,	SUM_YR_1,	Points_Sum,	avg_discount
- Standardization

## K-means Clustering
- Optimal number of cluster based on silhouette plot: 3
- Silhouette score: 0.27

## Agglomerative Clustering
- Optimal number of cluster based on dendrogram: 2
- Optimal number of cluster based on silhouette plot: 3
- Silhouette score: 0.27

## Result
**Cluster 0:**

Low recency score (high LAST_TO_END), low frequency, low monetary, average spending power, low points, average discount.

Interpretation: can be considered as 'potential customer' because they have spending power but did not utilize it. They received the same amount of discount as other cluster but did not engage with airline.

**Cluster 1:**

High recency score (low LAST_TO_END), high frequency, high monetary, high spending power, high points, average discount.

Interpretation: can be considered as 'premium customer'. They often fly and do not hesitate to spend money. Possible include business traveler and people with flexible schedule.

**Cluster 2:**

High recency score (low LAST_TO_END), average frequency, average monetary, low spending power, average points, low discount.

Interpretation: can be considered as 'general customer'. They receive small discount but still fly more frequently and longer.


