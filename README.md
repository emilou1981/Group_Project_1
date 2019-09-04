**US County Obesity Rates and Possible Linkages**

This project investigates US county obesity rates and possible economic and demographic linkages using 2016 data from the US Census Bureau, Bureau of Economic Analysis, and County Health Rankings & Roadmaps. All data are at the county level.

**Technical Requirements**

For this analysis, the following additional libraries were used within the Pandas and Jupyter Notebook: 

-   xlrd (pip install xlrd)
-   seaborn (pip install seaborn)
-   statsmodels.api (pip install -U statsmodels)

**Variables**

-   US Census Bureau data: 
    -   SNAP Recipient (%) = (SNAP benefit recipients/population) * 100
-   Bureau of Economic Analysis data:                 
    -   Income Per Capita
-   County Health Rankings & Roadmaps, Robert Wood Johnson Foundation: 
    -   Obesity (%)
    -   Some College (%)
    -   High School Graduate (%)
    -   Unemployment (%)

**Hypothesis**

Do obesity rates in US counties have strong correlations with demographical and economic characteristics such as SNAP benefits, education levels, income per capita, and unemployment rates?

**Analysis**

-   **Scatter Plots and Trendlines**

The results of scatter plots and trendlines of the relationships of the obesity rates versus the other individual independent variables are as the following. The relationship of the obesity rates versus unemployment rates or SNAP recipient rates is a positive one. The relationship is negative between the obesity rates versus income per capita, some college or high school graduate percent. The high school graduate percent and obesity rate relationship is weaker compared to the other relationships. The relationships form around the range of 20% - 40% obesity rates.

<img src="Markdown Images/Screen Shot 2019-09-03 at 5.52.50 PM.png" alt="Obesity vs. Unemployment Rate" style="zoom:40%;" />

<img src="Markdown Images/Screen Shot 2019-09-03 at 5.53.02 PM.png" alt="Obesity vs. SNAP Recipents" style="zoom:40%;" />

<img src="Markdown Images/Screen Shot 2019-09-03 at 5.54.36 PM.png" alt="Obesity vs. Income per Capita" style="zoom:40%;" />

<img src="Markdown Images/Screen Shot 2019-09-03 at 5.54.57 PM.png" alt="Obesity vs. Some College" style="zoom:40%;" />

<img src="Markdown Images/Screen Shot 2019-09-03 at 5.55.13 PM.png" alt="Obesity vs. High School Graduation Rate" style="zoom:40%;" />



-   **Multiple Regression**

The results of the first multiple regression model show multicollinearity issues with positive sign on the coefficient of high school graduate rates. One or more variables are removed at times to resolve multicollinearity. The predictive model of obesity rate for this project has two predictors, SNAP recipient rate and some college percent. The significant F-test and P-value of the final model provides evidence for us to conclude that the obesity rate is significantly determined by SNAP recipient rate and some college percentage.

<img src="Markdown Images/Screen Shot 2019-09-03 at 5.55.42 PM.png" alt="Regression Analysis" style="zoom:40%;" />



-   **Correlation Matrix**

The results of the correlation matrix support our aforementioned findings and conclude this project. The map reflects the findings using scatter plots and trendlines. It also shows correlations among independent variables which cause multicollinearity; e.g., positive strong correlations between unemployment rate and SNAP recipient rates and positive correlation between some college percent and income per capita.

<img src="Markdown Images/Screen Shot 2019-09-03 at 5.55.56 PM.png" alt="image of correlation matrix" style="zoom:40%;" />



**Conclusion **

According to the above findings, there is evidence to conclude that US county SNAP benefits, education levels, income per capita, and unemployment rates are possible linkages to US county obesity rates. Some linkages are positive whereas others are negative and/or weak. The implication, however, suggests against using all variables as predictors of the US county obesity rates together in one model since some of these predictors also have strong correlations among themselves. A model which resolves multicollinearity is presented. However, further tests of the model residuals beyond this project are highly recommended prior to using the predictive model. Exploratory factor analysis and a systematic algorithmic method for finding a suitable model would also be helpful.
