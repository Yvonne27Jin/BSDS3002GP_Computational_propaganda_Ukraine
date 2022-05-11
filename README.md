

# Readme

This is a course project of BSDS3002 Social computing from HKU. We aim to understand how both sides of Rassian-Ukrainian conflict used computational propaganda on twitter and how their influence and strategies differ. The complete report can be found [here](https://github.com/Yvonne27Jin/BSDS3002GP_Computational_propaganda_Ukraine/blob/main/Group%20Project%20Report.pdf).

We used the "[Ukraine Conflict Twitter Dataset](https://www.kaggle.com/datasets/bwandowando/ukraine-russian-crisis-twitter-dataset-1-2-m-rows/code?select=UkraineCombinedTweetsDeduped_FEB28_part1.csv.gzip)" on Kaggle. 

## Code

In "code" file there are all the code for data processing and network analysis, and this includes:

- [0_DCol.ipynb](https://github.com/Yvonne27Jin/BSDS3002GP_Computational_propaganda_Ukraine/blob/main/code/0_DCol.ipynb): Ramdom data sampling and regrouping.
- [1_DPP.ipynb](https://github.com/Yvonne27Jin/BSDS3002GP_Computational_propaganda_Ukraine/blob/main/code/1_DPP.ipynb): Data processing
  - hashtag sorting 
  - political stance categorisation of tweets and users 
  - tweet text processing 
- [2_SEDA.ipynb](https://github.com/Yvonne27Jin/BSDS3002GP_Computational_propaganda_Ukraine/blob/main/code/2_SEDA.ipynb): Simple Exploratory data analysis (EDA)
  - Discussion trend by political stance
  - Word clouds for both stances at different timeframe
- [3_NCon_N.ipynb](https://github.com/Yvonne27Jin/BSDS3002GP_Computational_propaganda_Ukraine/blob/main/code/3_NCon_N.ipynb): Network Construction
  - Bipartite Network construction
  - Projected one-mode user network
  - Export edgelist and nodelist for Gephi visualisation
  - node attributes: political orientation index and eigenvector centrality
- [4_NAna.ipynb](https://github.com/Yvonne27Jin/BSDS3002GP_Computational_propaganda_Ukraine/blob/main/code/4_NAna.ipynb): Bot detection
  - Bot detection using botometer API
- [5_bipartite_network_analysis.ipynb](https://github.com/Yvonne27Jin/BSDS3002GP_Computational_propaganda_Ukraine/blob/main/code/5_bipartite_network_analysis.ipynb): Network analysis
  - network properties: size, density, diameter, Average shortest path length, centrality, etc.
- [6_Propaganda.ipynb](https://github.com/Yvonne27Jin/BSDS3002GP_Computational_propaganda_Ukraine/blob/main/code/6_Propaganda.ipynb): Trend and information flow of Russia propaganda
  - discussion trend of the following keywords by time and political stance
    - "special military operation"
    - "Neo Nazis" and "fascists"

## Dataset

Code folder also include the most important datasets:

[20220502_resampled_dataset.csv](https://github.com/Yvonne27Jin/BSDS3002GP_Computational_propaganda_Ukraine/blob/main/code/20220502_resampled_dataset.csv) contains the raw data of tweets randomly sampled from the Kaggle dataset.

[labelled.txt](https://github.com/Yvonne27Jin/BSDS3002GP_Computational_propaganda_Ukraine/blob/main/code/labelled.txt) includs the final list of most frequent hashtags manually labelled for political stance.



## Visualisation

[Figures](https://github.com/Yvonne27Jin/BSDS3002GP_Computational_propaganda_Ukraine/tree/main/Figures) folder has all the plots of tweeter trends, including wordclouds, frequency histogram of hashtags, and density distribution of tweet/user creation time. 

We used Gephi to visualise the networks. In the Gephi visualisation folder:

[nodelist1.csv](https://github.com/Yvonne27Jin/BSDS3002GP_Computational_propaganda_Ukraine/blob/main/code/nodelist1.csv) and [nodelist2.csv](https://github.com/Yvonne27Jin/BSDS3002GP_Computational_propaganda_Ukraine/blob/main/code/nodelist2.csv): Node list exported for Gephi visualisation, containing user information of userid,username, user created date, No. Following and followers, total number of tweets, political orientation index, politcal categorization, and eigenvector centrality in the projected user network.

<u>projected_w_user_edgelist_1.csv</u> and <u>projected_w_user_edgelist_2.csv</u>: Weighted edgelist for the projected user network, where node representing users, edge representing the action of sharing the same tweet, and weight representing the number of overlapping tweets.

<u>clusters_viz1_new.gephi</u> and <u>clusters_viz2_new.gephi</u> are the updated Gephi graph file where we produced the network visualisation in the report. 

