# MC_ACNNR
# Multi-channel attention based CNN for indoor localization using dual band data
# Multi-channel convolutional neural network with attention mechanism using dual-band WiFi signals for indoor positioning systems in smart buildings"

The article link: https://www.sciencedirect.com/science/article/pii/S2542660524003767

# Abstract
One of the most crucial Internet of Things (IoT) services for smart buildings is the indoor positioning service, which enables the detection of the exact location of any object within a closed area. Indoor localization, a significant aspect of Internet of Things, often relies on Received Signal Strength Indicator (RSSI) values from WiFi access points due to their ubiquity. However, the indoor localization systems face challenges like RSSI variance, device diversity, and fingerprint similarities. To address these challenges, most existing methods utilize machine learning and deep learning techniques. However, most existing methods introduce additional overhead through pre-processing steps such as filtering or signal transformation. Moreover, they commonly use the same feature space for different frequency bands, which causes ignores the specific statistical correlations of different frequency bands. To mitigate these issues and enhance accuracy without extra hardware, this paper proposes a dual-band approach utilizing 2.4 GHz and 5 GHz WiFi signals by using a multi-channel convolutional neural network regression with attention mechanism (MC-ACNNR). It aims to capture high-level correlations for each band data, and to fuse high-level patterns by combining two features map coming from different channels. The proposed method is tested on signal maps from four buildings across two datasets: UTMInDualSymFi and SODIndoorLoc. The results show that the proposed method achieves higher positioning performance compared to existing methods in the literature.

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


Please cite: 

Kakisim, Arzu Gorgulu, and Zeynep Turgut. "Multi-channel convolutional neural network with attention mechanism using dual-band WiFi signals for indoor positioning systems in smart buildings." Internet of Things 29 (2025): 101435.

@article{kakisim2025multi,
  title={Multi-channel convolutional neural network with attention mechanism using dual-band WiFi signals for indoor positioning systems in smart buildings},
  author={Kakisim, Arzu Gorgulu and Turgut, Zeynep},
  journal={Internet of Things},
  volume={29},
  pages={101435},
  year={2025},
  publisher={Elsevier}
}
