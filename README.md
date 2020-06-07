# Using a Convolutional Neural Network (CNN) with Bayesian Optimization to Identify Cerebral Micro-Bleeds

NOTE: Created in Python 3.

## Description

Cerebral micro-bleeds (CMBs) are small chronic brain hemorrhages caused by structural abnormalities in brain vessels. Owing to the paramagnetic properties of blood, these bleeds can be detected in vivo using MRI. However, manual detection is time-consuming, less accurate, and subjective, especially due to their complex morphological structure and widespread distribution throughout the brain. Hence, we created a classifier that is quick to train and about 99% accurate on this task. The classifier is constructed using [Keras](https://keras.io/) and utilizes [Bayesian optimization](https://github.com/fmfn/BayesianOptimization) to automate hyper-parameter learning.

| <img src="/sample_images/cmb.png" width="400"> | <img src="/sample_images/non_cmb.png" width="400"> |
| CMB Samples | Non-CMB Samples |


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
