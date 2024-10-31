# MC_ACNNR
Multi-channel attention based CNN for indoor localization using dual band data
# Introduction
This paper proposes a dual-band approach utilizing 2.4GHz and 5GHz WiFi signals by using a multi-channel convolutional neural network regression with attention mechanism (MC-ACNNR). 
It aims to capture high-level correlations for each band data, and to fuse high-level patterns by combining two features map coming from different channels. 
The proposed method is tested on signal maps from four buildings across two datasets: UTMInDualSymFi and SODIndoorLoc.
# Datasets
Please download the dataset from this link 

SODIndoorLoc
https://github.com/renwudao24/SODIndoorLoc

UTMInDualSymFi
https://zenodo.org/records/7260097
# Run

Used jupyter notebook and Anaconda Enviroment

Download Training_SYL_All_30.csv and  Testing_SYL_All.csv in SYL folder of SODIndoorLoc dataset, make a folder named "data", and save them Training_SYL.csv and Testing_SYL.csv.

preprocessing_data.ipynb: firstly run this file to normalize the data and create final .csv files, and save them to SYL_preprocessed folder. We use selected MACs that were defined as 2.4 GHz and 5GHz in the file, named "Information of pre-installed APs.xlsx". For SYL building, there exist 23 MACs for 2.4 GHz and 23 MACs for 5 GHZ. We selected 46 MACs for our training and testing phases.

SOD_machine_learning.ipynb: run this file to obtain performance values for indoor localization using machine learning based regression models.

SOD_deep_learning.ipynb: run this file to obtain performance values for indoor localization using deep learning based regression models.
For MC-ACNNR, one channel takes 23 MACs for 2.4 GHz, and other channel 23 MACs for 5 GHz.

