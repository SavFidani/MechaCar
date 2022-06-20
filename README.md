# MechaCar

## Linear Regression to Predict MPG

In order to analyze the impacts of our variables, we were looking to format a regression of the following form:

mpg = ⍺ + βvehicle_length + βvehicle_weight + βspoiler_angle + βground_clearance + βAWD + 𝓊

where...
⍺ = our y-intercept
β = our independent variable coefficients 
𝓊 = the error term

Upon an initial analysis of the relationship between our variables we discover the following coefficients:

<img width="757" alt="Screen Shot 2022-06-19 at 8 54 47 PM" src="https://user-images.githubusercontent.com/99772755/174511838-e950f61c-77e9-43b7-a4de-21133583cc9f.png">

The primary question of interest here, is which variables of the above actually present statistical significance to our regression. The below image answers this question. 

<img width="477" alt="Screen Shot 2022-06-19 at 8 54 23 PM" src="https://user-images.githubusercontent.com/99772755/174512000-91066d98-2186-417d-b924-8333943a7675.png">

As indicated by *** our y-intercept, vehicle_length, and ground_clearance values are statistically significant. This means that statistically, they are unlikely to provide random amounts of variance to the linear model. For this reason, the slope of this model is not considered to be 0. When each other independent variable is equal to 0, these attributes will impact the observed trajectory of the mpg. 

Although we have found some statistically significant relationships, at this point in time the linear regression is still not accurate. As defined by our error term, 𝓊, the model has not yet been adjusted for bias, or tested for autoskedasticity & heteroskedasticity meaning we cannot guarantee accuracy. 

## Summary Statistics on Suspension Coils

"The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch."

To address the above specification in a clear and concise manner, the current manufacturing data does not meet this design specification for all manufacturing lots individually, but when observed together the requirement is met.

Please see below:
<img width="468" alt="Screen Shot 2022-06-19 at 10 03 54 PM" src="https://user-images.githubusercontent.com/99772755/174512835-ca0c3b19-3371-4fa0-ad88-0a8146023ba7.png">

The requirement is that variance < 100. When looking at the variance of each lot individually, we see lot 3 has a variance > 100 (170) therefore it does not meet the specifications.

When observing all 3 lots from an aggregate macro level, their combined variance does meet the specifications as indicated below:
<img width="332" alt="Screen Shot 2022-06-19 at 9 19 11 PM" src="https://user-images.githubusercontent.com/99772755/174512953-5fe3ac24-1c01-473d-b433-657a7d06ae7a.png">

## T-Tests on Suspension Coils

Upon running a t-test - assuming conditions of a 95% confidence interval - we would fail to reject the null hypothesis. Given that the absolute value of our t-statistic is < 0.05, we fail to reject the null. Please see below for our output results:

<img width="431" alt="Screen Shot 2022-06-19 at 9 32 15 PM" src="https://user-images.githubusercontent.com/99772755/174513426-a575ae81-5b20-4cbb-ab3d-e0187d24493a.png">

## Study Design: MechaCar vs Competition

When it comes to understanding whether you have the superior product, there are a few metrics of interest to your consumers that may prove to be useful in an analysis of your standing in comparison to your competition. Let's work under the assumption that our consumers value quality. To evaluate quality, we are going to analyze the metric of maintenance costs of our product versus the competitor. We will structure our analysis as follows:

H0: Our product has lower annual maintenance costs than the competitor.
H1: The opposite is true. 

H0 is rejected if the opposite is supported within a 95% confidence index (r = 0.05).

To analyze the above hypothesis, we would be running a two-sample t-test at the 95% confidence index. This is because we are looking to identify whether there is a statistical differencebetween the distribution means from multiple samples (maintenance costs of our cars versus the competitors). 

Ideal data would be an aggregation of all work completed on comparable models of cars from both brands, not for aesthetic purposes, but for operational and safety intentions. These costs can then be aggregated and compared to find the superior quality product. It is important to note, that simply looking at the cost presents biases and limitations. For instance, how does one define if costs caused by an accident are accounted for. Was the accident caused by mechanical failure of the product, or user failure. Furthermore, adjustments for frequency of use will need to be made. Especially in the presence of the pandemic and new work from home structures, some consumers drive significantly less frequently than others. 

These are just a glimpse of limitations that will potentially be faced; however, preliminary findings may be able to provide a general overview into the more successful and desireable product. 

