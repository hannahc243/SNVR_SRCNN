# SNVR SRCNN
Super resolving sparse astronomical X-ray imagery using deep learning.\
Reference Paper: **Link to paper** \
Corresponding Author: Hannah Collier, ETH Zürich, FHNW.\
Co-authors: Hannah Collier, William R. Dunn, Yu Tao, Graziella Branduardi Raymont, Jan Peter Muller.

# Description: 
SNVR SRCNN is a deep learning based method for performing single image super resolution restoration on sparse X-ray astronomical imagery.

# SNVR Dataset Preparation:
The SNVR dataset can be prepared by downloading the relevent .fits files from https://cda.harvard.edu/chaser/. The code "Create SNVR Dataset from Fits", reads in the fits files and performs the outlined preprocessing, the images are saved as .tiff files.

# Training a Model
## How to Train the SNVR model
The code in SNVR_readin_and_train reads in the previously created SNVR dataset and trains the convolutional network.

## How to Train the Div2k model
The code in SNVR_SRCNN/Div2k_Experiments/div2k_readin_and_train reads in the div2k dataset, performs all necessary preprocessing and trains the model on this data.

## Finetuning the Div2k Model on SNVR Data
Finetuning the div2k model can be done in finetuning_training.py by reading in the previously trained model and running it on new SNVR data.

## Image Quality Assessment Metric Computation
The code Calculate_IQA_on_test_images calculates the IQA scores based on the saved models.

Please contact Hannah Collier at hannah.collier.20@ucl.ac.uk if you have any questions or are interested in contributing!
