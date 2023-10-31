# HealthDataAnalytics


## Introduction
At the time of the writing of this paper, over 152 million cases of the virus have been reported globally- with nearly 3.2 million deaths being COVID-19 related.1 On the home front here in the United States of America, there have been nearly 32.4 million cases reported with just over 576 thousand deaths associated with COVID-19.1 Our group wanted to focus on COVID-19 effects closer to home. North Carolina has reported just over 965 thousand confirmed cases and 12.6 thousand deaths associated with COVID-19.1 We decided to explore the COVID-19 cases and deaths in North Carolina at the county level. Our focus was seeing if we could find a correlation between COVID-19 cases and deaths as it relates to geographical area, race, conditions such as diabetes prevalence and smoking status, and number of people who are fully vaccinated. We aimed to apply machine learning techniques to determine if any of the variables analyzed could be potentially used to predict who may become COVID-19 positive.
## Datasets
We initially looked at numerous datasets to try to find variables that could have some connection to coronavirus cases and/or deaths at the county level in North Carolina. Ultimately, we determined that the NC Department of Health and Human Services (NCDHHS) was what we wanted to use as our main data source. The NCDHHS website provides a public Tableau dashboard with numerous tabs in which you can sort through various datasets of interest. One data set included each North Carolina county, their number of cases (count), number of cases (rate), and number of deaths per county. Another data set available in the Tableau public data was one which listed the number of people who had been fully vaccinated against Coronavirus in each NC county. Next, we selected a dataset from the NC Institute of Medicine which listed the number of interesting county metrics. There were so many data points available that we narrowed down the set to just NC county metrics on the following demographics: elderly, white, Hispanic, and African American populations, college graduation rate, adult obesity, diabetes, and smoking prevalence, as well as poverty, unemployment, and heart disease death rates. By selecting data sets which had attributes listed by county we were able to join these tables together on “county”.
## Data Cleaning
There were several transformations that had to be used in order to load the data into tables in a way that each table could be merged into one large table for our final dataset. The NC Institute of Medicine county metrics data had over twenty-five different data points, thus we narrowed it down to a select number of categories and deleted rows and columns associated with the nonapplicable fields in the Excel spreadsheet. Numbers which were listed as percentages had to be converted into decimal format before loading in PostgreSQL. After loading the data into PostgreSQL, the tables were reviewed for data that needed to be cleaned. There were “null” values in some datasets which had to be converted to “0”. After loading and merging the tables together, reviewing the full merged dataset showed that there were rows that included all “null” values, which had to be removed. 
## Automation and Machine Learning
During the project, each person on the team had a different set up for their database. Some created a new database, while others created a new schema within an existing database. For the purposes of automation, this posed difficult. Therefore, we did not set up our project for automation, but did however, create a file that would simulate automation based on a particular setup. This process utilized the fact that we loaded csv files into our database for cleaning. The automation process included a .bat file that initiated and the creation of a table with needed columns while setting their data types. From there, the loading of the csv file was triggered and then a query to verify. Since we did not set up our project to accommodate automation, we provided just one example of the process.
## Visualization
Using Tableau, we modeled potential relationships between variables from the merged data set “analytics_project_county_covid_metrics.csv”. In the first sheet, we draw a map chart that shows the death distribution among North Carolina Counties. We used a map chart featuring number of deaths indicated by color intensity. In the second sheet, we draw a plot to draw the COVID cases and deaths distribution comparing by adding the feature to select, seeing the different rates of college graduation, heart disease, unemployment, and poverty. Also, in the next sheet, we were interested in seeing different Deaths/Cases distribution among the various populations like Hispanic, White, or African American population. In the last sheet, we have a horizontal bar for each county with a drop down to select among unemployment rate, college graduation rate, poverty rate, and heart disease death rate on the chart.
## Reference
1.	Johns Hopkins University & Medicine. (2021). Coronavirus Resource Center. Johns Hopkins University & Medicine- Coronavirus Resource Center. https://coronavirus.jhu.edu/data.


##-------------------------------------------------------------------------------------------------------------------------------
# LGBM RNN Based Methods for Predicting House Prices

## Abstract
Providing an accurate prediction of the value of a home is important in the home appraisal process. Loan officers use appraisals when determining the size of a mortgage a person can qualify for. In this paper, we propose a machine learning and neural network approach to providing an accurate prediction of the sale price of houses. The predicted sale price can be thought of as the value of a home. We show that an LGBM, RNN, and LGBM-RNN hybrid model are all viable models for solving this problem.

## Introduction
Purchasing or selling a house is a big decision in a person’s life. There are several factors to consider when purchasing a house, like is the house listed for a good deal or is listed for more than what it is worth. Another item to take into consideration is the appraisal value of the house. Predicting house prices is expected to help both buyers and sellers so they can know the price range in the future, then they can plan their finance well. In addition, house price predictions are also beneficial for property investors to know the trend of housing prices in a certain location. This paper hopes to show a machine learning and neural network-based approach to predicting what a house will sell for, given several factors.
There have been several studies on the US housing market using statistics, machine learning, and neural network-based approaches to make inferences about sale prices and time series forecasting. However, we could not find a study that used an aggregation/coupling of LGBM and RNN models. This paper aims to show that this method is a viable method for regression. 

Our group has decided to conduct an analysis on the 2021 housing market prices along with the housing inventory levels. We believe there are anomalies in the housing market that buyers and sellers might not be taking into consideration and have not yet been tested through data analysis. With the housing market prices at an all-time high and inventory levels at an all-time low throughout 2021, we hope to conduct an analysis that helps uncover patterns for this housing crisis and if a correlation between supply and demand truly exists.
Preexisting research work that was done prior to 2020 mainly focused on housing prices and general patterns in the housing market. Our research will differentiate because we will focus more on why the prices are increasing while taking into consideration the low inventory levels and lack of supply for the increasing population. There has been a lot of speculation around the lack of supply is indeed causing the high housing prices and we hope to test that theory with data.
With this project, we hope to gain a better understanding of the correlation between housing prices and inventory levels while also evaluating different factors that might be affecting housing prices other research papers have yet to consider. By conducting this research we hope to answer questions around whether increases in price affect the market at all if the housing inventory levels cannot withstand the growing population and an overall gauge of how much supply and demand truly affect the housing market industry.
Purchasing or selling a house is a big decision in a person’s life and needs a considerable amount of thought and research. Prediction house prices are expected to help both buyers and sellers so they can know the price range in the future, then they can plan their finance well. In addition, house price predictions are also beneficial for property investors to know the trend of housing prices in a certain location. 
Throughout 2021 the housing market has been breaking new records across multiple fronts across the United States. The COVID-19 pandemic and supply chain disruptions have caused low housing inventory leaving home buyers wondering if they should buy now or wait in the hope that more homes become available, and at more affordable prices later in 2022. This study tries to answer this question with the help of data mining algorithms and considering factors that affect house prices.

## Conclusion
All three models tested did well, however, the LGBM and hybrid models outperformed the base RNN. Figure 1 shows that the LGBM and hybrid models were able to have closer predictions than the RNN, especially with houses above the $350,000 range. 



##----------------------------------------------------------------------------------------------------------------------------
# Road Safety Analysis

## Introduction
Our project’s goal is focused on analyzing these roads and helping to provide context around what contributes to the likelihood of overall road safety and what external factors might increase the accident likelihood.
This study will aid in providing drivers with information that can help keep them safe on the road while providing them insights when making decisions on how to decrease their likelihood of getting into an accident on the road. 
We would like to analyze the following…
What days of the week/times of the day experience the highest amount of road traffic
What roads have the highest likelihood of an accident
What factors contribute to a road having an increased likelihood of accidents
What patterns do we see in the data that can help keep cars safe on the road

![image](https://github.com/JShirin/HealthDataAnalytics/assets/71100166/e80d525a-9170-49c5-84ce-0bb15f137459)
