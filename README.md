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
preprocessing_data.ipynb: firstly run this file to normalize the data and create final .csv files

SOD_machine_learning.ipynb: run this file to obtain performance values for indoor localization using machine learning based regression models.

SOD_deep_learning.ipynb: run this file to obtain performance values for indoor localization using deep learning based regression models.

