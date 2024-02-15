## Final Project

Team 8: Liza Sadykova & Valentina Hernandez

## Content
### Selected Topic
An analysis of global unemployment data from 2014-2024

### Topic Selection & Hypotheses

Our team will leverage the **Global Unemployment Data sourced from Kaggle** to explore and test various hypotheses pertaining to global unemployment trends from 2014 to 2024. Our analyses will encompass a range of inquiries, including but not limited to:

**Trend Analysis:** We will examine how the global unemployment rate has evolved over the specified timeframe (2014-2024). By analyzing annual variations, we aim to identify overarching patterns and potential drivers influencing global unemployment dynamics.

**Country-Level Analysis:** Our investigation will delve into identifying the countries with the highest and lowest average annual unemployment rates in 2020. This examination will offer insights into the disparities in labor market conditions across different regions of the world.

**Age Group Analysis:** Investigate which age group exhibits the highest average unemployment rate on a global scale. Understanding the differential impact of unemployment across various age demographics will shed light on demographic-specific challenges and opportunities.

**Predictive Modeling:** Employing advanced statistical techniques, we will assess the predictive power of different factors or indicators in forecasting future unemployment trends. By identifying the most influential predictors, we aim to develop robust models for anticipating and mitigating future unemployment challenges.

### Description of Source Data
Our project utilized the dataset from Kaggle: from https://www.kaggle.com/datasets/sazidthe1/global-unemployment-data

The data was stored in CSV format files, from 2014 to 2024. 

In total, our final dataset utilized a CSV file with over 1,135 rows and 13 columns.

Our data was broken up into several sections that led the way for our analysis. 

**country_name**
    Description: Name of the Country (Alphabetically categorized, contains at least a few countries from each continent, great regional variety)

**indicator_name**
    Description: Unemployment

**sex**
    Description: Gender (Male/Female)

**age_group**
    Description: Age groups categorized as Under 15, 15-24, 24+

**age_categories**
    Description: Age categories further classified as Children, Youth, Adult


![image](https://github.com/lizasadykova/Project-4/assets/142169119/f1e352af-e9ec-4467-8789-aa366c503d8c)

    

![image](https://github.com/lizasadykova/Project-4/assets/142169119/97416175-3638-467b-8108-67d12b94c96d)


![image](https://github.com/lizasadykova/Project-4/assets/142169119/ceff1b13-e9fa-4d11-9c17-93bf1388e4d6)


### Analysis Questions

- How has the global unemployment rate changed over the years (2014-2024)?
- What are the countries with the highest and lowest average annual unemployment rates in 2020?
- Which age group has the highest average unemployment rate globally?
- Which factors or indicators are most predictive of future unemployment trends?



## Machine Learning!

**Unupervised Learning:**

![Cluster Unemployment Rates](https://github.com/lizasadykova/Project-4/assets/142169119/a2b650a8-30f7-4c62-a6e9-ff4d94150e62)

Utilizing clustering techniques has significantly enhanced our analysis of global unemployment data. By grouping similar data points based on various attributes, such as geographical location or demographic factors, we've gained valuable insights into the underlying patterns and trends. As you can see in the clustered unemployment rates that compare the rate of unemployment on average between regions from 2014-2024. We can see that for the most part, countries did not experience significant changes in unemployment percentage outside of their baselines from 2014. This cluster chart did not define these countries for us so we took a closer look at what countries experienced an initial more than 30% unemployment rate in 2014 and analyzed it in 2024.

    
![image](https://github.com/lizasadykova/Project-4/assets/142169119/a6ca810c-a163-46e6-ae07-e8bd27dba7f5)


Through this chart we were able to pinpoint which countries significantly increased their unemployment rates and were thus considered outliers in our data. 


![New Note](https://github.com/lizasadykova/Project-4/assets/142169119/715a82e2-5cdd-4497-80d6-30268cecdc4d) 

Next, we were curious about which country had the greatest unemployment change which ended up being Bhutan. The change was primarily noteable in its Youth (15-24) category whose unemployment rate increase 23% in ten years. This begs the question of which factors influenced such a change.

![image](https://github.com/lizasadykova/Project-4/assets/142169119/fa270e86-fb1d-4458-a729-0665009bdbd4)


Furthermore, the top 5 countries with the highest unemployment change appeared to be Afghanistan, Iraq, Bhutan, Jordan, and South Africa. It may be hypothesized that political, social, and economic factors in the Middle East and Africa influenced these stark changes within their respective nations. 


![image](https://github.com/lizasadykova/Project-4/assets/142169119/4175cf69-61ba-4f5c-b117-32609a02a3a3)


**Supervised Learning:**


![New Note](https://github.com/lizasadykova/Project-4/assets/142169119/a2397711-6641-4476-a025-cfe57f10f9fe)

We relied on mean squared error (MSE) to assess the effectiveness of regression models when predicting global unemployment rates for the next ten years. 

Firstly, we gathered historical data that included past unemployment rates alongside relevant predictors like age categories and sex. This dataset formed the foundation for training the regression model. Then, we calculated the MSE by averaging the squared differences between the actual unemployment rates and the model's predictions.

We proceeded to make predictions for the next ten years. The prediction ended up being 11.57% unemployment rate globally.

Interpreting the MSE, I discerned whether the model's predictions closely aligned with actual unemployment rates. The MSE indicated lower precision because of the higher MSE of 8.47% , suggesting that my model's predictions were not strong. So, a higher MSE signified larger prediction errors, prompting us to reassess our model's performance and possibly refine it further.


![New Note](https://github.com/lizasadykova/Project-4/assets/142169119/b06ed2eb-7cb8-4fcc-9fe6-0e94840715c9)

Next, comes our p-value of .99. The elevated p-value resulting from the analysis comparing unemployment rates across different sex and age categories implied a lack of significant difference in unemployment rates between the groups. This suggests that, statistically, there isn't substantial evidence to support variations in unemployment rates based on sex or age. While the findings may seem counterintuitive given the potential socioeconomic disparities that often exist, it indicated a need for more investigation or consideration of other factors influencing employment dynamics. Further exploration into underlying socioeconomic factors, labor market conditions, and policies may shed light on the complex interplay affecting unemployment trends within distinct demographic groups. So, essentially, we failed to reject our null hypothesis and answer the analysis question: Which factors or indicators are most predictive of future unemployment trends? 

![New Note](https://github.com/lizasadykova/Project-4/assets/142169119/d0863481-3631-4bae-be40-ff95541c8f6f)

![New Note](https://github.com/lizasadykova/Project-4/assets/142169119/a2db4b1b-b2ab-4923-b317-b8739540ef46)

![image](https://github.com/lizasadykova/Project-4/assets/142169119/40917108-97f5-492b-8cd0-39475d7caef8)

Finally, we performed an augmented Dickey-Fuller (ADF) test which is a statistical tool used to assess whether a time series dataset is stationary or exhibits a trend over time. Stationarity implies that the statistical properties of the data, such as mean and variance, remain constant over time. In the context of our analysis of global unemployment data, we utilized the ADF test to determine if the unemployment rates fluctuate randomly or follow a predictable pattern over the years based on sex. By conducting the ADF test, we aimed to understand the underlying behavior of the unemployment data and identify any long-term trends or seasonality. If the ADF test indicates that the data is stationary, it suggests a stable unemployment trend, whereas a non-stationary result would imply the presence of underlying factors affecting unemployment rates that need to be further investigated. As you can see the unemployment rates for men and women decreased slightly from 2014-2024, with women having a slightly higher unemployment rate in comparison to men but if you look at the original dataset you can see there is no change at all in unemployment rates between men and women.


## RECOMMENDATIONS FOR FUTURE ANALYSIS

For future analysis, we would dive deeper into demographic segments beyond just sex and age categories. Explore variables such as education level, ethnicity, and urban/rural residence to understand how these factors influence unemployment rates differently across various groups.

Furthermore, we would investigate unemployment rates by different employment sectors, such as manufacturing, services, and agriculture. Analyzing sector-specific trends can provide insights into the resilience of various industries to economic fluctuations and technological advancements.

Overall, I feel as though the data could have included another dataset with a larger set of variables for exploration.



