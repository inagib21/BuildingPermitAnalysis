![image](https://github.com/inagib21/BuildingPermitAnalysis/assets/45716414/bb67dbe7-c231-4f44-b207-8f4593272ff3)


# Project Overview
Our project has two primary goals: identify and predict trends in NYC building permits and classify pre-1940 buildings based on recent maintenance. These efforts provide critical insights for our investment firm stakeholders, helping them seize valuable real estate opportunities.

# Business Understanding:
Real estate, a key economic driver in NYC, continually evolves due to the constant demand for new construction. By understanding these trends, stakeholders, like investment firms, make informed decisions and capitalize on lucrative opportunities. 

## Stakeholder: MetroStar Real Estate Investment Firm

MetroStar Real Estate Investment Firm is a NYC-based entity keen on leveraging data to understand and predict city construction trends. By focusing on new developments and buildings ripe for renovation, the firm aims to capitalize on investment potential. Our data analysis and predictive modeling services will offer crucial insights, shaping their future investment strategies effectively.

# Data Understanding: 
We used two datasets, [DOB NOW: Build – Approved Permits](https://data.cityofnewyork.us/Housing-Development/DOB-NOW-Build-Approved-Permits/rbx6-tga4) and [PLUTO](https://www.nyc.gov/site/planning/data-maps/open-data/dwn-pluto-mappluto.page), which offer comprehensive information on building permits and extensive land use details respectively.

## Old Buildings Classification & Maintenance 
We identified pre-1940 NYC buildings and categorized them based on maintenance status post-2018: 
- **Maintained Buildings:** Received upkeep since 2018, potentially in better condition but could still benefit from improvements.
- **Unmaintained Buildings:** Lacked maintenance since 2018, offering significant renovation and value enhancement opportunities.
  ![image](https://github.com/inagib21/BuildingPermitAnalysis/assets/45716414/5a7ddba4-2251-40d5-a1a7-e3ab69098da4)
                        <img width="571" alt="Screen Shot 2023-05-21 at 12 15 57 AM" src="https://github.com/inagib21/BuildingPermitAnalysis/assets/45716414/8ef3d147-16f7-4920-8c03-4da95cfbb96f">

     
    

                      
Classification Model Insights
The 'Approved Year' feature played a critical role in our model due to its strong connection with recent renovation activity. This aligns with our goal of identifying older buildings in top community boards that haven't seen recent upgrades, enabling targeted renovation planning and effective resource allocation.

However, the tight correlation between 'Approved Year' and the target variable 'recent_permit' might lead some to view this as data leakage. Hence, while the model successfully predicts recent renovations, its predictions may not go beyond what can be directly inferred from the 'Approved Year'.


# Data Cleaning and Preprocessing:
We cleaned and preprocessed the datasets by handling missing values, converting data types, and extracting useful features.

# Exploratory Data Analysis (EDA):
We conducted an EDA to understand data trends, distributions, and relationships, and identified top community boards within each borough based on building permit growth.

Here we can see the distribution of permits approved by borough:
<img width="739" alt="Screen Shot 2023-05-21 at 12 01 07 AM" src="https://github.com/inagib21/BuildingPermitAnalysis/assets/45716414/574518f9-f6d3-4da1-baec-4f58cf85fca0">



# Time Series Analysis and Forecasting: 
We performed time series analysis on the permit data and utilized several models (ARIMA, SARIMA, Prophet, LSTM) to forecast permit approval trends over the next year for each top community board.

### Prediction results for community board with the most growth in the BRONX.
<img width="896" alt="Screen Shot 2023-05-21 at 12 19 44 AM" src="https://github.com/inagib21/BuildingPermitAnalysis/assets/45716414/60fecec1-d64a-48f6-aa04-0b28045a7632">

RMSE: 8.979906
MAE: 6.870866

Our LSTM model's performance in predicting the number of building permits for the top community board in the Bronx is promising. The model achieved a Root Mean Squared Error (RMSE) of 8.98 and a Mean Absolute Error (MAE) of 6.87. These metrics suggest that our forecasts are close to the actual values, demonstrating the model's effectiveness in predicting building permit trends for future strategic planning.


# Limitations
While our analysis offers valuable insights, it's important to consider certain limitations:

1. **Reliance on Historical Data:** Past trends may not guarantee future outcomes due to unpredictable factors such as economic downturns or policy changes.
2. **Data Scope:** Our focus on building classifications and permits omits other crucial factors like property prices, market demand, and local amenities.
3. **Geographical Limitation:** Our NYC-centric analysis might not translate to other real estate markets with unique factors.
4. **Model Assumptions:** Our models assume a steady rate of growth and similar market conditions, which might not hold true.

# Further Analysis
Our work can be extended in several ways:

1. **Incorporate Additional Factors:** Enhance analysis accuracy by including elements like real estate prices, neighborhood crime rates, and school district ratings.
2. **Detailed Borough Analysis:** Understand micro-market trends within individual boroughs for hidden investment opportunities.
3. **Refine Predictive Models:** Fine-tune models with more complex machine learning algorithms and granular data for accurate future trend predictions.
4. **Expand to Other Markets:** Apply our methodology to different geographic areas for insights into diverse real estate markets.
Certainly, here is a section to help navigate your repository:

## Navigating The Repository

1. **.gitignore:** This [file](https://github.com/inagib21/BuildingPermitAnalysis/blob/main/.gitignore) is used to exclude certain files from the repository. If there are files or paths that we want Git to ignore, we can add rules for them in this file.

2. **LICENSE:** This [file](https://github.com/inagib21/BuildingPermitAnalysis/blob/main/LICENSE) contains information about the license that governs the use and distribution of the repository's content.

3. **Notebook.ipynb:** This Jupyter  [Notebook](https://colab.research.google.com/drive/18BKRAicX1gbMob93WoNRHUE39CLUfAOE#scrollTo=cl1J-CsNK_NO) for detailed analysis and findings.  contains all the code used for data preprocessing, exploratory data analysis, model training, model evaluation, and other computations.

4. **README.md:** This Markdown (file)[https://github.com/inagib21/BuildingPermitAnalysis/blob/main/README.md] provides an overview of the project, describes the business context, data, approach, results, and limitations, and explains how to navigate the repository. If you are viewing the project on GitHub, this is the first file you see on the main page of the repository.

Remember, you can click on any file in the repository to view its contents. If you have any questions or need additional help navigating the repository, don't hesitate to ask.
