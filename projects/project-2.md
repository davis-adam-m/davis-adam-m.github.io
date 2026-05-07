---
layout: page
title: "World Happiness Scores vs. Education and Population Metrics"
---

## Project Description
This project required the use of Power BI to clean and synthesize multiple data sources in diverse formats, build a semantic model and establish functional relationships, perform a regression analysis using calculated columns and DAX measures, and design a report layer for visual analysis, to be shipped with an executive summary packaging findings, key insights, and data-driven market expansion suggestions/targeted product recommendations.

[📥 Download Project Files (.zip)]({{ site.baseurl }}/assets/project-1/Project Files.zip)

* Power BI report (.pbix)
* Executive Summary (.docx)

## Data Preparation
I supplemented provided data with additional data on economic age demographics from BLS, for a total of 6 data sources. I loaded these into Power BI and used Power Query to perform cleaning functions to handle nulls, pivot/unpivot incorrectly formatted data, remove uneccesary columns/rows, merge tables, and create calculated columns.

[![Cleaned Table with Applied Steps]({{ site.baseurl }}/assets/project-1/applied steps.png)](https://davis-adam-m.github.io/assets/project-1/applied%20steps.png)
*An example of a finished table with a list of several applied steps visible to the right.*

A significant requirement of this project was to perform a linear regression analysis on the correlation between customer purchases and average state income. For this requirement, I created a regression table listing all states with x (average state income) and y (average customer purchases over 6mo period) variables, as well as calculated columns for x^2, y^2, and xy. I then used DAX measures to calculate all the variables necessary for the regression formula (b, m, etc.) as well as r^2 coefficient for the correlation between variables.

[![Regression Table with DAX Measure]({{ site.baseurl }}/assets/project-1/dax example.png)](https://davis-adam-m.github.io/assets/project-1/dax%20example.png)
*The final form of the regression table with an example of the DAX measure calculating the variable m.*

Once the 10 tables were finalized, I built a star-schema semantic model and established functional relationships between tables, considering the upstream filtering needs of the reporting layer. 

[![Semantic Model]({{ site.baseurl }}/assets/project-1/model.png)](https://davis-adam-m.github.io/assets/project-1/model.png)
*The final semantic model.*

## Visualizations
* A scatterplot with trendline, visualizing the correlation between average state income and average customer purchases, including cards displaying the r^2 value and regression formula.

[![Linear Regression]({{ site.baseurl }}/assets/project-1/regression.png)](https://davis-adam-m.github.io/assets/project-1/regression.png)
*Linear regression scatterplot.*

* Heatmap based on average income by state, allowing visual identification of high-potential areas and clusters, with tooltips displaying average state income, average predicted income of customer base (based on regression formula), number of customers per state, and average spend per customer (past 6mo period).

[![Income Heatmap]({{ site.baseurl }}/assets/project-1/heatmap.png)](https://davis-adam-m.github.io/assets/project-1/heatmap.png)
*Heatmap of average state income.*

* A histogram displaying the distribution of predicted incomes across the existing customer base, including a card displaying the customer with highest expected income based on purchase history. The report allows drill-through to either the product recommendations page or the income heatmap, allowing easy review of areas with particular income ranges and product recommendations for those areas/income ranges.

[![Income Histogram]({{ site.baseurl }}/assets/project-1/histogram.png)](https://davis-adam-m.github.io/assets/project-1/histogram.png)
*Histogram displaying the distribution of predicted incomes across the existing customer base.*

* Product recommendation report page, featuring a waterfall chart for quick identification of stock on hand per product, a macro for the high-level marketing strategy recommendation, sliders for exploration of products by filtering for 3 variables, a table listing product names and details, and a thumbnail of the income histogram allowing drill-through and dynamic display based on selected income ranges or products.

[![Product Recommendations]({{ site.baseurl }}/assets/project-1/prod rec.png)](https://davis-adam-m.github.io/assets/project-1/prod%20rec.png)
*Product recommendation report page.*

* A breakdown of total sales by state and customer age range using an interactive decomposition tree visual, linked to bar charts for average spend per customer by state and predicted total annual apparel spend by state (based on existing customer base age demographics and BLS economic data), as well as a table dsplaying the age ranges and their associated metrics.

[![Sales Breakdown]({{ site.baseurl }}/assets/project-1/sales decomp.png)](https://davis-adam-m.github.io/assets/project-1/sales%20decomp.png)
*Description: This chart illustrates the 15% growth trend observed in Q3.*

* A time-series overview for the given period, showing declining total sales trend and recent increase in average purchase amount.

[![Sales Trend Time Series]({{ site.baseurl }}/assets/project-1/sales trend.png)](https://davis-adam-m.github.io/assets/project-1/sales%20trend.png)
*Time-series line and bar chart for total sales and average purchase amount.*

## Executive Summary
The Power BI report ships with an Executive Summary .docx file, breaking down findings, key insights, and recommendations with walkthroughs of the analytical process and supporting visualizations.

[![Cleaned Table with Applied Steps]({{ site.baseurl }}/assets/project-1/exec summary gif.gif)](https://davis-adam-m.github.io/assets/project-1/exec%20summary%20gif.gif)
*A preview of the executive summary document.*

