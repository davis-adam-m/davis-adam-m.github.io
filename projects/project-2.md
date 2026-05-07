---
layout: page
title: "World Happiness Scores vs. Education and Population Metrics"
---

## Project Description
Using Python libraries including Pandas, NumPy, MatPlotLib, and Seaborn in a Jupyter notebook, I cleaned and merged a dataset derived from three separate original datasets, each providing complementary data on global countries over a range of years for a number of indicators, including happiness scores, educational benchmarks, and population metrics. I extracted insights about the relationships between variables of interest by analyzing the final dataset to detect patterns and outliers. The research question motivating the analysis: what patterns surface when evaluating the association between happiness scores and metrics of population/education?

[View the output of the project notebook]({{ site.baseurl }}/assets/project-2/world-happiness.html)

## Visualizations
I supplemented provided data with additional data on economic age demographics from BLS, for a total of 6 data sources. I loaded these into Power BI and used Power Query to perform cleaning functions to handle nulls, pivot/unpivot incorrectly formatted data, remove uneccesary columns/rows, merge tables, and create calculated columns.

[![Cleaned Table with Applied Steps]({{ site.baseurl }}/assets/project-1/applied steps.png)](https://davis-adam-m.github.io/assets/project-1/applied%20steps.png)
*An example of a finished table with a list of several applied steps visible to the right.*

A significant requirement of this project was to perform a linear regression analysis on the correlation between customer purchases and average state income. For this requirement, I created a regression table listing all states with x (average state income) and y (average customer purchases over 6mo period) variables, as well as calculated columns for x^2, y^2, and xy. I then used DAX measures to calculate all the variables necessary for the regression formula (b, m, etc.) as well as r^2 coefficient for the correlation between variables.

[![Regression Table with DAX Measure]({{ site.baseurl }}/assets/project-1/dax example.png)](https://davis-adam-m.github.io/assets/project-1/dax%20example.png)
*The final form of the regression table with an example of the DAX measure calculating the variable m.*

Once the 10 tables were finalized, I built a star-schema semantic model and established functional relationships between tables, considering the upstream filtering needs of the reporting layer. 

[![Semantic Model]({{ site.baseurl }}/assets/project-1/model.png)](https://davis-adam-m.github.io/assets/project-1/model.png)
*The final semantic model.*

[![Semantic Model]({{ site.baseurl }}/assets/project-1/model.png)](https://davis-adam-m.github.io/assets/project-1/model.png)
*The final semantic model.*

## Key Insights
1. Drivers of Happiness: Relationships between Happiness Scores and educational metrics vs. population metrics suggest that social and educational outcomes are more direct drivers of national happiness than total population; however, while larger countries display a range of different happiness outcomes, smaller countries consistently tend to report higher happiness scores, even in cases of moderate to low educational attainment or moderately high NEET Rates.

2. The Low NEET/High Primary Completion Factor: Low NEET Rate is one of the strongest predictors of high national happiness scores, but high NEET Rate alone is not a strong predictor for low happiness scores; however, low NEET Rate and high Primary Education Completion Rate together are highly associated with strong Happiness Score outcomes.

3. The Happiest Countries: A distinct takeaway from our final visualization is a clear pattern among the countries reporting the highest happiness scores: small population, high primary education completion rates, and low NEET Rates. The top 6 countries featured in this analysis are Nordic countries with low total population and high educational and social engagement. While many more variables and more rigorous analysis is necessary to make stronger claims, it is clear that we can expect countries with this winning combination of factors to consistently perform well on happiness reports.

