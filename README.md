Getting-and-Cleaning-Data
=========================

This repo contains files related to Course Project of Getting and Cleaning Data

Functions performed by R script...

Merges the training and the test sets to create one data set.
Extracts only the measurements on the mean and standard deviation for each measurement.
Uses descriptive activity names to name the activities in the data set
Appropriately labels the data set with descriptive activity names.
Creates a second, independent tidy data set with the average of each variable for each activity and each subject.

Below is the description of steps...

Download the dataset (create a directory and download dataset in that directory)
Use rbind to create the merged data set (this is assigned to variable X). This solves first problem  
Use grep function to get std() and mean() features, subset the dataset for only mean and std using this information .The result is in mean_std variable. This solves second problem
Load the activity labels, merge test and train data using rbind. Loop through activity names and replace activity indexes with names.  This solves third problem
Combines the labels and the data set using cbind . Do this operation for both mean_std and X. That solves fourth problem. (It was not clear if I have to do it for data set only. So I did it for mean_std also)
To address problem 5, first merge subject (test and train), then aggregate dataset X (using mean for averaging) by activity and subject. Save the result in tidy_data.txt file.
