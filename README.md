# COVID-19-impact-on-Hospital-related variables
This analysis was designed to understand the impact that COVID-19 had on select hospitals-related variables.

**Add image here**


**BACKGROUND**
The onset of COVID-19 has adversely affected our lives. As of July 31st, 2021, there have been approximately 35 million cases and 620,000 deaths.  Although many studies have indicated that chronic health conditions (i.e., obesity, cardiovascular disease, and diabetes) are related to COVID-19 related deaths, limited data have examined the impact of hospital system factors on COVID-related deaths.

_Purpose:_

The purpose of this study was to examine the relationship between hospital-related variables and COVID-19 deaths.  The proposed independent variables for our analysis were the number of patients hospitalized and the number of patients who were admitted to the intensive care unit (ICU). 
The dependent variable was COVID-confirmed or COVID-probable death.

_Hypotheses:_

1. We hypothesize that COVID-19 related hospitalization will be positively and significantly associated with COVID-19 related deaths.
2. COVID-19 related ICU stays will be positively and significantly associated with COVID-19 related deaths

**METHODS**

_Data availability_. Data were scraped from a publically available website (add website).  The original data consisted of 53 columns and 20,780 rows.  This time-series data tracked COVID-19 variables daily between January 1st, 2020, to March 7th, 2021. However, for the purposed of this study, we focused on data points that ranged from March 1st, 2020, to February 29th, 2021. 

_Data cleaning._ Data that were not pertinent to our analyses were deleted to create a new data frame.  To transform the data from long-form (i.e., time series) to short form, we used a series of Groupby and aggregate functions in Pandas version 3.6.  The resulting data frame consisted of 13 rows and 55 columns that contained summative data for our variables of interest. 

_Statistical analysis._ Descriptive statistics in the form of plots (i.e., MatPlotlib) were used to provide data on COVID-positive case count. Next, we computed a series of correlation heatmaps, regression, and scatter plots to describe associations between our independent and dependent variables. Finally, correlations were computed with Seaborn; regressions were computed with Scipy, and scatter plots were computed with Matplotlib. 

**RESULTS**
Below is a list of our study results by the visualization presented in the analysis. 

_Barchart._ COVID-positive cases appear to be highest in California, Florida, New York, and Texas.  We note that these data were not adjusted by population size. 

_Correlation heatmap._ Our correlation plot indicates significant and positive associations among our variables of interest.  COVID-related deaths were significantly and positively associated with ICU visits (r = 0.64), being on a ventilator (r = 0.42), and being hospitalized (r = 0.32).

_Regression and scatter plots._ The regression lines and scatter plots indicate a similar pattern of relationships as observed in the correlation matrix. Again, all variables are positively and significantly associated. 

_Line graphs over time._ The multiple line plot indicates similar trends in our data.  Of note, we observed peaks in COVID-19 cases around regular holiday seasons (i.e., Fourth of July and between Thanksgiving and Christmas).  In addition, ICU visits and COVID-related deaths follow a similar pattern of behavior over time.  Lastly, there is a 1-month lag between positive cases and    ICU visits, as observed in the first few months of our chart. 

**DISCUSSION**

There were significant and positive relationships in our sample between ICU visits, hospitalization, and COVID-19 related death.  These data are consistent with studies reported in the popular press as well as in scientific journals. Overall, our data show that death is a likely outcome once patients are hospitalized or visit the ICU to battle COVID-19. 

We note that these data do not paint a complete picture of the COVID-19 pandemic.  Other variables such as rates of obesity and other chronic health conditions (e.g., diabetes and cardiovascular disease), percent of adults over the age of 65 years, and the number of hospital and patient to provider ratios are contributing factors to these results.  Unfortunately, we could not include these data due to time constraints, which limits how much we can speculate about what is occurring as a whole and at the state level. Future studies should consider improving our analyses by adding these covariates to their models. 

This analysis had several strengths, including a large sample size, which included all 50 states and other US territories.  However, these data are not without their limitations.  In particular, we took a cross-sectional approach to analyze most of the data despite the longitudinal nature of the dataset. Therefore, these data do not imply causality. As a result, additional analyses that consider the nesting that occurs within states and days are warranted. Further, these data a non-normal, and other analytic techniques that account for the non-normality will better approximate the distribution of the outcome variable. 

In summary, this was an initial attempt to illustrate a complicated set of data plagued with issues such as missing or null values. The inconsistency of the missingness suggests that imputation may not enhance the interpretation of the data. Despite its flaws, we were able to observe significant and meaningful relationships among our variables of interest. 

