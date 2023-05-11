# DeepLearningDSREstimation
[![DOI](https://zenodo.org/badge/612833214.svg)](https://zenodo.org/badge/latestdoi/612833214)

## Abstract
The retrieval of downward shortwave radiation (DSR) with high spatiotemporal resolution and short latency is critical. It is the fundamental driving force of surface energy, carbon and hydrological circulations, and a key energy source for photovoltaic electricity. However, existing methods face significant challenges owing to cloud heterogeneity and their reliance on other satellite-derived products, which hinder the retrieval of accurate and timely DSR with high spatiotemporal resolution. In addition to the spectral features used in traditional approaches, deep learning (DL) can incorporate the spatial and temporal features of satellite data. This study developed and compared three DL methods, namely the DenseNet, the bidirectional gated recurrent unit without surface albedo as inputs (BiGRU_nor), and the convolutional neural network with gated recurrent unit  without surface albedo as inputs (CNNGRU_nor). These methods were used to estimate DSR at 1 km and 10/15 min resolutions directly from top-of-atmosphere reflectance over the Advanced Himawari Imager (AHI) onboard Himawari-8 and the Advanced Baseline Imager (ABI) onboard GOES-16 coverage, achieving high accuracies. The instantaneous root mean square error (RMSE) and relative RMSE for the three models were 68.4 (16.1%), 69.4 (16.3%), and 67.1 (15.7%) W/m^2, respectively, which are lower than the baseline machine learning method, the multilayer perceptron model (MLP), with RMSE at 76.8 W/m^2 (18.0%). Hourly accuracies for the three DL methods were 58.6 (14.1%), 57.8 (14.0%), and 57.3 (13.8%) W/m^2, which are within the DSR RMSEs that we estimated for existing datasets of the Earth's Radiant Energy System (CERES) (88.8 W/m^2, 21.4%) and GeoNEX (77.8 W/m^2, 18.8%). The study illustrates that DL models that incorporate temporal information can eliminate the need for surface albedo as an input, which is crucial for timely monitoring and nowcasting of DSR. Incorporating spatial information can enhance the retrieval accuracy in overcast conditions, and incorporating infrared bands can further improve the accuracy of DSR estimation.

## Models
The configuration of each model are summarized in DSR_Models.ipynb file. The final models are also uploaded as .h5 file. 
The TensorFlow 2.0.0 are used for traning DenseNET and CNNGRU models and the TensorFlow 2.7.0 are used for training MLP and BiGRU.

## Dataset
Reduced training dataset of each model is uploaded. The dataset has been pre-processed and normalized. 
