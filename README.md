# ML_regression
A typical workflow for a ML-based flux analysis is:
1. Using uproot to read a L2 root file and extract CALBranch into numpy format;
2. Arrange the CAL information into images;
3. Build a CNN, which takes the images as inputs;
4. Check the behavior of the model; If meet the requirement, then save the model;
5. Prepare the flight data in the same format, then load the saved model to make predictions;
6. With the recontructed energies, one could perform a flux analysis.
