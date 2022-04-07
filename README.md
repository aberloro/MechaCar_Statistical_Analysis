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

## D1: Linear Regression to Predict MPG
 The miles per gallon (mpg) can be predicted by the following linear model:

 mpg =  (6.267)vehicle_length + (0.00125)vehicle_weight + (0.0688)spoiler_angle + (3.546)ground_clearance + (-3.411)AWD - 104.0

![LM_SummaryStats](https://user-images.githubusercontent.com/93740725/162118389-17e9f4bf-b6d1-4fe3-87f1-c6b9e1ba8c68.png)

The above summary statistics tell us about the model's ability to predict mpg:
 - The Pr(>|t|) values show the probability that the coeffecient contributes random variance.  A Pr(>|t|) value below 0.05 indicates that coeffecient is statistically non-random: vehicle length, vechile ground clearance, and the intercept all have statistically significant impact on miles per gallon for this MechaCar prototype.  The significant intercept indicates that additional factors that have not been included in this model also impact mpg. 

 - The p-value is 5.35e-11, much less than the 0.05 threshhold where we would accept the null hypothesis. We therefor accept the alternate hypothesis: the slope of the linear model is not zero. 

 - This linear model effectively predicts the miles per gallon of the MechaCar prototype because the r-squared value is "strong" at over 0.7.  

## D2: Summary Statistics on Suspension Coils

Looking at the total summary of all lots collectively, the variance of 62.29 does *not* exceed 100 PSI:

![coils_total_summary](https://user-images.githubusercontent.com/93740725/162118430-7ae3defa-a472-4175-8535-048c589fe6b5.png)


Looking at the summary stats per lot: Lots 1 and 2 are within the design specs at only 0.98 and 7.47 respectively.  Lot 3 has a variance of over 170 and therefore exceeds the limit of 100 PSI:

![coils_lot_summary](https://user-images.githubusercontent.com/93740725/162118456-edf28509-ba26-4be0-9eda-7b11f5b46f8a.png)


## D3: T-Tests on Sespension Coils

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

A t-Test p-value of 0.042 tells us to *reject* the null hypothesis.  There *is* a statistical difference between the PSI of Lot3 mean of 1496.14 and the population mean of 1500. 


## D4: Study Design: MechaCar vs Competition
When it comes to an individual or family car, needs change over time.  The car that got you to and from class in highschool and college might need an update once you land that first data analysis job. That small sporty car might be less attractive than a larger and safer SUV after you have children.  Now your teens want to go camping, you'll need something with some off-road ability as well.  Your kids have kids and are now spread all over the country?...Might be time for an RV!

Your ability to upgrade vehicles as life's demands change will be impacted by your vehicle's resale value.  This proposed study will examine how the MechaCar's **resale value** holds up against the competition. 

This study will require 2 phases: Phase 1 will create a multiple linear regression model to predict the resale of the prototype based on resale values of other MechaCar Models in the same vehicle category.  Phase 2 will
compare the MechaCar prototype resale value against the competition.  

### Phase 1: Predict Resale Value

#### Phase 1 Metrics to be Tested
 - Dependent Variable: resale value
 - Independent Variables: safety rating, fuel economy, new-sale price, mileage, life time maintanance costs, condition of vehicle

#### Phase 1 Hypotheses 
The null hypothesis H<sub>01</sub>: The slope of the linear model is zero. 

The alternate hypotheses H<sub>a1</sub>: The slope of the linear model is not zero. 

#### Phase 1 Statistical Test
Multiple Linear Regression

#### Phase 1 Data
The linear regression model will require resale values of other MechaCar Models in the same vehicle class, assuming good condition, as well as the mileage, safety rating, fuel economy, new-sale price, and lifetime maintenance costs for each vehicle. 

If the null hypothesis is rejected and we find the slope of the linear regression model *is not* equal to zero, then we can proceed to Phase 2 of the study.

### Phase 2: Compare MechaCar Resale Value to the Competition

#### Phase 2 Metrics to be Tested
 - Predicted resale value for MechaCar prototype, assuming good condition.
 - Available resale value for the competition, also assuming good condition. 

#### Phase 2 Hypotheses 
The null hypothesis H<sub>02</sub>: The MechaCar prototype's resale value is *not() statistically different from the resale value of the competition.

The alternate hypotheses H<sub>a2</sub>: The MechaCar prototype's resale value *is* statistically different from the resale value of the competition.

#### Phase 2 Statistical Test
Two-Sample t-Test

#### Phase 2 Data
The 2-Sample t-Test will require the predicted resale value of the MechaCar prototype as well as available resale data of the competition, other factors such as mileage and condition held equal. 

