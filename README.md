# Airline-Customer-Segmentation
Dataset contains historical customer data of an airline company. The company wants to optimize its marketing strategies. The CMO has no starting point to create customer profile and wants your advice to create it based on data.

## Data Preprocessing
- Replace missing values
- Remove outliers outside upper Q3 and lower Q1 limits
- Feature selection is based on RFM model, spending habit, and Frequent Flyer Program engagement: LAST_TO_END,	FLIGHT_COUNT,	SEG_KM_SUM,	SUM_YR_1,	Points_Sum,	avg_discount
- Standardization

## K-means Clustering
- Optimal number of cluster based on silhouette plot: 2
- Silhouette score: 0.35

## Agglomerative Clustering
- Optimal number of cluster based on dendrogram: 2
- Silhouette score: 0.37

## Result
**Cluster 0:**

High recency score (low LAST_TO_END), high frequency, high monetary, high spending power, high points, average discount.

Interpretation: can be considered as 'premium customer'. They often fly and do not hesitate to spend money. Possible include business traveler and people with flexible schedule.

**Cluster 1:**

Average recency score (average LAST_TO_END), low frequency, low monetary, low spending power, low points, average discount.

Interpretation: can be considered as 'potential customer' because they have low score across all aspects. They received the same amount of discount as other cluster but did not engage with airline.

## Business Recommendation
**Cluster 0 (Premium Customer)**

Goal: Maintain loyalty and increase purchases

Strategy:

*   Provide special offers and rewards for loyal customer.
*   Provide exclusive experience in their journey, such as exclusive check-in counter, access to VIP lounge, priority boarding, upgrade to a higher class, and extra baggage allowance.
*  Use customer data to provide personalized experiences, such as flight recommendations or tour packages. Offer additional products or services that are relevant to the customer's purchasing history.
*  Collaborate with airlines, hotels, tour & travel companies, and insurance companies to offer attractive tour packages and travel insurance.


**Cluster 1 (Potential Customer)**

Goal: Drive engagement and encourage purchase

Strategy:

*   Offer attractive discounts and promotions.
*   Send personalized emails with product or service recommendations based on customer interests and purchase history.
*   Send surveys to identify potential barriers and how to overcome them.
