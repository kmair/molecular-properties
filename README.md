# Molecular properties prediction

This repository contains the prediction for the 
[CHAMPS - Predicting molecular properties](https://www.kaggle.com/c/champs-scalar-coupling)
Kaggle competition. The project is split into several jupyter notebooks as all of the training was carried out on Kaggle. 

## Basic outline

The dataset has `2358657` atoms and fitting various properties requires surplus time. To complete the execution within the 6 hour limit,
the process of training was split and the output of one notebook was used as an input for the subsequent file.
Since the analysis was carried out on Kaggle, all of the files were inherited from the previous notebook created and must be taken
care of while inheriting the data. The flow of the files is:

**1. create-acsf-structures:** Uses the principle of ACSF to make the spatial position independent of orientation.

**2. merge-acsf-structures-data:** Merges the various features created above into train and test dataset for prediction.

Now that we have the ACSF features, we need to use it to predict properties only available in train set and not the test set. 
2 predictions will be done for scalar coupling constants and Mulliken charges.

**3 a. predict-scalar-coupling-constants:** Predicts the 4 scalar coupling constants on the test dataset

**3 b. predict-mulliken-charges:** Predicts the Mulliken charges on the test dataset

**4. output-predictions:** Finally, using all the features, we create the output features.

## Final thoughts

As remarked in `output-predictions` we need improved feature engineering and more training epochs to improve the performance.
