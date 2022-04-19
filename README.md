# Correlation-Between-GDP-and-Happiness-Scores
The code in the Juptyer notebook file goes through the steps in finding a correlation between the GDP of a country and its happiness level. To run the code, it would need to be opened in Jupyter Notebook.

    To do this, I used two datasets, both from Kaggle. One of them contained the happiness scores of several countries along with related information and 
the other contained GDP per capita data from many countries and regions of the world. I used the data from 2015 in both datasets. The datasets can be found here:
-	https://www.kaggle.com/datasets/unsdsn/world-happiness (Happiness dataset)
-	https://www.kaggle.com/datasets/nitishabharathi/gdp-per-capita-all-countries (GDP dataset)

    In terms of the code, it starts out by sorting the data into singular pandas DataFrame object containing the countries, happiness scores and GDP data. Some of the sorting process was automated, but some had to be done manually. 
    Next, a linear regression model is applied to the data, but only after a transformation of applying the natural log to each GDP value. Without this transformation, the data does not follow a linear relationship and so a linear regression model would be worthless. The linear regression model was made using the LinearRegression class from the module sklearn.linear_model. The high r and r-squared values indicate a very strong positive linear correlation. 
    Afterwards, the code creates a linear model on a part of the data and checks it’s performance. This has nothing to do with the analysis and was just for fun. 
    The next part of the code performs a hypothesis test to see if the correlation is statistically significant. It implements a test on the slope of the regression line, with a null of a slope of 0 (no correlation) and an alternative of a positive slope (correlation). The process starts with checking the assumptions of the hypothesis test (along with a normal probability plot from Minitab which is also in the repository). Then it performs the hypothesis test, using a p-value obtained from Minitab. The results concluded (at the 5% significance level) the alternative that there is correlation between GDP and happiness levels. 
    Finally, the code displays statistics and graphs showing the contribution of the aspects of life listed in the happiness dataset. This shows that GDP is not the only thing that is heavily weighted when considering happiness. This opens the door to look into ways of improving the happiness of a country without necessarily increasing it’s GDP, which isn’t an easy thing to do of course.
    The code only shows correlation, not causation between GDP and happiness scores. There might be a third variable that causes them to be strongly correlated like they are. This topic isn’t discussed in the analysis.
