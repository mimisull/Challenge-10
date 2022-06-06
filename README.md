# Challenge-10
The Directory for this respoitory is:
[Summary](https://github.com/mimisull/Challenge-10/blob/main/README.md)
[Code](https://github.com/mimisull/Challenge-10/blob/main/crypto_investments.ipynb)

**Assembling investment portfolios that are based on Cryptocurrencies**

Specifically, I am building a tool to determine the best invesment portfolio based on crypto.

I accomplish this using analysis not only based on returns and volatility, but also other factors that might impact the crypto market—leading to better performance for your portfolio..

*User Story*:
As a user, I need to determine what are good investment opportunities.

As a user, I need to be able to visualize trends in the crypto.

As a user, I need to be able to visualize and compare results

*Acceptance Criteria*:
Given that I’m unable to store data in excel files and go through them, I need to use this tool to sort through all different types of cryptocurrencies


## Usage
The project works by retrieving accurate data using open, high, low, close, volume, and daily_returns stats for each stock.

Imported the necessary tools with this code:

'''import pandas as pd
import hvplot.pandas
from path import Path
from sklearn.cluster import KMeans
from sklearn.decomposition import PCA
from sklearn.preprocessing import StandardScaler'''

Selected info with this:

'''df_market_data = pd.read_csv(
    Path("Resources/crypto_market_data.csv"),
    index_col="coin_id")'''

'''scaled_data = StandardScaler().fit_transform(df_market_data)'''

'''df_market_data_scaled = pd.DataFrame(
    scaled_data,
    columns=df_market_data.columns
)'''

Found k with this: 

'''for i in k:
    model = KMeans(n_clusters=i, random_state=0)
    model.fit(df_market_data_scaled)
    inertia.append(model.inertia_)'''

'''elbow_data = {
    "k": k,
    "inertia": inertia
}

df_elbow = pd.DataFrame(elbow_data)'''

'''df_elbow.hvplot.line(x="k", y="inertia", title="Elbow Curve", xticks=k)'''
visualized with this:

'''df_market_data.hvplot.line(
    width=800,
    height=400,
    rot=90
)'''

'''df_market_data_scaled_predictions.hvplot.scatter(x="price_change_percentage_24h", y="price_change_percentage_7d", by="Crypto Clusters")'''

'''df_market_data_pca_predictions.hvplot.scatter(x="1", y="2", by="Crypto Clusters PCA")'''
## Contributors
Michael Sullivan

Cal Berkeley Fintech 

Kevin Lee
