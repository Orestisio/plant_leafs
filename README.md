# Multi-classification of Plant Leaf Images 
Multi-classification of plant diseases based on cut leaf images. 

We are parsing the root location of our dataset and extract the 
*  Folder names(labels)
*  File_paths
*  The total amount of files for each folder.


## [Dataset Exploration and preparation](https://github.com/Orestisio/plant_leafs/tree/main/Prepare%20Dataset).
We perform Exploratory Data Analysis (EDA) to be acquainted with our dataset. 
We identify specific Plant and labels that don't have enough files in order to split to _validation_ and _test sets_ and are removed.

The dataset imbalance is _61%_ with 16 labels __below__ the mean value or at __risk__ and 11 labels of 5 Plant species occuping a file distribution below of 10% of the total distribution.
> Risk being vaues that __lower__ than the _half of the mean_.

We have 8 Plant species and 26 categories which may include _One or more_ __Disease__ and one __Healthy__ category.

![File and Category distribution](https://github.com/user-attachments/assets/4f5355b1-ae09-4676-beec-a461ebd70003)

Each label of the dataset is splited by ~40% of a value that the user choose from, in this case I choose the __mean__ value.
>  Validation splitof 20% and Test split of 20%. Labels that had not enough files for the full split we choose the half of that value.

Original images from each label are taken and are used for augentation. The augmentations are responsible to mimic __weather__, __light conditions__.
Each image will be passed by __3 Augmentation functions__:
1.  Weather transformations
2.  Light transformations
3.  Geometrical transformations.

