# MechaCar Statistical Analysis

## Linear Regression to Predict MPG
The first statistical analysis performed on this dataset was a linear regression model to predict MPG based on various factors.  The factors that were considered were vehicle length, vehicle weight, spoiler angle, ground clearance, and AWD status.  The results produced utilizing the lm() function are as follows:

![mpg_linear_regression](https://user-images.githubusercontent.com/85641017/135906621-2b820e56-b842-4d58-bcf1-f581ccfa428e.png)

As can be seen in this graphic, vehicle length and ground clearance provide a non-random amount of variance to MPG values as evidenced by their respective Pr values being below the expected significance level of .05%.  Given that the overall p-value for the regression is far below the expected significance of .05%, it can also be determined that there is sufficient evidence to reject the null hypotheses and that the slope of this linear model is not zero. This linear model is effective for predicting information based on this specific dataset, but multiple linear regression models can suffer from overfitting (evidenced by lack of significant variables).  Therefore, beyond this particular dataset, this model may not predict mpg of MechaCar prototypes for future data.

## Summary Statistics on Suspension

