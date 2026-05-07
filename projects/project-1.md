---
layout: page
title: "Apparel Chain Market Analysis"
---

## Project Description
This project required the use of Power BI to clean and synthesize multiple data sources in diverse formats, build a semantic model and establish functional relationships, perform a regression analysis using calculated columns and DAX measures, and design a report layer for visual analysis, to be shipped with an executive summary packaging findings, key insights, and data-driven market expansion suggestions/targeted product recommendations. 

## Data Preparation
I supplemented provided data with additional data on economic age demographics from BLS, for a total of 6 data sources. I loaded these into Power BI and used Power Query to perform cleaning functions to handle nulls, pivot/unpivot incorrectly formatted data, remove uneccesary columns/rows, merge tables, and create calculated columns.

![Cleaned Table with Applied Steps]({{ site.baseurl }}/assets/project-1/applied steps.png)
*An example of a finished table with a list of several applied steps visible to the right.*

A significant requirement of this project was to perform a linear regression analysis on the correlation between customer purchases and average state income. For this requirement, I created a regression table listing all states with x (average state income) and y (average customer purchases over 6mo period) variables, as well as calculated columns for x^2, y^2, and xy. I then used DAX measures to calculate all the variables necessary for the regression formula (b, m, etc.) as well as r^2 for the correlation between variables.

![Regression Table with DAX Measure]({{ site.baseurl }}/assets/project-1/dax example.png)
*The final form of the regression table with an example of the DAX measure calculating the variable m.*

Once the 10 tables were finalized, I built a star-schema semantic model and established functional relationships between tables, considering the upstream filtering needs of the reporting layer. 

![Semantic Model]({{ site.baseurl }}/assets/project-1/model.png)
*The final semantic model.*

## Visualizations

![Main Insight Chart]({{ site.baseurl }}/assets/project-1/applied steps.png)
*Description: This chart illustrates the 15% growth trend observed in Q3.*

![Main Insight Chart]({{ site.baseurl }}/assets/project-1/applied steps.png)
*Description: This chart illustrates the 15% growth trend observed in Q3.*

![Secondary Analysis]({{ site.baseurl }}/assets/project-1/applied steps.png)
*Description: Correlation heatmap showing the relationship between marketing spend and conversions.*

![Main Insight Chart]({{ site.baseurl }}/assets/project-1/applied steps.png)
*Description: This chart illustrates the 15% growth trend observed in Q3.*

![Main Insight Chart]({{ site.baseurl }}/assets/project-1/applied steps.png)
*Description: This chart illustrates the 15% growth trend observed in Q3.*

![Main Insight Chart]({{ site.baseurl }}/assets/project-1/applied steps.png)
*Description: This chart illustrates the 15% growth trend observed in Q3.*

## Resources
[📥 Download Project Files (.zip or .pdf)](#)
