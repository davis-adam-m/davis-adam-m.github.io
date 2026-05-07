---
layout: page
title: "World Happiness Scores vs. Education and Population Metrics"
---

## Project Description
Using Python libraries including Pandas, NumPy, MatPlotLib, and Seaborn in a Jupyter notebook, I cleaned and merged a dataset derived from three separate original datasets, each providing complementary data on global countries over a range of years for a number of indicators, including happiness scores, educational benchmarks, and population metrics. I extracted insights about the relationships between variables of interest by analyzing the final dataset to detect patterns and outliers. The research question motivating the analysis: what patterns surface when evaluating the association between happiness scores and metrics of population/education?

[View the output of the project notebook]({{ site.baseurl }}/assets/project-2/world-happiness.html)

## Visualizations
Evaluating the relationship between Happiness Score and Population, we detect a weak to moderate negative correlation, with a notable extreme outlier with high population and high happiness score: the United States. This plot clearly displays that there is a pattern of increasing happiness scores with lower population sizes, but there are other other factors at play; the most populated country in the analysis has an above-average happiness score, indicating that variables other than population likely have a greater impact on happiness scores.

<p style="text-align: center;">[![Happiness vs. Population Scatterplot]({{ site.baseurl }}/assets/project-2/hap-pop.png)](https://davis-adam-m.github.io/assets/project-2/hap-pop.png)</p>
*Scatterplot: correlation between happiness scores and population.*

This plot reveals a moderate to strong negative correlation between Happiness Score and NEET Rate, although wide variability is evidenced by both high and low extreme outliers, especially noticeable at the low happiness end of the scale. This pattern may indicate that where happiness scores are low, NEET Rate is not a highly correlated factor, but high happiness is associated with a low NEET Rate; in other words, countries with high happiness scores tend to have low NEET Rates, but countries with low happiness scores have a wide range of NEET Rates.

<p style="text-align: center;">[![Happiness vs. NEET Rate Scatterplot]({{ site.baseurl }}/assets/project-2/hap-neet.png)](https://davis-adam-m.github.io/assets/project-2/hap-neet.png)</p>
*Scatterplot: correlation between happiness scores and NEET rate.*

This plot displays a significant strong positive correlation between happiness scores and completion rates for primary education. This is the strongest correlation in our analysis, indicating that there is an important connection between primary education completion rates and happiness scores for countries. Some especially low outliers on the Primary Completion axis indicate that there are other factors present that can lead to high happiness rates even in cases where primary education completion rates are lower than average. Especially telling are the three countries scoring near 98% on the primary completion axis, but with a broad spread over the entire Happiness Score spectrum, direct evidence that while a strong factor on its own, the metric of completion rates for primary education cannot tell the story on its own. 

<p style="text-align: center;">[![Happiness vs. Education Metric Scatterplot]({{ site.baseurl }}/assets/project-2/hap-edu.png)](https://davis-adam-m.github.io/assets/project-2/hap-edu.png)</p>
*Scatterplot: correlation between happiness scores and primary education completion.*

The multivariate bubble chart pulls together all variables of interest into a cohesive visual unit, telling a more complete story than any individual pairing. With Happiness Score on the Y-axis and NEET Rate on the X-axis, we highlight one of the major takeaways of this analysis visually by the distinct downward slope of data points from left to right; although some outliers are present, reminding us that there are always other factors that can override a correlation, the pattern of decreasing happiness with increasing NEET Rates tells a clear story: youth engagement is a crucial piece of the puzzle for global happiness.

Population is intuitively represented by bubble size; visual inspection confirms that overall, we tend to find that smaller populations are associated with higher happiness scores, and larger populations are associated with lower happiness scores; but the United States stands as an example that we cannot fully understand the relationship from this analysis. There are clearly other factors at play that outweigh population alone.

Finally, bubble color represents Primary Education Completion Rates, with darker colors standing for lower completion rates and lighter colors for higher rates. The multivariable visual allows us to easily make comparisons across variables of interest: we can quickly detect a relationship between high primary completion rates and high happiness scores, low-moderate primary completion rates and high NEET rates, as well as detecting variables that are less correlated such country population and primary completion rates (we can easily distinguish several bubbles of comparable size with a wide range of varying primary completion rates).

[![Multivariate Bubble Chart]({{ site.baseurl }}/assets/project-2/worldhappiness.png)](https://davis-adam-m.github.io/assets/project-2/worldhappiness.png)
*Multivariate bubble chart.*

## Key Insights
1. Drivers of Happiness: Relationships between Happiness Scores and educational metrics vs. population metrics suggest that social and educational outcomes are more direct drivers of national happiness than total population; however, while larger countries display a range of different happiness outcomes, smaller countries consistently tend to report higher happiness scores, even in cases of moderate to low educational attainment or moderately high NEET Rates.

2. The Low NEET/High Primary Completion Factor: Low NEET Rate is one of the strongest predictors of high national happiness scores, but high NEET Rate alone is not a strong predictor for low happiness scores; however, low NEET Rate and high Primary Education Completion Rate together are highly associated with strong Happiness Score outcomes.

3. The Happiest Countries: A distinct takeaway from our final visualization is a clear pattern among the countries reporting the highest happiness scores: small population, high primary education completion rates, and low NEET Rates. The top 6 countries featured in this analysis are Nordic countries with low total population and high educational and social engagement. While many more variables and more rigorous analysis is necessary to make stronger claims, it is clear that we can expect countries with this winning combination of factors to consistently perform well on happiness reports.

