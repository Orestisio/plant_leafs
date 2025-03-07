We have 8 Plant species and 26 categories which may include _One or more_ __Disease__ and one __Healthy__ category.

![File and Category distribution](https://github.com/user-attachments/assets/4f5355b1-ae09-4676-beec-a461ebd70003)

Each label of the dataset is splited by ~40% of a value that the user choose from, in this case I choose the __mean__ value.
>  Validation splitof 20% and Test split of 20%. Labels that had not enough files for the full split we choose the half of that value.
> The amount of split was rounded down. In this case a choice has been made to be rounded form 241 to __200__.

On the __left image__ we have the File distribution after the split of validation and test set.
Based on the amount that we chose, label discrepancy will be compensated through augmentation. 
The __image on the right__ represents the amount of files that we need to reach.

| <img src="https://github.com/user-attachments/assets/f7b6ac74-8483-464e-b1d3-b0c4eebf096b" > | <img src="https://github.com/user-attachments/assets/abd08579-35fa-411c-b33c-3654d89f8ded"> |
|---|---|
