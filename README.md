# MechaCar_Statistical_Analysis

## Overview of Project

### Purpose
Production troubles are blocking progress on the MechaCar prototype. An analysis of  production data is needed to provide insights that might be helpful to the manufacturing team. 

### Deliverables
 - Liner Regression to Predict MPG
 - Summary Staatistics on Suspension Coils
 - T-Test on Suspension Coils
 - Study Comparing MechaCar to the Competition
 
### Resources
 - Data Sources: MechaCar_MPG_dataset, Suspension_Coil_dataset
 - Technology: R, RStudio

## Linear Regression to Predict MPG
 The miles per gallon (mpg) can be predicted by the following linear model:

 mpg =  (6.267)vehicle_length + (0.00125)vehicle_weight + (0.0688)spoiler_angle + (3.546)ground_clearance + (-3.411)AWD - 104.0

 --- insert LM_SummaryStats Image ----

The above summary statistics tell us about the model's ability to predict mpg:
 - The Pr(>|t|) values show the probability that the coeffecient contributes random variance.  A Pr(>|t|) value below 0.05 mean that coeffecient is statistically non-random: vehicle length, vechile ground clearance, and the intercept all have statistically significant impact on miles per gallon for this MechaCar prototype.  

 - The p-value is 5.35e-11, much less than the 0.05 threshhold where we would accept the null hypothesis. We therefor accept the alternate hypothesis: the slope of the linear model is not zero. 

 - This linear model effectively predicts the miles per gallon of the MechaCar prototype because the r-squared value is "strong" at over 0.7.  

## Summary Statistics on Suspension Coils

--- insert coils_total_summary.png ---
Looking at the total summary of all lots collectively, the variance of 62.29 does *not* exceed 100 PSI.  

--- insert coils_lot_summary.png ---
Looking at the summary stats per lot: Lots 1 and 2 are within the design specs at only 0.98 and 7.47 respectively.  Lot 3 has a variance of over 170 and therefore exceeds the limit of 100 PSI. 


## T-Tests on Sespension COils

## Study Design: MechaCar vs Competition

