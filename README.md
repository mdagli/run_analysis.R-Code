
DESCRIPTION of FUNCTION
(this is best described on the annotated function text)

The first part of the function will read in the various files using read.table.  
It assumes that the files are within the working directory. It only reads in the necessary files. 
It ignores the files in the Inertial Signals folders as these do not appear to be necesssary for the assignment. That being said
I am not clear what they are doing in this experiment. 

This next part of the function will label the column names.  The acquired data is relabelled to make it more understandable.  
The next part of the function will merge the testing  and training data using cbind and rbind
It will then subset the relevant mean and data columns. Because the assignment does not specify, I choose only a small subset of 
possible columns in order to make it more manageable. 
The Function then recodes the activity variables from numbers to more explanatory variables. 

The next part of the function requires installation of the dplyr package.  
These can be installed with 
install.packages("dplyr”)  library(dplyr)  }  

It will group the data by subject and activity
It then computes the means of each variable segregated by the thirty subject and six activity. 
The function then returns the dataset in the variable "meanresults"

CODEBOOK FOR THE RETURNED MEANRESULTS DATA SET

The experiments have been carried out with a group of 30 volunteers within an age bracket of 19-48 years.
Each person performed six activities (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING) wearing a 
smartphone (Samsung Galaxy S II) on the waist. Using its embedded accelerometer and gyroscope, 
we captured 3-axial linear acceleration and 3-axial angular velocity at a constant rate of 50Hz. The experiments have 
been video-recorded to label the data manually. The obtained dataset has been randomly 
partitioned into two sets, where 70% of the volunteers was selected for generating the training data and 30% the test data. These
data sets were merged for this analysis. 


1. "subject"  -  The subject of interest from 1-30
2. "activity" - The activity of interest. Categories:  WALKING , WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING
3. "avgmeanbodyaccelerationXdir":  average mean body acceration in X direction. units 'g'
4. "avgmeanbodyaccelerationydir" : average mean body acceration in Y direction. units 'g'
5. "avgmeanbodyaccelerationZdir" : average mean body acceration in X direction. units 'g'
6. "avgstddevbodyaccelerationXdir" :average standard deviation of body acceration in X direction. units 'g'
7. "avgstddevbodyaccelerationYdir" : average standard deviation of body acceration in Y direction. units 'g' 
8. "avgstddevbodyaccelerationZdir" : average standard deviation of body acceration in Z direction. units 'g'
9. "avgmeanGravityaccerationXdir" :  average mean of gravity acceration in X direction. units 'g'
10. "avgmeanGravityaccerationYdir" : average mean  of gravity acceration in Y direction. units 'g'
11. "avgmeanGravityaccerationZdir" : average mean of gravity acceration in Z direction. units 'g'
12. "avgSTDGravityaccerationXdir" :  average standard deviation of gravity acceration in X direction. units 'g'
13. "avgSTDGravityaccerationYdir" : average standard deviation of gravity acceration in Y direction. units 'g'
14. "avgSTDGravityaccerationZdir") : average standard deviation of gravity acceration in Z direction. units 'g'






