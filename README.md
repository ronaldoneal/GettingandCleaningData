==================================================================
Getting and Cleaning Data
Course Project
==================================================================
Ronald O'Neal
ronaldoneal@yahoo.com

==================================================================

The program performs the following tasks based on the data from experiments that have been carried out with a group of 30 volunteers within an age bracket of 19-48 years. Each person performed six activities (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING) wearing a smartphone (Samsung Galaxy S II) on the waist. Using its embedded accelerometer and gyroscope, we captured 3-axial linear acceleration and 3-axial angular velocity at a constant rate of 50Hz. 

From each window, a vector of features was obtained by calculating variables from the time and frequency domain. See 'features_info.txt' for more details. 

For each record it is provided:
================================================================================================

- An identifier of the subject who carried out the experiment.
- Its activity label.
- Whether the data is a measurement type of "train" or "test" data.
- A 561-feature vector with time and frequency domain variables. 

The dataset includes the following files in the home directory:
================================================================================================

- 'README.md':  Top level application description.

- 'run_analysis.R': R program to process files

- 'run_analysis_code_book.txt': Field definitions

- 'features.txt': List of all features.

- 'activity_labels.txt': Links the class labels with their activity name.

- 'train/X_train.txt': Training set.

- 'train/y_train.txt': Training labels.

- 'test/X_test.txt': Test set.

- 'test/y_test.txt': Test labels.

The following files are available for the train and test data. Their descriptions are equivalent. 

- 'train/subject_train.txt': Each row identifies the subject who performed the activity for each window sample. Its range is from 1 to 30. 

==================

The process followed to complete this data merge is as follows:

  1.  Read features.txt to get the header names for the data table columns
  
  2-a. Read training data into R and merge and sort on SubjectID, ActivityID
    b. Appropriately labels the data set with descriptive variable names (No. 4 below)
    c. Merge on row names (row number) and add variable
    d. Track rows matching between data tables
    e. Merge on row names (row number)
    f. Track rows matching between data tables
  
  3-a. Read test data into R and merge
    b. Appropriately labels the data set with descriptive variable names (No. 4 below)
    c. Merge on row names (row number) and add variable
    d. Track rows matching between data tables
    e. Merge on row names (row number)
    f. Track rows matching between data tables
    
  4. Extracts only the measurements on the mean and standard deviation for each measurement. 
  
  5. Uses descriptive activity names to name the activities in the data set

  6. Appropriately labels the data set with descriptive variable names.
     
     >>> Variable names added just after data load to minimize additional steps to track columns <<<

  7. From the data set in step 6, creates a second, independent tidy data set with the 
     average of each variable for each activity and each subject.

==================


For more information about this dataset contact: activityrecognition@smartlab.ws

License:
========
Use of this dataset in publications must be acknowledged by referencing the following publication [1] 

[1] Davide Anguita, Alessandro Ghio, Luca Oneto, Xavier Parra and Jorge L. Reyes-Ortiz. Human Activity Recognition on Smartphones using a Multiclass Hardware-Friendly Support Vector Machine. International Workshop of Ambient Assisted Living (IWAAL 2012). Vitoria-Gasteiz, Spain. Dec 2012

This dataset is distributed AS-IS and no responsibility implied or explicit can be addressed to the authors or their institutions for its use or misuse. Any commercial use is prohibited.

Jorge L. Reyes-Ortiz, Alessandro Ghio, Luca Oneto, Davide Anguita. November 2012.

