# MechaCar Statistical Analysis

## Linear Regression to Predict MPG
The first statistical analysis performed on this dataset was a linear regression model to predict MPG based on various factors.  The factors that were considered were vehicle length, vehicle weight, spoiler angle, ground clearance, and AWD status.  The results produced utilizing the lm() function are as follows:

![mpg_linear_regression](https://user-images.githubusercontent.com/85641017/135906621-2b820e56-b842-4d58-bcf1-f581ccfa428e.png)

As can be seen in this graphic, vehicle length and ground clearance provide a non-random amount of variance to MPG values as evidenced by their respective Pr values being below the expected significance level of .05%.  Given that the overall p-value for the regression is far below the expected significance of .05%, it can also be determined that there is sufficient evidence to reject the null hypotheses and that the slope of this linear model is not zero. This linear model is effective for predicting information based on this specific dataset, but multiple linear regression models can suffer from overfitting (evidenced by lack of significant variables).  Therefore, beyond this particular dataset, this model may not predict mpg of MechaCar prototypes for future data.

## Summary Statistics on Suspension
The second statistical analysis performed was based on the suspension coil information provided for the MechaCar prototypes.  For this analysis we completed summary analyses of the PSI for the suspension coils in the dataset both for the entire dataset as well as grouping them by manufacturing lots.  The summary analsysis performed on the entire dataset produced the following results:

![total_summary](https://user-images.githubusercontent.com/85641017/135912879-ad2b7662-fe6f-4767-a335-9f7deaaa0812.png)

The summary statistics grouped by manufacturing lot produced the following results:

![lot_summary](https://user-images.githubusercontent.com/85641017/135913018-701d54c5-8151-402d-a5f3-fa0f304256d3.png)

It has been determined that the design specifications for the MechaCar suspension coils dictate that the variance of the coils must not exceed 100 PSI.  If we look at the overall summary for the suspension coils dataset, this requirement is met (Variance = 62.29).  However, when the coils were grouped by manufacturing lot, a concerning result was discovered with Manufacturing Lot 3 showing a variance that well exceeds the design specifications (Variance = 170.286).  Further analysis will be required on Manufacutring Lot 3 to isolate the specific coils that are not within design specification, identify the root cause for the unacceptable variance, and make the necessary changes before those coils can be placed into production.

## T-Tests on Suspension Coils
For the third statistical analysis performed on the given data, four separate t-tests were performed to analyize the PSI data and compare it to the population mean.  The first t-test was performed across all manufacturing lots to determine if the PSI was statistically different from a population mean of 1500 PSI.  
![t-test for all lots](https://user-images.githubusercontent.com/85641017/135920018-49080833-3b9c-409d-9b78-ab781610b7a1.png)

This test shows a p-value of .06028 which would be higher than the anticipated .05% significance rate.  Therefore, there is not sufficient evidence to reject the null hypothesis in this scenario and it can be determined that the true mean is not statistically significantly different from 15000. 

The second t-test was performed on a subset focused on only those coils associated with manufacturing lot 1.  
![t-test for lot 1](https://user-images.githubusercontent.com/85641017/135921034-40f305be-1a14-4a27-937b-15870b206972.png)

Similar to the t-test for the whole dataset, the p-value for this test shows a value of 1 thereby also indicating that there is not sufficient evidence to reject the null hypothesis and that the true mean is not statistically different from 1500.

The third t-test was performed on a subset focused on only those coils associated with manufacturing lot 2.
![t-test for lot 2](https://user-images.githubusercontent.com/85641017/135922372-26d7aaa6-ecdf-4586-9049-b2ba93d13582.png)

While the p-value for this test is lower than the previous two, it also shows a score that is higher than the anticipated statistical significance of .05%.  As with the previous 2 tests, the null hypothesis cannot be rejected in this case and it can be assumed that the true mean is not statistically different from 1500.

The fourth t-test was performed on a subset focused only on those coils associated with manufacturing lot 3.
![t-test for lot 3](https://user-images.githubusercontent.com/85641017/135922608-90dd39e9-344a-408d-9100-e18be8d27768.png)

This test diverges from the previous three due to the fact that the p-value is lower than the anticipated statistical significance of .05%.  Unlike the previous tests, the null hypothesis would be rejected and the alternative hypothesis of "true mean is not equal to 1500" would be accepted.

##  Study Design: MechaCar vs Competition
In order to make MechaCar more appealing to the market, it would be beneficial to determine some key metrics where MechaCar outperforms the competition.  Three primary metrics that the typcial consumer may look at would be:  initial cost of the vehicle, ongoing maintenance cost of the vehicle, and general fuel efficiency of the vehicle.  The comparison between MechaCar and identified competitors would all be based on a Null Hypotheses of:  There is no statistically significant difference between the average values of the given category, and an Alternate Hypothesis of:  There is a statistically significant difference between the average values of the given category.  To start, a sample dataset would bet obtained in two separate files:  one for MechaCar and the other for the competitor.  Each dataset will contain data gathered from various points around the country and will include the cost of the car, the cost of annual manintenance for the car, and the average fuel efficience (between highway and city) for the car.  Once this has been obtained, summary statistics will then be performed on each dataset to obtain the Mean value for each of the given categories.  Once the averages are obtained, then t-tests can be performed to determine the statistical difference between the two groups based on the given category.  This information can then be presented so as to demonstrate how the MechaCar performs compared to the competition.  
