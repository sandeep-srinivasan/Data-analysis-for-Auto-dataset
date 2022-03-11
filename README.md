# Data-analysis-for-Auto-dataset

After creating the binary variable mpg01 and a data frame with the original predictors and the new response, the structure of the modified data set looks like:

![image](https://user-images.githubusercontent.com/42225976/157774448-49612cb8-c7f9-42c8-ac96-9f2e5039f07b.png)

From the summary, it can be seen that there are 304 vehicle names for these 392 observations and the variable name will not be used as a predictor in the following analysis.

![image](https://user-images.githubusercontent.com/42225976/157775442-fcd0848b-ffa1-4fcb-9802-a00d380c2cbb.png)

Based on the boxplots above, cylinder, displacement, horsepower and weight will be most useful in predicting the response mpg01 while acceleration seems to be least useful. The origin of car also shows a sufficient difference between two classes.

Pairwise Scatter Plot Matrix of Predictors is shown below,

![image](https://user-images.githubusercontent.com/42225976/157775557-6e38898d-1def-4c53-b4c0-551aa6a203b9.png)

From the scatterplots, it can be seen that the variables which strongly help in predicting mpg01 are cylinders, displacement, horsepower, weight. The variables which also in predicting mpg01 are acceleration, year and origin.

Linear Discriminant Analysis (LDA), Quadratic Discriminant Analysis (QDA), Logistic Regression model and K-Nearest Neighbors (KNN) are fitted to the dataset and looking at the test error values, KNN with k=7 performs best on the dataset. The test error rate vs the number of neighbors plot is as shown below,

![image](https://user-images.githubusercontent.com/42225976/157776621-808ccfe6-30ea-41be-a748-f05925a01280.png)

For larger values of n, when the limit of (1 - 1/n)^n is applied as n goes to infinity, it can be seen that the value turns out to be approximately equal to exp(-1). So the probability that the jth observation is in the bootstrap sample, whwn n is large is 1 - exp(-1), which is approximately equal to 0.632. That is the reason why a straight line is added with the expression exp(-1) in the plot.
And this reinstates that fact of bootstrap being called 0.632 Bootstrap, since the observation will be in the bootstrap sample 63.2% of the times for large values of n.
