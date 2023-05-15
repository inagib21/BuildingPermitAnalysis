# Project Overview
In this project, our primary aim was to identify areas of high growth in building permits within New York City and predict the future trends of these permits. We focused our analysis on the five boroughs of New York City: Manhattan, Brooklyn, Bronx, Queens, and Staten Island.

Our dataset consisted of building permit data obtained from the Department of Buildings[DOB NOW: Build – Approved Permits](https://data.cityofnewyork.us/Housing-Development/DOB-NOW-Build-Approved-Permits/rbx6-tga4) of New York City. This dataset contained information about each permit, including the filing reason, location details, work type, permittee's license type, approval and expiry dates, job description, estimated job costs, and owner information.


Analysis of [DOB NOW: Build – Approved Permits](https://data.cityofnewyork.us/Housing-Development/DOB-NOW-Build-Approved-Permits/rbx6-tga4)
# Business Understanding:
The real estate industry is one of the largest and most important industries in New York City, with a significant impact on the local economy. As a result, real estate investment firms are always looking for ways to gain insights into the current demand for new construction in NYC, as this information can help them make informed decisions about where and when to invest.

One such real estate investment firm is interested in this topic and wants to conduct an analysis to gain insights into new construction in NYC. The firm is particularly interested in identifying the current demand for new construction in the city, as well as any trends or patterns that may be emerging in the industry.

# Data Understanding: 
The [DOB NOW: Build – Approved Permits](https://data.cityofnewyork.us/Housing-Development/DOB-NOW-Build-Approved-Permits/rbx6-tga4) dataset provides information on all approved construction permits issued by the Department of Buildings (DOB) since 2016. The dataset is provided by the Department of Buildings and is updated daily with an automated process. The data contains 446,000 rows and 35 columns, with each row representing a single permit.

The columns in the dataset provide information about the permit, such as the job filing number, filing reason, house number, street name, borough, lot, block, work type, permittee's license type, applicant information, approved date, issued date, expired date, job description, estimated job costs, and owner information.

## Data Cleaning and Preprocessing:
We started by cleaning the dataset and performing necessary preprocessing steps, such as handling missing values, converting data types, and extracting useful features.

## Exploratory Data Analysis (EDA):
We conducted an exploratory analysis to understand the trends, distributions, and relationships in the data. This helped us identify the top community boards within each borough based on the growth of building permits.

## Time Series Analysis and Forecasting: 
Next, we applied time series analysis to the building permit data. We started with a naive baseline model (Random Walk) to set a benchmark for our forecasts. We then utilized various time series models including ARIMA, SARIMA, and Prophet to forecast the number of permits expected to be approved over the next year for each of the top community boards. Lastly, we trained a Long Short-Term Memory (LSTM) model, a type of recurrent neural network well-suited for time series data, to further improve our predictions.

This series of models allowed us to predict the growth of building permits with a degree of confidence and provide stakeholders with potentially valuable insights into future development opportunities in these areas.


please view the first simple model here: 
[Notebook](https://colab.research.google.com/drive/18BKRAicX1gbMob93WoNRHUE39CLUfAOE#scrollTo=cl1J-CsNK_NO)
