_THE RESEARCH PAPER IN PDF FORMAT ALONG WITH THE PYTHON CODE USED IN THIS STUDY, IS AVAILABLE IN THIS REPOSITORY. IF YOU FIND THIS APPROACH HELPFUL, KINDLY CITE THIS PAPER. CLICK ON THIS LINK TO FIND THE IEEE COPY OF THIS PAPER:_

**Predicting the number of new COVID-19 cases in India using Survival Analysis and LSTM**

Abstract:
COVID-19 has been the cause of death for  thousands of  people across the globe. The goal of this study is to forecast the new COVID-19 cases in India.  The other methods used to forecast COVID-19 cases fail to give results with good accuracy when they try to forecast the number of new cases for a long period of time or when the number of daily cases reported is large since the population of a country is large. In this study we tackle this problem by firstly, customizing our dataset. Secondly, by choosing the suitable covariates using survival analysis and thirdly, feeding the data to the Long Short-Term Memory (LSTM) Network. The data between 30th January, 2020 to 16th June, 2021 was taken to estimate the number of new cases everyday for the next 21 days with a mean absolute percentage error of 5.79%.

Key idea and goal: 
1. It is observed tha the ratio of the new_no_of_cases/total_no_of_cases lies between 0.01 to 0.08 (mostly 0.03) when a country sees a peak in the numberof new cases
2. The above observation helps in generalizing the forecast for all countries irrespective of its population and population density.
3. Though this paper focuses only on India, this approach can be used for other countries as well

