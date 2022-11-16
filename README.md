# Medical-Claims-Analysis

### Overview of Project
#### Purpose
The goal of this project is to look deeper into my weight lifting data over the course of 4 months, hopefully finding some evidence of progress! This data was recorded in an Excel sheet populated with my training program. Naturally as a powerlifter, this program focuses on squat, bench, and deadlift with assesory movement to supplement these lifts. Data was taken from these main lifts (Squat, Bench, Deadlift), specifically: weight lifted, repititions completed, sets completed, rate of perceived exhaustion, and date completed. This data is also split into 2 different training programs. This data was extracted, organized, and cleaned before beginning to dig into the data.

### Analysis
To better understand the data, the number of each lift day, total number of training days, percent of days trained, and average days between each lift day were found first. The average increase in weight per week and standard deviation was calculated for each lift per program. A t-test was going to be run on the changes in weight / week to determine if the average weight increase per week was not significantly different between lifts, however, a Kolmogorov-Smirnov test determined that the data was not normally distributed.

Scatter plots of weight lifted over time were created per each lift to observe the relationship between weight and time. Plots were shaded per program. To investigate the relationship between the weights lifted per week and the volume complete (volume = sets x reps, volue has an inverse relationship with weight), scatter plots were created with volume and weight on the y-axes and time on the x-axis. Finally, to determine the linearity of the relationship between time and weight lifted, linear regressions were calculated and plotted for each lift. 

### Results
#### First look into the data:
Inpatient claims data size: (66773, 81)
Outpatient claims data size: (790790, 76)
Beneficiary claims data size: (116352, 32)




### Discussion
Which program resulted in a higher weight increase / week?
Looking at the data, the sample size was rather small unfortunately. There were only 3, 4, and 3 deadlift, squat, and bench training days recorded in program 2. Thus it was unlikely to get accurate comparisons between program 1 and program 2. However, the average weight increase / week was higher in program 1 for all lifts. This may have been due to cofounding variables; strength increases very quickly initially followed by a slow in progression. 

Is there a relationship between volume and weight used?
The inverse relationship between weight and volume is clearly seen in program 1. Program 2 maintained the same volume and weight throughout. In practical terms, this means program 2 is more exhaustive than program 1 and will lead to strength fatigue faster. If continuing with program 2, some time should be taken with lower volume to avoid this. 

What's next?
I would like to collect more data points for program 2 and compare the progress seen in programs 1 and 2. Furthermore, it would be interesting to look at accessory lifts to find any correlations betweent those lifts and the main lifts. If correlations are found, these accessory lifts would be the best choice to optimize strength increases in the main lifts. 
