## module_10_challenge
This project sets out to create a portfolio based on different cryptocurrencies to examine investment opportunities.  I will be using hvplot, pandas and various sklearn tools to accomplish this, as well as data from a cryptocurrency csv in the "Resources" folder.

# Libraries
import pandas as pd
import hvplot.pandas
from path import Path
from sklearn.cluster import KMeans
from sklearn.decomposition import PCA
from sklearn.preprocessing import StandardScaler

## Other functions used
# for loop used for elbow curve
k = list(range(1, 11))
inertia = []
for i in k:
    k_model = KMeans(n_clusters=i)
    k_model.fit(df_market_data_scaled)
    inertia.append(k_model.inertia_)