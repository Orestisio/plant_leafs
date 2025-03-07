We have 8 Plant species and 26 categories which may include _One or more_ __Disease__ and one __Healthy__ category.

![File and Category distribution](https://github.com/user-attachments/assets/4f5355b1-ae09-4676-beec-a461ebd70003)

Each label of the dataset is splited by ~40% of a value that the user choose from, in this case I choose the __mean__ value.
>  Validation splitof 20% and Test split of 20%. Labels that had not enough files for the full split we choose the half of that value.
> The amount of split was rounded down. In this case a choice has been made to be rounded form 241 to __200__.

Furthermore we compute based on the files after the split _how many_ __original images__ we need to augment in order to reach the total amount of files that the user chose. (In this case the mean value)

On the __left image__ we have the File distribution after the split of validation and test set.
Based on the amount that we chose, label discrepancy will be compensated through augmentation. 
The __image on the right__ represents the amount of files that we need to reach with augmentation for each label.

| <img src="https://github.com/user-attachments/assets/f7b6ac74-8483-464e-b1d3-b0c4eebf096b" > | <img src="https://github.com/user-attachments/assets/abd08579-35fa-411c-b33c-3654d89f8ded"> |
|---|---|


The Augmentation process includes 3 functions in order to simulate __weather__ and __light__ conditions of the real-world, and geometrical transformations.
Each Augmentation produce different transformations:
1. Weather -> Rain, Snow
2. Light -> Multiplicative noise, Grid Cutout
3. Geometrical -> CLAHE, Horizontal, Vertical Flip

each run does not produce same outcome and through the pipeline we do a round of 5 runs. 

This means that if we pass 1 image through our pipeline we produce 15 new images.
![Screenshot 2025-03-07 130233](https://github.com/user-attachments/assets/ecc27694-1185-4034-96d3-d34e30e21fee)
