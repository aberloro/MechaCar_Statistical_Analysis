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
 - Data Sources: [MechaCar_mpg.csv](https://github.com/aberloro/MechaCar_Statistical_Analysis/blob/main/MechaCar_mpg.csv), [Suspension_Coil.csv](https://github.com/aberloro/MechaCar_Statistical_Analysis/blob/main/Suspension_Coil.csv)
 - Technology: R, RStudio

## Linear Regression to Predict MPG
 The miles per gallon (mpg) can be predicted by the following linear model:

 mpg =  (6.267)vehicle_length + (0.00125)vehicle_weight + (0.0688)spoiler_angle + (3.546)ground_clearance + (-3.411)AWD - 104.0

![LM_SummaryStats](https://user-images.githubusercontent.com/93740725/162118389-17e9f4bf-b6d1-4fe3-87f1-c6b9e1ba8c68.png)

The above summary statistics tell us about the model's ability to predict mpg:
 - The Pr(>|t|) values show the probability that the coeffecient contributes random variance.  A Pr(>|t|) value below 0.05 indicates that coeffecient is statistically non-random: vehicle length, vechile ground clearance, and the intercept all have statistically significant impact on miles per gallon for this MechaCar prototype.  The significant intercept indicates that additional factors that have not been included in this model also impact mpg. 

 - The p-value is 5.35e-11, much less than the 0.05 threshhold where we would accept the null hypothesis. We therefor accept the alternate hypothesis: the slope of the linear model is not zero. 

 - This linear model effectively predicts the miles per gallon of the MechaCar prototype because the r-squared value is "strong" at over 0.7.  

## Summary Statistics on Suspension Coils

Looking at the total summary of all lots collectively, the variance of 62.29 does *not* exceed 100 PSI:
![coils_total_summary](https://user-images.githubusercontent.com/93740725/162118430-7ae3defa-a472-4175-8535-048c589fe6b5.png)


Looking at the summary stats per lot: Lots 1 and 2 are within the design specs at only 0.98 and 7.47 respectively.  Lot 3 has a variance of over 170 and therefore exceeds the limit of 100 PSI:
![coils_lot_summary](https://user-images.githubusercontent.com/93740725/162118456-edf28509-ba26-4be0-9eda-7b11f5b46f8a.png)


## T-Tests on Sespension Coils

### All Lots
![t-TestAll](https://user-images.githubusercontent.com/93740725/162118472-43fc3a7d-a730-4430-98e7-8d8db69c38cc.png)

A t-Test p-value of 0.060 tells us to *accept* the null hypothesis that there is no statistical difference between the PSI of all Lots and the population mean of 1500.  

### Lot 1
![t-TestLot1](https://user-images.githubusercontent.com/93740725/162118495-79de9fc3-fad7-43f6-8fe2-49cc5372eafa.png)

A t-Test p-value of 1 tells us to *accept* the null hypothesis that there is no statistical difference between the PSI of Lot1 and the population mean of 1500. 

### Lot 2
![t-TestLot2](https://user-images.githubusercontent.com/93740725/162118530-a39ecc0c-e6d9-48c0-b757-2c8c392e2603.png)

A t-Test p-value of 0.61 tells us to *accept* the null hypothesis that there is no statistical difference between the PSI of Lot2 and the population mean of 1500. 

### Lot 3
![t-TestLot3](https://user-images.githubusercontent.com/93740725/162118558-7a3c6986-e343-4ab9-9d51-3bfb6961f462.png)

A t-Test p-value of 0.042 tells us to *reject* the null hypothesis.  There is a statistical difference between the PSI of Lot3 mean of 1496.14 and the population mean of 1500. 


## Study Design: MechaCar vs Competition

