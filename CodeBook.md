## Code Book

This code book will describe the data used in this project.
Steps for processing and to create the resulting tidy data set.

### Overview

30 volunteers performed 6 different activities while wearing a smartphone. The smartphone captured various data about their movements.

### Explanation of each file and the loaded variables

* `subject_train`: A vector that is loaded with data from 'train/subject_train.txt'. This has 7352 obs. of 1 variable
* `subject_test`: A vector that is loaded with data from 'test/subject_test.txt'. This has 2947 obs. of 1 variable
* `X_train`: A vector that is loaded with data from 'train/X_train.txt'. This has 7352 obs. of 561 variables
* `X_test`: A vector that is loaded with data from 'test/X_test.txt'. This has 2947 obs of 561 variables
* `y_train`: A vector that is loaded with data from 'train/y_train.txt'. This has 7352 obs. of 1 variable
* `y_test`: A vector that is loaded with data from 'test/y_test.txt'. This has 2947 obs. of 1 variable
* `featureNames`: A vector that is loaded with data from 'features.txt'. This has 561 obs. of 2 variables


* train is a vector that is created through cbind of subject_train, y_train and x_train vectors. This has 7352 obs. of 563 variables
* test is a vector that is created throguh cbind of subject_test, y_test, x_test vectors. This has 2947 obs. of 563 variables
* combined is a vector that is created through rbind of train and test vectors. This has 10299 obs. of 68 variables

* melted is a vector that is created as an objet into molten data frame
* tidy is  a vector that was created as a output file vector
### Data files that were not used

This analysis was performed using only the files above, and did not use the raw signal data. Therefore, the data files in the "Inertial Signals" folders were ignored.

### Processing steps

1. All of the relevant data files were read into data frames, appropriate column headers were added, and the training and test sets were combined into a single data set.
2. All feature columns were removed that did not contain the exact string "mean()" or "std()". This left 66 feature columns, plus the subjectID and activity columns.
3. The activity column was converted from a integer to a factor, using labels describing the activities.
4. A tidy data set was created containing the mean of each feature for each subject and each activity. Thus, subject #1 has 6 rows in the tidy data set (one row for each activity), and each row contains the mean value for each of the 66 features for that subject/activity combination. Since there are 30 subjects, there are a total of 180 rows.
5. The tidy data set was output to a CSV file.

