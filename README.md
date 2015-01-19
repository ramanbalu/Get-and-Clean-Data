## This is course project work that is part of 
## "Getting and Cleaning Data"

** Here are the steps that must be performed before running the R script:**

1. Download the zip file from [this URL](https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip).
2. Unzip the file to "UCI HAR Dataset" directory
3. Set working directory to "UCI HAR Dataset".
4. Ensure that you have 2 sub directories, ie test and train.
5. Ensure that test folders has 3 txt files namely subject_test.txt, x_test.txt and y_test.txt
6. Ensure that train folders has 3 txt files namely subject_train.txt, x_train.txt and y_train.txt

** Note: Folders and files specified in step 4, 5 & 6 are created when you unzip the zip file that you have downloaded.

** Once those steps are complete, you can run the R script - run_analysis.R.
** Note that it requires the [reshape2 package](http://cran.r-project.org/web/packages/reshape2/index.html), which can be downloaded from CRAN.

** The output of the R script is a tidy data set - tidy.csv

** You can read more about the data and the analysis in the code book - CodeBook.md.

