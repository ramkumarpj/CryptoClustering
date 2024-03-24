# CryptoClustering

For this challenge, Python and unsupervised learning will be used to predict if cryptocurrencies are affected by 24-hour or 7-day price changes.

### Overview of the Analysis

* The objective is to build an unsupervised machine learning model that will predict cryptocurrencies that are affected by 24-hour or 7-day price changes.

* Following data points are provided in the dataset "coin_id, price_change_percentage_24h, price_change_percentage_7d, price_change_percentage_14d, price_change_percentage_30d, price_change_percentage_60d, price_change_percentage_200d, price_change_percentage_1y"

* The data provided is normalised using "StandardScaler()" module from scikit-learn

#### Cluster CryptoCurrencies using KMeans Model

* KMeans clustering algorithm is selected to build the upsupervised learning model.
   
* "Elbow Method' is used to find the optimal value of K.

* KMeans model was created using the optimal value of K (4) deduced using 'Elbow Method'

* KMeans model was fitted using the normalised data and used to predict clusters of cryptocurrencies

* The predicted clusters were then plotted using scatter plot "x="price_change_percentage_24h"` and `y="price_change_percentage_7d"

#### Optmize clusters using Principal Component Analysis (PCA)

* PCA model is created with n_components = 3

* PCA model is fitted and transformed using scaled dataset

* Explained variance ratio is retrieved from the PCA Model to determine how much information can be attributed to each principal component.

* K Means Model steps outlined above is used for PCA data provided by the PCA Model.

### Summary

Elbow method suggested to use '4' as the value of K in both instances. 

The explained variance ratio for PCA model is '0.8950'

[Elbow Plots](Output/ElbowPlots.html)

[CryptoCurrencies Clusters](Output/CryptoCurrenciesClusters.html)


After analysing the plots, we can see that both methods predicted 4 different clusters fairly well. Few points in cluster 0 and cluster 2 became more closely located when fewer features were used. Cluster 1 was charted more distinctively when using fewer features. 


