# Using a Convolutional Neural Network (CNN) with Bayesian Optimization to Identify Cerebral Micro-Bleeds

NOTE: Created in Python 3.

## Description

Cerebral micro-bleeds (CMBs) are small chronic brain hemorrhages caused by structural abnormalities in brain vessels. Owing to the paramagnetic properties of blood, these bleeds can be detected in vivo using MRI. However, manual detection is time-consuming, less accurate, and subjective, especially due to their complex morphological structure and widespread distribution throughout the brain. Hence, we created a classifier that is quick to train and about 99% accurate on this task. The classifier is constructed using [Keras](https://keras.io/) and utilizes [Bayesian optimization](https://github.com/fmfn/BayesianOptimization) to automate hyper-parameter learning.

The images below present a few CMB and non-CMB samples.
<img src="/sample_images/cmb.png" width="400"> | <img src="/sample_images/non_cmb.png" width="400">
:---: | :---:
CMB Samples | Non-CMB Samples


## Repository Tree
```
./cerebral-micro-bleeds-detection
├── sample_images                                 # Contains sample images
│   └── ...
├── README.md
├── cmb_detection.ipynb                           # Notebook to run
└── dataset_41_41_1_13031.mat                     # Dataset
```

## Frameworks/Tools

- [Keras](https://keras.io/)
- [Bayesian Optimization](https://github.com/fmfn/BayesianOptimization)

## Usage

Cells in [cmb_detection.ipynb](/cmb_detection.ipynb) are to be run sequentially from top to bottom. A brief description about the function of each cell is provided below.

Cell Title | Cell Description
:---: | ---
Import Modules | Imports all the required modules.
Settings | Sets the following parameters: seeds, split fraction, iterations of grid search, iterations of random search, iterations of Bayesian optimization, and epochs for training the CNN.
Functions | Defines entities like the CNN structure, image augmentations, objective function for Bayesian optimization, and evaluation metrics.
Create Train/Test Sets | Splits the dataset into train and test sets. The train set undergoes image augmentation and test set remains un-augmented. Hold-out validation is used here.
Preview Samples | Displays samples from the train set.
Grid Search | Finds the optimum set of hyper-parameters for the model using grid search.
Random Search | Finds the optimum set of hyper-parameters for the model using random search.
Bayesian Optimization | Finds the optimum set of hyper-parameters for the model using Bayesian optimization.
Comparing Results | Retrains the model using hyper-parameter sets obtained from grid search, random search, and Bayesian optimization. Compares the accuracy, sensitivity, specificity, and precision obtained from these methods.
