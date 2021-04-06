# Covid-19-forecasting-using-lstm
The dataset from where I collected information about covid 19 upto November 16, 2020 to customize my own dataset, was from: https://ourworldindata.org/coronavirus-source-data
It is observed that when we take the new cases/ totalnumber cases ratio, as we approach peak, the value varies between 0.01 to 0.08(most of the time the values stays between 0.01 to 0.03) and as the cases decrease this value decreases and again when there in an increase in the number of cases this ratio begins to approach 0.01 to 0.08
Survival analysis
About the dataset:
Finaldataset1: it consists of data from 13 different countries
Location: name of the country
Day: no. of days from which the onset of covid cases was observed 
Avg_new/total: average number of new cases observed in that month by the total number of cases observed since the onset on covid in that country
Growth rate: here, it is calculated by total number of cases observed from the onset of covid in the current monthtotal  number of cases observed from the onset of covid in the previous month1/t-1
Where t=number of days, here 30
Pden:  population density, here countries with population density greater than 100 is cosidered as 1 and countries with population density lesser  than  100 is considered zero
We have used population density to see if it has any statistical significance with the dataset we are using for effective forecasting of covid 19 cases
Status: 1 indicated increase in cases upto the peak and 0 indicates decrease in cases from peak
We are using Cox proportional hazard to check for the hazard ratio of our covariates ie. Growth rate, avg_new/total and pden.
For duration col we are using day column and for event col  we are using status. 

Fig 1
Since the p values of growth rate and avg_total cases is less than 0.005, they are statistically significant.
The hazard ratio(exp(coef)) for growth rate and avg_total cases is greater than 1, which means that the risk in the increase in the number of cases strongly depends on these values.

Fig2
From fig 2, we can visualize the significant difference between growth rate and avg_new/total with confidence interval of 95%

Forecasting Covid-19 using multivariate LSTM
About the dataset:
Indiacases1:  this dataset contains data about covid cases in India upto 16th November, 2020
New_cases: new cases reported everyday
Total_cases: total no. of cases reported on that day since the onset of covid 19 in India
New/total: new_case/ total  cases
Growth rate: here it is calculated by: 
total number of cases observed from the onset of covid in the current daytotal  number of cases observed from the onset of covid in the previous day1/t-1
Where,  ‘t’ is the number of days and here, it is 1.
We are forecasting the no. of new cases per day upto the next 21 days
X: new cases per day, new/total, growth rate, total cases
Y: new cases per day after 21 days
X_train: data upto 257 days
Y_train: new cases per day from day 257 to 279 
X_test: data from day 257 to 279
Y_test: new cases per day from day 279 to 300
Val_loss=0.0416




Means absolute error: 4069.6266082354955
mse: 25426634.559960097

 

