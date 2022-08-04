# ML_regression
A typical workflow for a ML-based flux analysis is:
1. Using uproot to read a L2 root file and extract CALBranch into numpy format;
2. Arrange the CAL information into images;
3. Build a CNN, which takes the images as inputs;
4. Check the behavior of the model; If meet the requirement, then save the model;
5. Prepare the flight data in the same format, then load the saved model to make predictions;
6. With the recontructed energies, one could perform a flux analysis.

Steps:
0. Install tensorflow, uproot, astropy.table, glob, os;
1. Download MC root files from NKU server for preparing training samples. Use "flat" files for individual elements.
2. Convert root file into images that tensorflow can read using training_sample_preparation.ipynb;
3. Train the model using train_cnn_energy_reconstruction.ipynb. I have already save some trained models. But when new version of data is available, models should be updated.
4. Convert the root file that needs energy reconstruction into images using prediction_preparation.ipynb;
5. Energy reconstruction is included in the codes for flux analysis. 
