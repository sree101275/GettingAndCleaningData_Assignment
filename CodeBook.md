CodeBook for Getting and Cleaning Data Project

Data Source:

Site from where the Data was fetched

http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones 
Data for the Project

https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip 
Saved in the Working Directory as folder named:

    UCIHAR Dataset

About the Data set :

The experiments have been carried out with a group of 30 volunteers within an age bracket of 19-48 years. Each person performed six activities (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING) wearing a smartphone (Samsung Galaxy S II) on the waist. Using its embedded accelerometer and gyroscope, we captured 3-axial linear acceleration and 3-axial angular velocity at a constant rate of 50Hz. The experiments have been video-recorded to label the data manually. The obtained dataset has been randomly partitioned into two sets, where 70% of the volunteers was selected for generating the training data and 30% the test data.

The sensor signals (accelerometer and gyroscope) were pre-processed by applying noise filters and then sampled in fixed-width sliding windows of 2.56 sec and 50% overlap (128 readings/window). The sensor acceleration signal, which has gravitational and body motion components, was separated using a Butterworth low-pass filter into body acceleration and gravity. The gravitational force is assumed to have only low frequency components, therefore a filter with 0.3 Hz cutoff frequency was used. From each window, a vector of features was obtained by calculating variables from the time and frequency domain

run_analysis.R

Step 1. Merges the training and the test sets to create one data set.

Variables defined and their purpose are given below:

subtest <- read.table("./UCIHAR Dataset/test/subject_test.txt")
xtest <- read.table("./UCIHAR Dataset/test/X_test.txt")
ytest <- read.table("./UCIHAR Dataset/test/Y_test.txt")
subtrain <- read.table("./UCIHAR Dataset/train/subject_train.txt")
xtrain <- read.table("./UCIHAR Dataset/train/X_train.txt")
ytrain <- read.table("./UCIHAR Dataset/train/Y_train.txt")
features <- read.table("./UCIHAR Dataset/features.txt")
activities <- read.table("./UCIHAR Dataset/activity_labels.txt")



Merging the data and train and subject tables using rbind() function.

Coded to perform the other steps mentioned below.

Step 2 :Extracts only the measurements on the mean and standard deviation for each measurement.

Step 3 : Uses descriptive activity names to name the activities in the data set

Step 4 :Appropriately labels the data set with descriptive activity names.

Step 5 :Creates a second, independent tidy data set with the average of each variable for each activity and each subject.

The file SamsungData.txt is created.


Output :

Files are available in the working directory - UCIHAR Dataset

    Samsung_Data.txt

