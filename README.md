# MLM-1
Title: Clustering Analysis on car prices and sales data

Project Objectives | Problem Statements 1.1. PO1 | PS1: Market Segmentation:
The clustering results will reveal distinct market segments, each characterized by specific features such as luxury, economy, and performance. This segmentation can assist manufacturers and dealers in targeting their marketing efforts more precisely and tailoring their products to meet the needs of different consumer groups. 1.2. PO2 | PS2: Price Range Identification:
The clusters will provide clear distinctions between various price ranges, enabling a better understanding of the competitive landscape. This information can be valuable for pricing strategies, allowing companies to position their products competitively within the market. 1.3. PO3 | PS3: Product Development Insights:- By analyzing the common features within each cluster,we can gain insights into consumer preferences and emerging trends. This can inform product development and innovation strategies, ensuring that new models align with market demand. Incorporating the additional descriptive statistics and visualizations into the report would result in the following:
2. Description of Data

2.1. Data Source, Size, Shape

2.1.1. Data Source (Website Link): Kaggle Vehicle Sales Data
2.1.2. Data Size: 2493.625 KB
2.1.3. Data Shape (Dimension): 16 variables | 60313 records
2.2. Description of Variables

2.2.1. Index Variable(s): None
2.2.2. Categorical Variables or Features (CV):
Nominal Type: 'make', 'model', 'trim', 'body', 'vin', 'state', 'color', 'interior', 'seller', 'saledate'
Ordinal Type: 'transmission'
2.2.3. Non-Categorical Variables or Features: 'year', 'condition', 'odometer', 'mmr', 'sellingprice'
2.3. Descriptive Statistics

2.3.1. Categorical Variables or Features:
Count | Frequency Statistics:
For example, there were 36 records with missing 'trim', 495 missing 'body', and 2139 missing 'transmission'.
Proportion (Relative Frequency) Statistics:
'color' and 'interior' have higher frequencies with 26.369% and 122.569% respectively (which may indicate repeated counts or a need for normalization).
2.3.2. Non-Categorical Variables or Features:
Measures of Central Tendency and Dispersion:
'year' has a mean of 2009.41 with a standard deviation of 3.33.
'condition' averages at 29.56 with a standard deviation of 13.36.
'odometer' shows a mean of 77089.52 with a large standard deviation of 52306.50, indicating a wide range of values.
'mmr' and 'sellingprice' are correlated with a correlation coefficient of 0.976478, suggesting they move almost in unison.
Correlation Statistics (with Test of Correlation):
A significant negative correlation between 'year' and 'odometer' (-0.697794), suggesting older cars tend to have higher odometer readings.
A strong positive correlation between 'sellingprice' and 'mmr' (0.976478), indicating that as the market value increases, so does the selling price.
3. Analysis of Data

3.1. Data Pre-Processing

Missing Data Statistics and Treatment:
Records: Average missing data per record is 0.36.
Categorical Variables: 'make' has 55 missing entries, 'model' has 56, and 'transmission' is missing in 2139 records.
Non-Categorical Variables: 'condition' has 4359 missing entries, which is significant and requires attention.
Outlier Statistics and Treatment (Scaling | Transformation):
Non-Categorical Variables: Outliers are observed in 'year', 'odometer', 'mmr', and 'sellingprice'.
3.2. Data Analysis

Unsupervised Machine Learning Clustering Algorithm: K-Means (Base Model):
Silhouette Score for 3 clusters: 0.5463474167763533
Silhouette Score for 4 clusters: 0.510728846811461
Davies-Bouldin Score for 3 clusters: 0.5933411149704748
Davies-Bouldin Score for 4 clusters: 0.6026263296576294
4. Results | Observations

Visualizations:
Elbow Curve for Optimal K: Indicates that the drop in within-cluster sum of squares (WCSS) lessens significantly after 3 clusters, which suggests that the optimal number of clusters might be 3.
DBSCAN Clustering Result: Shows a dense cluster of data points with selling price up to around 20,000 and higher values being treated as outliers or noise (cluster label -1).
5. Managerial Insights

The number of segments or clusters for K-Means, as suggested by the Elbow Curve, is 3, which aligns with the silhouette and Davies-Bouldin scores.
**The strong positive correlation between 'mmr' and 'sellingprice' can
be used to predict selling prices based on market values.**

Given the insights from DBSCAN, caution should be exercised when dealing with higher-priced vehicles as they tend to deviate from typical patterns.
The standardized data shows how different variables compare against each other when scaled to a mean of 0 and standard deviation of 1, which can be useful for identifying variables with the most variance or impact.
This report incorporates the latest findings, including descriptive statistics for categorical and non-categorical variables and the results from clustering algorithms. It provides a comprehensive overview of the dataset's characteristics and the implications of the clustering analysis.
