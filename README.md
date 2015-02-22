# Getting_and_Cleaning_Data
This is a repository for the course project in Getting and Cleaning data

Purpose/Goal
The purpose of this project is to demonstrate ability to collect, work with, and clean a data set. The goal is to prepare tidy data that can be used for later analysis.  

Data
One of the most exciting areas in all of data science right now is wearable computing - see for example this article . Companies like Fitbit, Nike, and Jawbone Up are racing to develop the most advanced algorithms to attract new users. The data linked to from the course website represent data collected from the accelerometers from the Samsung Galaxy S smartphone. A full description is available at the site where the data was obtained:
http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones
Below is the link to the data for the project:
https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip

Requirements
Submit the following: 
1) a tidy data set 
2) a link to a Github repository with your script for performing the analysis
3) a code book that describes the variables, the data, and any transformations or work that were performed to clean up the data called CodeBook.md. 
4) A README.md should also be included in the repo with the scripts. This repo explains how all of the scripts work and how they are connected. 
5) R script called run_analysis.R that does the following:
  Merges the training and the test sets to create one data set.
  Extracts only the measurements on the mean and standard deviation for each measurement. 
  Uses descriptive activity names to name the activities in the data set
  Appropriately labels the data set with descriptive variable names. 
  From the data set in step 4, creates a second, independent tidy data set with the average of each variable for each   activity and each subject.


Explanation of the script

- Download the file and unzip the file in the UCI HAR Dataset folder in the working directory.
- Check the files inside the UCI HAR folder.
- Read the Activity files, Subject files and Features files.
- Merges the training and the test sets to create one data set for each.
- Set the variables names.
- Merge all three data sets using cbind to get the data frame "Data".
- Extracts only the measurements on the mean and standard deviation and create a subset to take names of Features with   "mean()" or "std()".
- Use descriptive activity names to name the activities in the data set.
- Appropriately label the data set with descriptive variable names.
-Create an independent tidy data set with the average of each variable for each activity.









