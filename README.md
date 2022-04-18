# MechaCar Statistical Analysis
## Overview
AutosRUs’ newest prototype, the MechaCar, is suffering from production troubles that are blocking the manufacturing team’s progress. AutosRUs’ upper management has called on Jeremy and the data analytics team to review the production data for insights that may help the manufacturing team.

Help Jeremy and the data analytics team do the following:
  - Perform multiple linear regression analysis to identify which variables in the dataset predict the mpg of MechaCar prototypes
  - Collect summary statistics on the pounds per square inch (PSI) of the suspension coils from the manufacturing lots
  - Run t-tests to determine if the manufacturing lots are statistically different from the mean population
  - Design a statistical study to compare vehicle performance of the MechaCar vehicles against    vehicles from other manufacturers. For each statistical analysis, you’ll write a summary  interpretation of the findings.
## Results
### Linear Regression to Predict MPG
![lm](https://user-images.githubusercontent.com/59906657/163736188-47f7fd0c-25a9-4533-af5c-e4d8216481ab.PNG)
![lm_summary](https://user-images.githubusercontent.com/59906657/163736192-938049f3-7a57-4d7c-8769-22acaab8c00f.PNG)
1. The variables and coefficients that provided a non-random amount of variance to the mpg values in the dataset if using the standard level of significance value of 0.05 are:  intercept, vehicle length, and ground clearance.
2. The slope is not considered zero because each of the variable coefficients are not close enough to zero and several p-values are significantly low making it less likely the slope is zero.
3. It depends on the level of accuracy needed.  The r-squared value of 71.49% is good because that percentage of the data fit the model, but adding or removing some variables may help increase the fit.
### Summary Statistics on Suspension Coils
![summarize](https://user-images.githubusercontent.com/59906657/163737770-b8bc3b0a-8f42-422f-9f4a-25d62a8b5c9b.PNG)
![lot_summarize](https://user-images.githubusercontent.com/59906657/163737773-b547a849-f43e-424d-b33e-f6816ce7308f.PNG)  

When viewing the total summary the variance is 62.29 lbs which is within the design specifications.  However, when breaking it down by lots, Lot 3 is way above acceptable limits at 170.29 lbs.  It would be best to investigate why Lot 3 is so much higher than one (.98) and two (7.47) before approving the design specifications.  
### T-Tests on Suspension Coils
![t_test](https://user-images.githubusercontent.com/59906657/163738072-28694fe1-63af-48d4-b0ec-6e004959668f.PNG)  
![t_test_subset](https://user-images.githubusercontent.com/59906657/163738078-8a5cfe80-6787-4031-83e8-c08c3120afee.PNG)  
The mean PSI for the sample is 1498.78 which is not equal to 1500.  The p-value is above 0.05 meaning the null hypothesis cannot be rejected.  The means for lots one and two were not significantly different from the mean of 1500, and the p-values for each are above the 0.05 significance level.  However, lot 3 shows enough difference and a p-value below the significance level with a 0.04.

## Study Design: MechaCar vs Competition
Due to high gas prices in the current economy, many consumers would be very interested how MechaCar compares to their competition in City/Highway fuel efficiency.  The metrics that would be needed are City miles-per-gallon and Highway miles-per-gallon for each vehicle.  The data needs to be collected in a controlled environment such as a testing track to limit outside interference as much as possible.  This data should be collected from several runs through each kind of track.  The null hypothesis would be that there is no significant diffence in City/Highway MPG between MechaCar and the competition.  The alternative hypothesis is that MechaCar has a significantly better City/Highway MPG than the competition.  To determine this, a t-test can be performed on both City and Highway and each seperately compared against the competition's ratings.  A significance level of 0.05 will be used.
