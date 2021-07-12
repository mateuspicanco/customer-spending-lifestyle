# Identifying Lifestyle Patterns in Credit Card Spending

This project aims at illustrating novel approaches to customer segmentation using Credit Card Records (CCRs) by leveraging modeling techniques similar that of text mining tasks. It is based on the [Sequences of purchases in credit card data reveal lifestyles in urban populations](https://www.nature.com/articles/s41467-018-05690-8) by Clemente Et al, that elucidates patterns in sequences credit card transactions in different merchant categories as a means of uncovering user lifestyles when verifying results on sociodemographic data about the users.

My take on this idea is to develop a clustering mechanism based on `topic modeling` techniques rather than using traditional clustering approaches (based of raw spending). The idea is that sequences of events are more representative of peculiar purchasing patterns, as they do not take into account biases related to the different categories (such as transactions on Airlines being more expensive than those on restaurants), as well as income-related biases (customers spending more or less on their credit cards).

The results were significant, as peculiar spending patterns were found using a `Latent Dirchlett Allocation` model.

# Data Sources
The dataset used for this project was provided by IBM researchers in [this link](https://data.world/ealtman/synthetic-credit-card-transactions). The dataset spans over 15 years of synthetic and realistic credit card records for `2000` distinct users. A [paper](https://arxiv.org/abs/1910.03033) about the dataset is also provided. 

# Technologies used for this project
1. Data Processing: `Apache Spark`, `pandas`, `numpy`;
2. Data Visualization: `plotly`, `seaborn`, `matlotlib`, `pyLDAvis`;
3. Modeling: `gensim`, `umap`, `hdbscan`, `sklearn`;
4. Versioning: `dvc`;

# Results
The plots below illustrate a few of the results obtained:

![LDA Clusters Example](reports/img/LDA_CLUSTERS.png)
> Example of the clusters identified by the LDA topic model over the UMAP projection.

![LDA Topic Distance Map](reports/img/LDA_PREM_MODEL_SCREEN.png)
> Inter-topic distance map on PCA projections for the clusters (topics) identified.

![Summary of LDA Results over the Different MCCs](reports/img/AVERAGE_FREQ_MCC_LDA.png)
> Frequency of transactions in different merchant categories identified in LDA clusters.



