# Customer-Personality-Analysis
## Problem Statement
Customer segmentation helps a business to modify its product based on its target customers from different types of customer segments. For example, instead of spending money to market a new product to every customer in the company’s database, a company can analyze which customer segment is most likely to buy the product and then market the product only on that particular segment.The target of this project is to perform clustering to summarize customer segments.

In this project, I will perform an unsupervised clustering of data on the customer's records from a groceries firm's database
## Flow of Project
1. Import the libraries
2. Load the data
3. Data Cleaning
4. Data Preprocessing
5. Data Visualization with Exploration
6. Dimensionality Reduction
7. Performing Clustering
8. Draw observations from clusters
9. Conclusion 
## About the data
* Data has 2240 rows and 29 columns
* Data has various features like marital status, educational qualification, Total amount spent by customers, total purchases made by customers in different sections, Number pf campaigns accepted by customers, Number of deals purchased by customes,Age, Family size, Number of days engaged with company
## Inferences drawn from exploratory analysis
* Amount of money spent on wine and meat products are positively correlated with income.
* Money spent of fruits, sweets, wine and meat is inversely correlated with is_parent, family_size.
* Total Purchases made by customers who are single and undergraduate customers are high.
* Most of the customers have income between 25,000 and 85,000.
## Data Modelling
* Data is then modelled to required number of features.
### Data is Standardised using StandardScaler.
## Dimensionality Reduction
* Principal Component Analysis (PCA) is used here.
* Plotting the Cummulative Explained variance graph, to preserve around 80% of variance, number of components is taken as 3.
## KMeans
* To decide for number of clusters in KMeans, within cluster sum of squares(wcss) is calculated for n_clusters ranging from 1 to 11.
* Plotting the elbow graph using wcss and number of clusters, find the optimum number of clusters.
* Optimum number of clusters here it is taken as 4, because after the value of 4, there is no significant drop in the elbow plot.
## Observations
* 4 clusters are formed.
###### Cluster 0 (Bronze)
- It has 929 customers, most crowded segment
- Low income.
- Low spending
- Mostly parents (maximum 5 members in the family, at least 2 members in thr family).
- They have more deal purchases, these customers cab be target audience for deals
- Highest number of web visits.
###### Cluster 1 (Platinum)
- It has 472 customers.
- These customers have accepted more campaigns, target audience for campaigns.
- Highest Income
- Highest Spendings
- Minimum age is less than minimum age of Cluster 0, simillarly for maximum age is greater than maximum age of Cluster 0.
- Not a parent (maximum 2 members in the family)
- Highest number of purchases from catalog and stores.
- Target audience for campaigns.
- Has highest spendings in meat, wine, fruits, sweet products.
###### Cluster 2 (Gold)
- It has 651 customers.
- Middle income.
- Average  spending.
- Maximum 3 members in the family.
- Target audience for Web Purchases and store purchases.
- Target audience for deals and store purchases.
###### Cluster 3 (Silver)
- It has 160 customers.
- Not parents (maximum 2 members in the family)
- Low income
- Average spending.
