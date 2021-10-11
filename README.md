# SNVR SRCNN
Super resolving sparse astronomical X-ray imagery using deep learning.\
Reference Paper: **Link to paper** \
Corresponding Author: Hannah Collier, University College London.\
Contributors: Hannah Collier, William R. Dunn, Yu Tao, Graziella Branduardi Raymont, Jan Peter Muller.

# Description: 
SNVR SRCNN is a deep learning based method for performing single image super resolution restoration on sparse X-ray astronomical imagery.\
**Add details about the required setup and software necessary to run this code**\
**Maybe also include a pretrained model for demonstration purposes**

# SNVR Dataset Preparation:
To prepare the SNVR dataset:
1. Download and save the .fits files in the folder named "FITS Files" to a given directory.
1. In the file "Create SNVR Dataset from Fits", replace the "path to fits files" on line 12, with the path to where you have saved the fits files.
1. Replace "path to directory" in this code with where you wish to store the created .tif files.
1. Run code.

# Training a Model
## How to Train the SNVR model
1. Replace "path to directory" in the SNVR_SRCNN/SNVR_Experiments/SNVR_readin_and_train file with the path to the folder in which the SNVR images you previously created are stored. 
1. Add a line at the end of the code to save the trained model, if you wish. You can use tensorflow's model.save('path/to/directory').
1. Run the code in SNVR_readin_and_train to train the model. 

## How to Train the Div2k model
1. The code in SNVR_SRCNN/Div2k_Experiments/div2k_readin_and_train reads in the div2k dataset, performs all necessary preprocessing and trains the model on this data.
1. You may wish to add a line at the end of the file to save the trained mode, as previous.

## Finetuning the Div2k Model on SNVR Data
1. In SNVR_SRCNN/Finetuning Experiments/finetuning_training, include the file location of the saved div2k model, in line 11. 
1. Replace "path to directory" on line 13 with the file location of the saved SNVR .tiff dataset.
2. Add a line to save the model to your preferred location.
3. Run code.

## Image Quality Assessment Metric Computation
1. Fill in the path to the folder in which you saved the test images on line 5 of Calculate_IQA_on_test_images.
2. Fill in the path to the saved model which you want to test on line 35.
3. Run code.

Please contact Hannah Collier at hannah.collier.20@ucl.ac.uk if you have any questions or are interested in contributing!
