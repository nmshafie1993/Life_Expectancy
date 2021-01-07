# Statistical Analysis on factors influencing Life Expectancy
## Project Goal
In this project, we are investigating the factors that are impacting the life expectency in 193 countries. We aim to develope a model that can predict the life expectancy using regression.  
<img src="https://github.com/nmshafie1993/Life_Expectancy/blob/master/images/1.png">
## Data Source:
This dataset has been obtained from the Kaggle Website : https://www.kaggle.com/kumarajarshi/life-expectancy-who <br>
Note from the Kaggle Website : The data was collected from WHO and United Nations website with the help of Deeksha Russell and Duan Wang.<br>
## Data Description:
The project relies on accuracy of data. The Global Health Observatory (GHO) data repository under World Health Organization (WHO) keeps track of the health status as well as many other related factors for all countries The data-sets are made available to public for the purpose of health data analysis. The data-set related to life expectancy, health factors for 193 countries has been collected from the same WHO data repository website and its corresponding economic data was collected from United Nation website. Among all categories of health-related factors only those critical factors were chosen which are more representative. <br>
|Field|Description|
|---:|:---|
|Country|Country|
|Year|Year|
|Status|Developed or Developing status|
|Life expectancy|Life Expectancy in age|
|Adult Mortality|Adult Mortality Rates of both sexes (probability of dying between 15 and 60 years per 1000 population)|
|infant deaths|Number of Infant Deaths per 1000 population|
|Alcohol|Alcohol, recorded per capita (15+) consumption (in litres of pure alcohol)|
|percentage expenditure|Expenditure on health as a percene of Gross Domestic Product per capita(%)|
|Hepatitis B|Hepatitis B (HepB) immunization coverage among 1-year-olds (%)|
|Measles|Measles - number of reported cases per 1000 population|
|BMI|Average Body Mass Index of entire population|
|under-five deaths|Number of under-five deaths per 1000 population|
|Polio|Polio (Pol3) immunization coverage among 1-year-olds (%)|
|Total expenditure|General government expenditure on health as a percene of total government expenditure (%)|
|Diphtheria|Diphtheria tetanus toxoid and pertussis (DTP3) immunization coverage among 1-year-olds (%)|
|HIV/AIDS|Deaths per 1 000 live births HIV/AIDS (0-4 years)|
|GDP|Gross Domestic Product per capita (in USD)|
|Population|Population of the country|
|thinness 1-19 years|Prevalence of thinness among children and adolescents for Age 10 to 19 (%)|
|thinness 5-9 years|Prevalence of thinness among children for Age 5 to 9(%)|
|Income composition of resources|Income composition of resources|
|Schooling|Number of years of Schooling(years)|
## Results
Let's briefly review our findings from exploratory data analysis:<br>
1. One of the most important finding is that in general life expectancy is increasing.
<img src="https://github.com/nmshafie1993/Life_Expectancy/blob/master/images/5.png">
2. Below image shows the correlation between the factors that are influencing the life expectancy:<br>
<img src="https://github.com/nmshafie1993/Life_Expectancy/blob/master/images/4.png">
3. To have a better understanding, Let's see the distribution of our column variables. <br>
<img src="https://github.com/nmshafie1993/Life_Expectancy/blob/master/images/2.png">
4. We also detect outliers... <br>
<img src="https://github.com/nmshafie1993/Life_Expectancy/blob/master/images/3.png"> <br>
5. We were able to model our data using linear regression. Here is our result:
<img src="https://github.com/nmshafie1993/Life_Expectancy/blob/master/images/Capture.png">
## Conclusion
Looking at R-quared and Adj. R-squared, seems that our model is doing very good. (R-squared: 0.964), (Adj. R-squared:0.962) The model converted each of dummy variables to a independent variables and showed the p-value. Here, any p-value less than 0.05 means that it is significant to our model. There are some values such BMI and Diphtheria have relatively high p-values which means they are not significant to our mdoel. Although the number of variables increased due to having dummy variables, the number of variables is still very less than number of observations. Therefore, using Ridge Regression for regularization would not be very useful. However, probably using lasso regression or elastic net regression would give us even better result. However our current result is very good in its current shape.
