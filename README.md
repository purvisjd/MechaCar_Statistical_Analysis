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


