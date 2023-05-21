# Project Overview
In this project, our primary aim was to identify areas of high growth in building permits within New York City and predict the future trends of these permits. We focused our analysis on the five boroughs of New York City: Manhattan, Brooklyn, Bronx, Queens, and Staten Island.

Our dataset consisted of building permit data obtained from the Department of Buildings of New York City. This dataset contained information about each permit, including the filing reason, location details, work type, permittee's license type, approval and expiry dates, job description, estimated job costs, and owner information.

# Business Understanding:
The real estate industry is a cornerstone of New York City's economy, significantly influencing local economic dynamics. With the city's architectural landscape continually evolving, there is a constant demand for new construction. Understanding these construction trends is crucial for stakeholders like real estate investment firms, as it allows them to make well-informed decisions and seize lucrative investment opportunities.

One such firm has expressed interest in leveraging data analysis to gain insights into the current and future construction trends in New York City. Their primary objectives are:

## Understand the Current Demand: 
The firm wants to identify areas within NYC experiencing high growth in building permits. This information will provide a snapshot of the current demand for new construction across the city and identify hotspots of development activity.

## Identify Emerging Trends:
The firm is interested in uncovering any patterns or trends in the approval dates of building permits. This might include seasonal variations, correlations with other factors, or long-term growth or decline trends within specific boroughs or community boards.

## Forecast Future Demand:
Using the historical data, the firm wants to predict the number of building permits likely to be approved over the next year within each borough and, more specifically, within the top growth community boards. This forecast will provide valuable insights into future construction demand and help the firm plan its investment strategy accordingly.

Our goal is to not only understand the past and present construction trends but also accurately predict the future, providing our client with a robust foundation for their investment decisions.



# Data Understanding: 
The [DOB NOW: Build – Approved Permits](https://data.cityofnewyork.us/Housing-Development/DOB-NOW-Build-Approved-Permits/rbx6-tga4) dataset provides information on all approved construction permits issued by the Department of Buildings (DOB) since 2016. The dataset is provided by the Department of Buildings and is updated daily with an automated process. The data contains 446,000 rows and 35 columns, with each row representing a single permit.

The columns in the dataset provide information about the permit, such as the job filing number, filing reason, house number, street name, borough, lot, block, work type, permittee's license type, applicant information, approved date, issued date, expired date, job description, estimated job costs, and owner information.

The [PLUTO](https://www.nyc.gov/site/planning/data-maps/open-data/dwn-pluto-mappluto.page) dataset, an acronym for Primary Land Use Tax Lot Output, is a richly detailed dataset provided by the New York City Department of City Planning. It contains extensive land use and geographic data at the tax lot level.

This data is quite comprehensive and includes detailed information on every building in New York City, including the tax block and lot identifiers, building type, address, owner, land use category, zoning, commercial/residential floor area, year built, number of floors, and so forth.

Additionally, the PLUTO dataset includes spatial information for each tax lot, namely the longitude and latitude, which can be used to map the data.

In our project, we're using the PLUTO dataset to supplement our primary dataset by providing the geographical coordinates (longitude and latitude) for the building permits. This allows us to visualize the building permits data on a map, which can provide additional insights into the spatial distribution and concentration of construction activity across New York City's boroughs and neighborhoods.

## Data Cleaning and Preprocessing:
We started by cleaning the dataset and performing necessary preprocessing steps, such as handling missing values, converting data types, and extracting useful features.

## Exploratory Data Analysis (EDA):
We conducted an exploratory analysis to understand the trends, distributions, and relationships in the data. This helped us identify the top community boards within each borough based on the growth of building permits.

## Time Series Analysis and Forecasting: 
Next, we applied time series analysis to the building permit data. We started with a naive baseline model (Random Walk) to set a benchmark for our forecasts. We then utilized various time series models including ARIMA, SARIMA, and Prophet to forecast the number of permits expected to be approved over the next year for each of the top community boards. Lastly, we trained a Long Short-Term Memory (LSTM) model, a type of recurrent neural network well-suited for time series data, to further improve our predictions.

This series of models allowed us to predict the growth of building permits with a degree of confidence and provide stakeholders with potentially valuable insights into future development opportunities in these areas.

Certainly, here's an example of a Limitations and Further Analysis section for your README file:

## Limitations

1. **Historical Data:** Our analysis relies heavily on historical data, which, while useful, doesn't guarantee future trends. Real estate markets can be influenced by numerous unpredictable factors such as economic downturns, policy changes, and social events.

2. **Scope of Data:** Our current analysis focuses on building classifications and permit approvals. However, real estate investment decisions should also take into account other factors like market demand, property prices, and local amenities, which are not covered in our current data set.

3. **Geographical Focus:** The analysis is specific to NYC, limiting its applicability to other real estate markets. Each market has unique factors that need to be considered independently.

4. **Predictive Model Assumptions:** Our forecasting models are based on a number of assumptions, such as a steady rate of growth and similar market conditions. These assumptions may not hold true, leading to variations in actual outcomes.

## Further Analysis

1. **Inclusion of Additional Factors:** We can enhance the accuracy of our analysis by including other factors, such as real estate price trends, rent yield ratios, neighborhood crime rates, school district ratings, and local amenities.

2. **In-depth Borough Analysis:** A more detailed analysis can be conducted on individual boroughs to understand micro-market trends and identify hidden investment opportunities.

3. **Refinement of Predictive Models:** Our models can be fine-tuned by introducing more complex machine learning algorithms and incorporating more granular data. This would enable more accurate prediction of future trends.

4. **Expansion to Other Markets:** The methodology used for this analysis could be applied to other geographic areas to gain insights into diverse real estate markets.

[Notebook](https://colab.research.google.com/drive/18BKRAicX1gbMob93WoNRHUE39CLUfAOE#scrollTo=cl1J-CsNK_NO)
