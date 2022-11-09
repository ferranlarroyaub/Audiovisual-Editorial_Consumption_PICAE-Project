# PICAE PROJECT

PICAE – Intelligent Publication of Audiovisual and Editorial Contents

The PICAE project develops new models and analytical tools for recommending audiovisual and editorial content with the aim of improving the user experience, based on their profile and environment, and the level of satisfaction and loyalty. 

https://eurecat.org/en/portfolio-items/picae/

This repository contains the Python scripts (Jupyter notebook) used to study, process and analyze the audiovisual and editorial consumption data of the PICAE project (non-open data). 

## CAS OF STUDY 1: CCMA (Catalan Corporation of Audiovisual Media)

### picae_consumption_processing.ipynb      
Given the original Dataset of consumption data: "consumption_data_logged_original.csv" this code cleans and processes the file and makes it ready to study the statistical patterns of consumption and apply the clustering algorithm. It returns the processed file:  "consumption_data_logged_processed.csv".

### picae_consumption_clustering_KPrototypes.ipynb      
Given the processed dataset "consumption_data_logged_processed.csv". This code executes the K-Prototypes algorithm. The output is the same file "consumption_data_logged_clusters.csv" with a new column added "Segment" that contains the cluster labels (in which cluster each consumption unit belongs to). 

### picae_results_consumption_statistics.ipynb     
Given the processed dataset, "consumption_data_logged_processed.csv", in this notebook we study the consumption patterns (Pdfs, mean values, etc).

### picae_results_consumption_clustering.ipynb     
Given the processed and clusterised dataset, "consumption_data_logged_clusters.csv", in this notebook we study the results of the clustering.


## CAS OF STUDY 2: GEC (Big Catalan Encyclopedia)
