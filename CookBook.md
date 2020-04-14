1.) Download the dataset
Dataset was downloaded and input into R


2.) Assigning variables
subject_test <- test/subject_test.txt 
  subject IDs for test
x_test <- test/X_test.txt 
  variables in test 
y_test <- test/y_test.txt 
  ID for test
subject_train <- test/subject_train.txt 
  subject IDs for train
x_train <- test/X_train.txt 
  variables in train
y_train <- test/y_train.txt 
  ID in train
features <- features.txt 
  Label of each variable
activity_labels <- activity_labels.txt 
  Labels of activities performed
subject_test <- test/subject_test.txt  
  test subjects observed


3.) Merges the train and test sets to one data set
X: merged x_train and x_test using rbind()
Y: merged y_train and y_test using rbind()
Subject: merged subject_train and subject_test using rbind()
Merged: merged Subject, Y and X using cbind()


4.) Extracts only the measurements on the mean and standard deviation for each measurement
extract is created by subsetting Merged, selecting only columns subject, code and the measurements on the mean and standard deviation


5.) Uses descriptive activity names to name the activities in the data set
Numbers in code column of the extract replaced with corresponding activity from second column of the activities variable


6.) Appropriately labels the data set with descriptive variable names
code column in extract renamed into activity_labels
Column names were replaced with the descriptive variable names (Accelerometer, Gyroscope, Body, MAgnitude, etc.) 

7.) From step 4, create a second, independent tidy data set with the average of each variable for each activity and each subject
Final is created by sumarizing extract taking the means of each variable for each activity and subject, after groupped by subject and activity.
Export Final into Final.txt file.
