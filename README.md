# Cryptocurrencies
## Overview of Project
This project consisted of the analyst to get a clear understanding of what unsupervised learning is used for, how to process the data, how to cluster the data, and how to reduce the dimensions, and the final step of how to reduce the principal components using PCA to prepare for an analysis on the cryptocurrency market. A report was created that included what cryptocurrencies are being trading on the market and how they could be grouped to create a classification system for the new investment. The grouping of the cryptocurrencies a clustering algorithm will be created, and the findings will be shown by creating a 3D and hvscatter charts. This project has the following deliverables developed and submitted:

•	Deliverable 1: Preprocessing the Data for PCA

•	Deliverable 2: Reducing Data Dimensions Using PCA

•	Deliverable 3: Clustering Cryptocurrencies Using K-means

•	Deliverable 4: Visualizing Cryptocurrencies Results



## Results
### Deliverable 1 Requirements:
The following five preprocessing steps have been performed on the crypto_df DataFrame:

•	All cryptocurrencies that are not being traded are removed

     	The IsTrading column is dropped

     	All the rows that have at least one null value are removed

     	All the rows that do not have coins being mined are removed

     	The CoinName column is dropped

•	A new DataFrame is created that stores all cryptocurrency names from the CoinName column and retains the index from the crypto_df DataFrame

•	The get_dummies() method is used to create variables for the text features, which are then stored in a new DataFrame, X 

•	The features from the X DataFrame have been standardized using the StandardScaler fit_transform() function

### Deliverable 2 Requirements:
The following steps were performed to complete Deliverable 2 requirements:

•	The PCA algorithm reduces the dimensions of the X DataFrame down to three principal components

•	The pcs_df DataFrame is created and has the following three columns, PC 1, PC 2, and PC 3, and has the index from the crypto_df DataFrame

### Deliverable 3 Requirements:
The following steps were performed to complete Deliverable 3 requirements:

•	The K-means algorithm is used to cluster the cryptocurrencies using the PCA data, where the following steps have been completed:
     
     	An elbow curve is created using hvPlot to find the best value for K

![elbow_curve]( https://github.com/fletchrk/Cryptocurrencies/blob/main/Resources/elbow_curve.png)

     	Predictions are made on the K clusters of the cryptocurrencies’ data

     	A new DataFrame is created with the same index as the crypto_df DataFrame and has the following columns: 
       Algorithm, ProofType, TotalCoinsMined, TotalCoinSupply, PC 1, PC 2, PC 3, CoinName, and Class

### Deliverable 4 Requirements:
The following steps were performed to complete Deliverable 4 requirements:

•	The clusters are plotted using a 3D scatter plot, and each data point shows the CoinName and Algorithm on hover

![3D_Crypto_currencies]( https://github.com/fletchrk/Cryptocurrencies/blob/main/Resources/3D_Crypto_currencies.png)


•	A table with tradable cryptocurrencies is created using the hvplot.table() function

•	The total number of tradable cryptocurrencies is printed

•	A DataFrame is created that contains the clustered_df DataFrame index, the scaled data, and the CoinName and Class columns

•	A hvplot scatter plot is created where the X-axis is "TotalCoinsMined", the Y-axis is "TotalCoinSupply", the data is ordered by "Class", and it shows the CoinName when you hover over the data point

![hvscatter]( https://github.com/fletchrk/Cryptocurrencies/blob/main/Resources/hvscatter.png)


