### Predicting the Next Pandemic of Dengue [Draft]




The data for this competition comes from multiple sources aimed at supporting the Predict the Next Pandemic Initiative. Dengue surveillance data is provided by the U.S. Centers for Disease Control and prevention, as well as the Department of Defense's Naval Medical Research Unit 6 and the Armed Forces Health Surveillance Center, in collaboration with the Peruvian government and U.S. universities. Environmental and climate data is provided by the National Oceanic and Atmospheric Administration (NOAA), an agency of the U.S. Department of Commerce.

In their own words:

Accurate dengue predictions would help public health workers ... and people around the world take steps to reduce the impact of these epidemics. But predicting dengue is a hefty task that calls for the consolidation of different data sets on disease incidence, weather, and the environment.

This is a complicated and messy problem, to be sure. But real data is often complicated and messy. Study up using the resources below—your insights could save lives!


### Problem Description

Your goal is to predict the total_cases label for each (city, year, weekofyear) in the test set. There are two cities, San Juan and Iquitos, with test data for each city spanning 5 and 3 years respectively. You will make one submission that contains predictions for both cities. The data for each city have been concatenated along with a city column indicating the source: sj for San Juan and iq for Iquitos. The test set is a pure future hold-out, meaning the test data are sequential and non-overlapping with any of the training data. Throughout, missing values have been filled as NaNs.


## Data dictionary:

|data| data type | details |
-----|----|------|
|id  | object |  |               
verified | float |  |         
concrete_cement | float |  |    
healthy_metal | float |  |     
incomplete  | float |  |         
irregular_metal   | float |  |   
other | float |  |     

#Approach:

Time Series Analysis


### Features in Data:

#### City and date indicators
city – City abbreviations: sj for San Juan and iq for Iquitos
week_start_date – Date given in yyyy-mm-dd format


#### NOAA's GHCN daily climate data weather station measurements
station_max_temp_c – Maximum temperature
station_min_temp_c – Minimum temperature
station_avg_temp_c – Average temperature
station_precip_mm – Total precipitation
station_diur_temp_rng_c – Diurnal temperature range


#### PERSIANN satellite precipitation measurements (0.25x0.25 degree scale)
precipitation_amt_mm – Total precipitation


#### NOAA's NCEP Climate Forecast System Reanalysis measurements (0.5x0.5 degree scale)
reanalysis_sat_precip_amt_mm – Total precipitation
reanalysis_dew_point_temp_k – Mean dew point temperature
reanalysis_air_temp_k – Mean air temperature
reanalysis_relative_humidity_percent – Mean relative humidity
reanalysis_specific_humidity_g_per_kg – Mean specific humidity
reanalysis_precip_amt_kg_per_m2 – Total precipitation
reanalysis_max_air_temp_k – Maximum air temperature
reanalysis_min_air_temp_k – Minimum air temperature
reanalysis_avg_temp_k – Average air temperature
reanalysis_tdtr_k – Diurnal temperature range


#### Satellite vegetation - Normalized difference vegetation index (NDVI) - NOAA's CDR Normalized Difference Vegetation Index (0.5x0.5 degree scale) measurements
ndvi_se – Pixel southeast of city centroid
ndvi_sw – Pixel southwest of city centroid
ndvi_ne – Pixel northeast of city centroid
ndvi_nw – Pixel northwest of city centroid



#### Perfomance Metric

Performance is evaluated according to the mean absolute error.




#Data:

STAC- SpatioTemporal Asset Catalog Data:  https://s3.amazonaws.com/drivendata-public-assets/stac.tar

Links: https://www.worldbank.org/en/topic/disasterriskmanagement/brief/global-program-for-resilient-housing

https://github.com/google/styleguide/blob/gh-pages/pyguide.md



#External Resources

Dengue Forecasting Homepage
CDC Dengue Overview
NOAA Wiki

https://www.drivendata.org/competitions/44/dengai-predicting-disease-spread/page/82/
