# GettingAndCleaningData
Getting And cleaning Data

# Getting and Cleaning Data Course Project

The files in this folder provide a solution for the Coursera "Getting And Cleaning Data" course project. 

## The Transformation Script run_analysis.R

The file run_analysis.R contains an R script for transforming the original dataset into a second dataset according to the following rules:

You should create one R script called run_analysis.R that does the following:

1. Merges the training and the test sets to create one data set.
2. Extracts only the measurements on the mean and standard deviation for each measurement. 
3. Uses descriptive activity names to name the activities in the data set
4. Appropriately labels the data set with descriptive variable names. 
5. From the data set in step 4, creates a second, independent tidy data set with the average of each variable for each activity and each subject.

### Running The Script

The script requires the package dplyr.

The script assumes that the extracted dataset can be found in the current working directory, i.e. the current working directory contains the folder ```UCI HAR Dataset```. 

To run the script ```run_analysis.R```:

1. put it into the parent folder of ```UCI HAR Dataset```
2. launch an R session and change into that directory using the ```setwd``` command
3. type ```source("run_analysis.R")``` to execute the script

The script will read the test and training data from the folder ```UCI HAR Dataset```, apply the transformations listed above and write the result to the file "tidydata.txt" in the current working directory.

The file "tidydata.txt" can be read into a data.frame using

```R
read.table("tidydata.txt", header = T)
```

## The codebook. 

The codebook is contained in the file CodeBook.md. It describes the variables of the output data set and summaries used to calculate the values, along with units and any other relevant information.




