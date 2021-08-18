# public-health-analysis
Linear Regression in R for Public Health
course - 
https://www.coursera.org/learn/linear-regression-r-public-health/home/welcome


Problem statement - 
predict -  walking distance

walking ability(patient can walk in 6 min) - MWT1(reading 1), MWT2(reading 2) , MWT1Best (best of 2 reading)

Predictive variables - 
Lung function - FEV1 (predict lung function)
and AGE

---------------------------
Explore how to fit a multiple regression model in R, to quantify the relationship between the lung function (FEV1), age, and walking distance (MWT1Best) in COPD patients. 

The basic format of a multiple linear regression is: 

Y = α + β1*X1 + β2*X2 + ε 

Where: 

Y = outcome (i.e. dependent) variable. 

X1 = first predictor (i.e. independent) variable. 

X2 = second predictor (i.e. independent) variable. 

α = intercept (average Y when X1=X2=0). Note: α is unit specific. 

β1 = slope of the line (change in Y for a 1 unit increase in X1 when X2 is held constant). Note: β1 is unit specific. 

Β2 = slope of the line (change in Y for a 1 unit increase in X2 when X1 is held constant). Note: β2 is unit specific. 

ε is the random variation in Y, i.e. the residuals. 

To run a multiple linear regression in R, the basic format of the function is very similar to that of a simple linear regression – the only difference is that you are adding two predictor variables instead of one: 

Model name <- lm(outcome ~ predictor1 + predictor2, data =dataframe) 

So, for example, if you want to run a multiple linear regression to check whether lung function and age are predictors of walking distance in COPD patients, the R command is: 

MWT1Best_FEV1_AGE <- lm(MWT1Best~FEV1+AGE, data = COPD) 

where: 

MWT1Best_FEV1_AGE is the name of our model 

MWT1Best is the outcome variable 

FEV1 is the first predictor variable 

AGE is the second predictor variable 


