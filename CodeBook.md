Data in:
features.txt 
activity_labels.txt
test/subject_test.txt
test/X_test.txt
test/y_test.txt
train/subject_train.txt
train/X_train.txt
train/y_train.txt
Data out:
clean_data.txt
features include different measured variables from the Human Activity Recognition Using Smartphones Data Set 
For each record in the dataset it is provided: 
- Triaxial acceleration from the accelerometer (total acceleration) and the estimated body acceleration. 
- Triaxial Angular velocity from the gyroscope. 
- A 561-feature vector with time and frequency domain variables. 
- Its activity label. 
- An identifier of the subject who carried out the experiment.
activity_labels is the catalog with the 6 different activities 
1 WALKING
2 WALKING_UPSTAIRS
3 WALKING_DOWNSTAIRS
4 SITTING
5 STANDING
6 LAYING
both files used for adding variables names or identifying ID's.

subject_test and subject_train include id's of the tested subjects used to identify the data with each different user.

Y_train and Y_test include the ID of each activity for each subject to know wich activity was he realizing in each measure

X_train and X_test include all the differente measures of the data for each subject.

the data with Id's where identified and asociated with the activity of each.
the subjects where joined with the activity they where doing and with all the measures provided and all of the variables where named befoere getting them into the output file.
