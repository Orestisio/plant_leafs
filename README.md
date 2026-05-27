# Multi-classification of Plant Leaf Images 
Multi-classification of plant diseases based on cut leaf images. 

We are parsing the root location of our dataset and extract the 
*  Folder names(labels)
*  File_paths
*  The total amount of files for each folder.


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

## Model Definition and Creation
