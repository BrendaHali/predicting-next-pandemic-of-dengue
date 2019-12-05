# Predicting the Next Pandemic of Dengue
#### by Brenda Hali

----
## Problem Statement

Dengue is a mosquito-borne viral infection that has spread throughout the tropical world over the past 60 years and now affects over half the world’s population. In its less severe form infected patients will experience flu-like symptoms that vary from mild to intense, but severe dengue or, Dengue Hemorrhagic Fever, can be fatal without proper medical care.  The geographical range of dengue is expected to further expand due to ongoing global phenomena including climate change and urbanization.

The Centers for Disease Control (CDC) estimates one third of the world population is exposed to the dengue virus and is at risk of contracting the disease. According to the CDC “As many as 400 million people are infected yearly.” The World Mosquito Program states that “500,000 cases develop into dengue hemorrhagic fever… which results in up to 25,000 deaths annually worldwide.”  The World Health Organization (WHO) in their publication “Global strategy for dengue prevention and control 2012-2020” asserts that “Dengue morbidity can be reduced by implementing improved outbreak prediction and detection through coordinated epidemiological and entomological surveillance”.

A large number of studies have confirmed that the incidence of dengue is positively correlated with climatic conditions, specifically, temperature, humidity and precipitation levels. Many of these studies include quantitative models correlating climate variables with the incidence of dengue cases.

Looking to answer the question: How well would we be able to predict future cases of the disease based on climate variables that are included in weather forecasts? Several departments of the U.S. Federal Government have joined efforts to create the Dengue Forecasting project, which makes climate and dengue data available to data scientists at large and challenges them to submit predictive models to help forecast future dengue epidemics.

Accurate dengue predictions would help public health workers, government, and people around the world take steps to reduce the impact of these epidemics

---


## Executive Summary

[ A Paragraph saying what I did with the project ]

----


### Project Goal

The goal is to answer the question: How well would we be able to predict future cases of the disease based on climate variables that are included in weather forecasts?


### Data Description

- Dengue data. Historical surveillance data was provided for two endemic locations: Iquitos, Peru and San Juan, Puerto Rico. The data include weekly laboratory-confirmed and serotype-specific cases for each location.

- Other data. Environmental data from weather stations, satellites, and climate models are also provided along with relevant metadata.

- Temporal range. Data corresponds to two time periods at each location, a training period and a testing time period. The initial data only covers the training period, 1990-2009 for San Juan and 2000-2009 for Iquitos. Testing data for 2009- 2013.


The data full description can be found here [link to the document].

















### Methodology

The project follows a typical Machine Learning Process

[image]

1. Obtain data
2. Perform exploratory data analysis
3. Choose a learning model
4. Preprocess	the data for machine learning	model (feature	engineering)
5. Tune the model
6. Run	the model on the test dataset
7. Capture predictions
8. Iterate for better results

#### Performance Metric and Evaluation

Mean absolute error (MAE) is the mean absolute difference between predictions yˆ and observations y over n data points:





#### Modeling Process

To model the data, a simple baseline model, FBProphet and SARIMAX models were used.

FB Prophet was the model that performed better with the following results:





## Conclusions  
"This week" weather is not important. Mosquitoes reproduce better in warm, humid weather. Eggs take from 4 to 6 weeks to hatch. And from 4 to 8 months for the first cases to appear.
Right now, given that there is not enough organized data, dengue is still difficult to predict and prevent accurately
Hyperparameters and feature engineering matter!

### Next Steps
Make with more data, create a model that is useful anywhere in the world.
Connect it with a dynamic database for ‘live’ results.




### Computational resources:


To run properly the project you can refer to the `0-Installs` notebook located in the `2-Code` f. older



#### References and external resources:

Dengue Forecasting Project: https://dengueforecasting.noaa.gov/docs/project_description.pdf

Data Driven Competition: https://www.drivendata.org/competitions/44/dengai-predicting-disease-spread/page/82/

Auto regression models forecasting in Python:
https://machinelearningmastery.com/autoregression-models-time-series-forecasting-python/

AMIRA Model: https://alkaline-ml.com/pmdarima/tips_and_tricks.html

Dengue Forecasting Project: https://dengueforecasting.noaa.gov/docs/project_description.pdf
