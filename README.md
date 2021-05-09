# Comparing Income in Baltimore, MD and New York, NY with Opportunity Atlas Data

## Background
This project aims to compare household income in Baltimore (MD) and New York (NY). I choose these two cities because I attend university in Baltimore, and have visited New York most of the time as an international student. While Baltimore and New York are only 3-hours drives away and both are in a Metropolitan area, they are very different. New York's medium income is around $52,737 while Baltimore's median income is $41,819. New York housing costs are 495.4% more expensive than Baltimore housing costs. And New York's population is around 8,000,000 while Baltimore's population is around 620,000. The above data are from [2021 Compare Cities Overview: Baltimore, MD vs New York, NY](https://www.bestplaces.net/compare-cities/baltimore_md/new_york_ny/overview).

In particular, I want to dive into the comparison of the household income in Baltimore and New York. Since household income is related to socioeconomic status, and are key indicators of the economic robustness of a city, I would also like to investigate income difference between U.S. Native and Immigrant, and income comparision among differenct races.

The dataset I used for this study is from the [Opportunity Insight Project](https://www.opportunityatlas.org/), which is a project with a mission is to identify barriers to economic opportunity and develop scalable solutions that will empower people throughout the United States to rise out of poverty and achieve better life outcomes.

## Business Question 
_How is the Individual Income level differ in Baltimore and New York?_

## List of Data Source 
I obtain my data source all from the same website (https://www.opportunityatlas.org/) . And attached are links to my source cvs files: 
- [Baltimore City Immigrant Individual Income](https://github.com/sophiaxuu/decision-analytics/blob/main/mini-proj1/sources/baltimore_cty_kir_imm_rP_gP_pall.csv)
- [Baltimore City U.S. Native Individual Income](https://github.com/sophiaxuu/decision-analytics/blob/main/mini-proj1/sources/baltimore_cty_kir_native_rP_gP_pall.csv)
- [New York City Immigrant Individual Income](https://github.com/sophiaxuu/decision-analytics/blob/main/mini-proj1/sources/ny%20cty_kir_imm_rP_gP_pall.csv)
- [New York City Native Individual Income](https://github.com/sophiaxuu/decision-analytics/blob/main/mini-proj1/sources/ny_cty_kir_native_rP_gP_pall.csv) 

- [Average individual income for immigrants in New York and in Baltimore](https://github.com/sophiaxuu/decision-analytics/blob/main/mini-proj1/sources/imm_parent_child_income_comparisoin.xlsx)

## Data Question
### 1. How does the Individual Income level differ for U.S. Native and Immigrants in Baltimore and New York?

![Figure 1: Average Individual Income for Immigrants and U.S. Natives in Baltimore](https://github.com/sophiaxuu/decision-analytics/blob/main/mini-proj1/figures/Figure1.png)
![Figure 2: Average Individual Income for Immigrants and U.S. Natives in New York](https://github.com/sophiaxuu/decision-analytics/blob/main/mini-proj1/figures/Figure2.png)

By observing Figure1 and Figure2, we can find out that the Average Individual Income for Immigrants for both Baltimore and New York are approximately the same, which is about $31,500. And the Average of Individual Income for U.S. Native for both Baltimore and New York are also approximately the same, which is around $30,000. The finding is a bit surprise for me because previously I would assume immigrants will have a lower level of average income than natives. Some possible reasons may be there is a higher population of U.S. natives who are in the lowest income range, which could potentially drive the average down. 

### 2. How does Parent Income affect the Immigrant’s Average Individual Income in Baltimore? 
![Figure 3: Average Individual Income Relative to Parent Income for Immigrants in Baltimore](https://github.com/sophiaxuu/decision-analytics/blob/main/mini-proj1/figures/Figure3.png)

The answer is obtained by getting the average individual income level for different races (black, white, Hispanic, Asian), and for different parent income levels (high represent 75 percentiles in income level, middle represent 50 percentiles, and low represent 25 percentile). 

There are a few interesting observations. First, I find that the Hispanics in Baltimore relatively low social mobility - this is shown by the high positive gradience of the approx linear relationship between Parent Income Level and Individual Average Income. The steep line represents that individuals with wealthy parents tend to have much higher income. 

Secondly, I find that there is a negative correlation between Parent Income Level and Individual Average Income for Asian living in Baltimore. This is counter-intuitive as it means that individuals with less wealthy parents will have higher income. 

### 3. How does Parent Income affect the Immigrant’s Average Individual Income in New York? 
![Figure 4: Average Individual Income Relative to Parent Income for Immigrants in New York](https://github.com/sophiaxuu/decision-analytics/blob/main/mini-proj1/figures/Figure4.png)

The answer is also obtained by getting the average individual income level for different races (black, white, Hispanic, Asian), and for different parent income levels (high represent 75 percentiles in income level, middle represent 50 percentiles, and low represent 25 percentile)

Looking at the line graph created, there is a positive correlation between Parent Income and Individual Income for all races. And the most are linearly related with a similar gradient. 


## My Data Manipulation 
This is a step-by-step descriptions on how I manipulated the Excel data and get the following files: 
- [New York City Immigrants vs U.S. Native Income](https://github.com/sophiaxuu/decision-analytics/blob/main/mini-proj1/sources/ny_cty_kir_imm_and_native_rP_gP_pall.xlsx)
- [Baltimore City Immigrants vs U.S. Native Income](https://github.com/sophiaxuu/decision-analytics/blob/main/mini-proj1/sources/baltimore_cty_kir_imm_and_native_rP_gP_pall.xlsx)
- [Immigrant's Parent and Individual Income Comparision](https://github.com/sophiaxuu/decision-analytics/blob/main/mini-proj1/sources/imm_parent_child_income_comparisoin.xlsx)

Steps: 
1. To compare average individual income for immigrants and US Native, I create pivot table with immigrant/native category, and values of average individual outcome. 
2. To see trend of changes in average income relative to parent income for immigrants in baltimore, I merge several line graph (for each race) into one.
3. To see trend of changes in average income relative to parent income for immigrants in New York, I merge several line graph (for each race) into one.

## Summary
To summarize from the above analysis, I find that: 
The individual income level for U.S. Native is smaller than Immigrants for both Baltimore and New York, and the values are approximately the same. 

In most cases, individuals with wealthy parents will have higher individual income than the poor. Yet there is still a notable difference in income inequality among different races both in New York and Baltimore. 

For New York, the correlation between parents and children's income level is pretty similar across all races.  For Baltimore, some specific races have atypical relationships between parent income and children's income. 

These data findings show that New York has a more robust economy than Baltimore as it has a higher average household income. To further explore why there is such a income difference, we could explore data on education level, employment types etc.
