CodeBook for the tidy dataset
Data source

This dataset is derived from the "Human Activity Recognition Using Smartphones Data Set" which was originally 
made avaiable here: http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones

Feature Selection

The features selected for this database come from the accelerometer and gyroscope 3-axial raw signals timeAcc-XYZ 
and timeGyro-XYZ. These time domain signals were captured at a constant rate of 50 Hz. 
Then they were filtered using a median filter and a 3rd order low pass Butterworth filter with a corner frequency 
of 20 Hz to remove noise. Similarly, the acceleration signal was then separated into body and gravity acceleration 
signals (timeBodyAcc-XYZ and timeGravityAcc-XYZ) using another low pass Butterworth filter with a corner frequency of 0.3 Hz.

Subsequently, the body linear acceleration and angular velocity were derived in time to obtain Jerk signals 
(tBodyAccJerk-XYZ and tBodyGyroJerk-XYZ). Also the magnitude of these three-dimensional signals were calculated 
using the Euclidean norm (timeBodyAccMagnitude, timeGravityAccMagnitude, timeBodyAccJerkMagnitude, 
timeBodyGyroMagnitude, timeBodyGyroJerkMagnitudes).

Finally a Fast Fourier Transform (FFT) was applied to some of these signals producing freqBodyAccMagnitude, 
freqBodyAccJerkMagnitude, freqBodyGyroMagnitude, freqBodyGyroJerkMagnitude.

Variables
Identification variables
"activityId"	  "subjectId"
Categorical variables
"activityType"
variables measured in units of time
"timeBodyAccMagnitudeMean"     	"timeBodyAccMagnitudeStdDev"	
"timeGravityAccMagnitudeMean"	  "timeGravityAccMagnitudeStdDev"	
"timeBodyAccJerkMagnitudeMean"	"timeBodyAccJerkMagnitudeStdDev"	
"timeBodyGyroMagnitudeMean"	    "timeBodyGyroMagnitudeStdDev"	
"timeBodyGyroJerkMagnitudeMean"	"timeBodyGyroJerkMagnitudeStdDev"	
variables measured in units of frequency
"freqBodyAccMagnitudeMean"      "freqBodyAccMagnitudeStdDev"	
"freqBodyAccJerkMagnitudeMean"	"freqBodyAccJerkMagnitudeStdDev"
"freqBodyGyroMagnitudeMean"	    "freqBodyGyroMagnitudeStdDev"	
"freqBodyGyroJerkMagnitudeMean"	"freqBodyGyroJerkMagnitudeStdDev"	

abbreviations
    Mean: Mean value
    StdDev: Standard deviation



Overview DATASET
Section 1. Merge the training and the test sets to create one data set.
After setting the source directory for the files, read into tables the data located in
    features.txt
    activity_labels.txt
    subject_train.txt
    x_train.txt
    y_train.txt
    subject_test.txt
    x_test.txt
    y_test.txt
Assign column names and merge to create one data set.
Section 2. Extract only the measurements on the mean and standard deviation for each measurement.Create 
a local vector that contains TRUE values for the ID, mean and stdev columns and FALSE values for the others. 
Subset this data to keep only the necessary columns.
Section 3. Use descriptive activity names to name the activities in the data set
Merge data subset with the activityType table to cinlude the descriptive activity names
Section 4. Appropriately label the data set with descriptive activity names.
Use gsub function for pattern replacement to clean up the data labels.
Section 5. Create a second, independent tidy data set with the average of each variable for each activity 
and each subject.
