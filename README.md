# DCNN_sandbar_seg_GRCA
Data, tools, and scripts used in manuscript "Semantic Segmentation of Time Series Imagery using Deep Convolutional Neural Networks: A Case Study of Sandbars in Grand Canyon"


Within this repository you will find all the scripts and data necessary to repeat our study.

we provide the image pre-processing steps for four of the ten sites. To demonstrate the workflow
Images used for training and testing all ten sites are included.

This repo contains the following directories
'Calibration_and_remove_distortion'
	Provides files and scripts necessary to undistort four of the sites in this study
	> calibration_images 
	> Matlab calibration session file
	> and scripts to undistory each site 
'labeling'
	everything in labeling folder was taken from
		https://github.com/dbuscombe-usgs/dl_tools.git
		with significant updates by https://gitlab.nps.edu/bbwells/labeling
		params.py files for two of the ten sites are provided.
'Rectification'
	contains scripts and data used to rectify four of the ten sites. 
	Convert_Panels_EN_to_KML.ipynb :
		> this jupyter notebook allows you to convert eastings and northings to KML to visualize GCPs on google earth
	RCXXXXX
		> each of these directories contains 2017 and 2019 GCP images, KMLs, and correspondences between E,N, and image coordinates
		> rectification error surfaces
		> jupyter notebooks showing how GCPs were used to create homographies and generate error surfaces for 2017 & 2019
'Registration'
	Registration_tools.py
	>Contains all of the functions necessary to register imagery from sandbar sites, all three methods
	>provides examples with jupyter notebooks on how to register imagery for two sites
'Segmentation'
   The following four scripts contain all of the functions needed to complete image segmentation.
   TO DO: add jupyter notebook or google colab notebook demonstrating workflow for segmentation.
	DCNN_support_scripts.py
	support_scripts.py
	Unet_models.py
	
'Splitting_sampling_imagery'
	contains scripts useful for sampling imagery, and splitting into test and train
'one_site_train'
	contains rectified image label pairs from RC0307Rf used to train the DCNN
'five_site_train'
	Contains rectified image label pairs from RC0307Rf, RC0220Ra, RC0235L, RC0566R, RC1459L
'three_site_train'
	Contains rectified image label pairs from RC0307Rf, RC0220Ra, RC0235L 
'test1_site'
	contains rectified image label pairs from RC0307Rf used to test the DCNN
'test3_site'
	Contains rectified image label pairs from RC0307Rf, RC0220Ra, RC0235L 
'test5_site'
	Contains rectified image label pairs from RC0307Rf, RC0220Ra, RC0235L, RC0566R, RC1459L
'test10_site'
	Contains rectified image label pairs from RC0307Rf, RC0220Ra, RC0235L, RC0566R, RC1459L, RC1227R, RC0917R, RC1377L, RC1946L, RC1044R
	
	
Augmented image data sets were not included due to their large size. Scripts and jupyter notebooks needed to complete
image augmentation can be found in the 'Splitting_sampling_imagery' directory.	
	