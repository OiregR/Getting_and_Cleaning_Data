

#Codebook

This document describes the variables of the output data set and summaries used to calculate the values, along with units and any other relevant information.

The first section summarizes relevant parts from the input data codebook. The next section describes the output variables with their units. The last section describes the transformations used to calculate the output values.

###Input Data

The original data set contains a codebook that describes the data set. In this section I repeat the parts of the codebook relevant to the generated data set.

The input data contains data recorded from the accelerometer and the gyroscope of a smartphone while the person who carried the smartphone was performing one of the following six activities: WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING.

###Input Data Variables

From the raw measurements, several other values were derived. The input dataset contains data for the following variables:

####Variable 	

tBodyAcc-XYZ 	    

tGravityAcc-XYZ 

tBodyAccJerk-XYZ

tBodyAccMag 

tGravityAccMag 

tBodyAccJerkMag 

fBodyAcc-XYZ 

fBodyAccJerk-XYZ

fBodyAccMag

fBodyAccJerkMag 

tBodyGyro-XYZ

tBodyGyroJerk-XYZ 

tBodyGyroMag

tBodyGyroJerkMag 

fBodyGyro-XYZ

fBodyGyroMag

fBodyGyroJerkMag

####source 	
accelerometer
gyroscope

####domain
time
frequency


The original sensor data was recorded at a rate of 50 Hz. The data was grouped into fixed-width sliding windows of 2.56 sec and 50% overlap (128 readings/window). Several functions where applied to these windows to compute the input features. The functions include:

    mean(): Mean value
    std(): Standard deviation
    mad(): Median absolute deviation
    and many others.

In total, each input record contains 651 features.

###Input Data Units

The accelerometer data is measured in standard gravity units 'g'. The gyroscope data is measured in radians/second.

The input features are normalized and bounded within the interval [-1,1]. During normalization the units have been divided by themselves so units have been cancelled.

###Structure of the input data

The input data is split into two subsets: a training set and a test set. Each subsets consists of three files:

  A features file (train/X_train.txt and test/X_test.txt) with one feature vector per row
  A label with one activity label per row (train/y_train.txt and test/y_test.txt)
  A file with a subject id per row (train/subject_train.txt and test/subject_test.txt)

The names of the features are listed in the file features.txt.

Additionally, the input contains the file activity_labels.txt which links the class labels with their activity name.

The input data set also contains the raw measurement data that was used to compute the features. This raw data is not being used in this project.

###Variable Units

subjectid: identifier of an observed volunteer within an age bracket of 19-48 years
    Data type: Numeric
    Value range: 1 - 30
activityname: Label string of the observed activity a person was performing
    Data type: factor
    Labels: WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING
Rows 3 - 68: Means of selected features per subjectid and activityname
    Data type: The feature means have the same units as their input data. Due to the normalization they do not have units attached see Input Data Units
    Value range: [-1, 1]

###Additional notes

Some input variable names contain the string 'BodyBody'. I considered this to be a typo and transformed it to the string 'Body'.
The original input data contained duplicated variable names. This does not affect our script since the features with duplicated names are not selected as source for the output data.

###Transformations

To compute the mean values for the features, the input data was grouped by column 1 and column 2. Afterwards the mean for each feature variable per group was computed.

The activity ids were converted to readable activity descriptions by loading the activity descriptions from the file "activity_labels.txt" provieded with the input data.

