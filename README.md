# Multi-classification of Plant Leaf Images 
Multi-classification of plant diseases based on cut leaf images.
*  Data Preparation
*  Model Definition
*  Folder __Modules__ if we want to package our Functionalities.
*  [Kaggle](https://www.kaggle.com/code/creativetank/plant-leafs): a single script that has all the processes & functionalities to run the hole project
    *  Data is already processed and prepared to ready to go splits stored in Kaggle, here we just __LOAD__
    *  Here we have a simple function to load & prepare specific collection of models


## [Dataset Exploration and preparation](https://github.com/Orestisio/plant_leafs/tree/main/Prepare%20Dataset).
Data engineering + augmentation pipeline with Python and Tensorflow
*  Parsing and structuring the dataset
*  Performing EDA and imbalance analysis
*  Designing intelligent train/validation/test splitting logic
*  Building an augmentation pipeline with controlled balancing strategies
*  Supporting both local persistence and streaming-based augmentation for memory efficiency

We perform Exploratory Data Analysis (EDA) to be acquainted with our dataset and create file with dataset statistics for further processing. 
We identify specific Plant and labels that don't have enough files in order to split to _validation_ and _test sets_ and are removed.

The dataset imbalance is _61%_ with 16 labels __below__ the mean value or at __risk__ and 11 labels of 5 Plant species occuping a file distribution below of 10% of the total distribution.
> Risk being vaues that __lower__ than the _half of the mean_.

![Screenshot 2025-03-07 112243](https://github.com/user-attachments/assets/ff8474b3-7437-4c02-ad6a-b96bbfa4891c)

## [Model Definition and Creation](https://github.com/Orestisio/plant_leafs/blob/main/Models).
A modular deep learning experimentation framework to generate multiple model variations automatically 
*  Select from Pretrained CNN Backbones 
*  Addition of Custom classification "heads"
*  Optionaly load architectures/weights from files 
*  Automated experimentation and benchmarking workflows

##   [Kaggle](https://www.kaggle.com/code/creativetank/plant-leafs)
Here we have a single script that runs the hole project with all the final outputs.
The data preparation already took place and the new splits are stored in Kaggle ready to be loaded.
>   Code that is wraped in comments is the trial of streamlinng the Augmentantion process while loading data to train the model.
> It was not 100% succesful or efficient at that moment thus is frozen.
The models are defined , created and compiled. They are splited in groups in order to produce answers to different questions.
Then __training__ takes place and we __evaluate__  our models with unseen data.
> Confusion matrix with other graphs have been produced

