# PICAE PROJECT

PICAE – Intelligent Publication of Audiovisual and Editorial Contents

The PICAE project develops new models and analytical tools for recommending audiovisual and editorial content with the aim of improving the user experience, based on their profile and environment, and the level of satisfaction and loyalty. 

https://eurecat.org/en/portfolio-items/picae/

This repository contains the Python scripts (Jupyter notebook) used to study, process and analyze the audiovisual and editorial consumption data of the PICAE project (non-open data). 

## CAS OF STUDY 1: CCMA (Catalan Corporation of Audiovisual Media)
In this case we study the (delayed) consumption data of logged users for a period of 3 years (2019-2021). After filtering and processing the data, we have approximately 2,400,000 consumption records and 19 dimensions (date and time of consumption, duration, content, user id, device...).

### picae_consumption_processing.ipynb      
Given the original Dataset of consumption data: "consumption_data_logged_original.csv" this code cleans and processes the file and makes it ready to study the statistical patterns of consumption and apply the clustering algorithm. It returns the processed file:  "consumption_data_logged_processed.csv".

### picae_consumption_clustering_KPrototypes.ipynb      
Given the processed dataset "consumption_data_logged_processed.csv". This code executes the K-Prototypes algorithm. The output is the same file "consumption_data_logged_clusters.csv" with a new column added "Segment" that contains the cluster labels (in which cluster each consumption unit belongs to). 

### picae_results_consumption_statistics.ipynb     
Given the processed dataset, "consumption_data_logged_processed.csv", in this notebook we study the consumption patterns (probability density functions, mean values, etc).

### picae_results_consumption_clustering.ipynb     
Given the processed and clusterised dataset, "consumption_data_logged_clusters.csv", in this notebook we study the results of the clustering.


## CAS OF STUDY 2: GEC (Big Catalan Encyclopedia)
In this case we study the editorial consumption data of logged users for a period of 6 months (May-November 2022). We have approximately 115,000 consumption records and 12 columns/dimensions (date and time of consumption, user id, visited URL, browser...)

### picae_consum_GEC.ipynb
This jupyter notebook contains the study of the consumption data. In a first stage, we remove those columns (dimensions) that  are either irrelevant or uninformative (contain only one value or are not well informed). This procedure reduces the number of columns to 4, corresponding to the user ID, the visited URL, the timestamp of the visit (YYYY:MM:DD HH:MM:SS) and the day of the week (Monday-Sunday). In a second stage, each of the columns is analyzed in detail by obtaining the main statistics and visualizing the data (for example the probability density function of the visit time of the day). Then the consumption data is clusterized using the K-Prototypes algorithm. A thorough study is performed on the clustering results and the consumption groups found. Finally, the interevent time events (time between consecutive visits for a given user) are also studied.

### picae_users_GEC.ipynb
This jupyter notebook delves into the study of registered users who have consumed content from Encyclopaedia. A new data-set is created where the rows correspond to each user (2,475 unique users) and the columns represent the number of visits of each user in each consumption cluster (3 clusters) and in each weekday (7 days). Then, a second clustering algorithm is applied to users (DBSCAN) in order to find groups of users with a specific consumption profile. 


Each Jupyter Notebook contains a detailed description of the code and of the performed study (including an index).
