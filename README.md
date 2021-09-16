
## Zillow Regression Project
###### This is a repository that will contain a modeling project using the Zillow Database from the Codeup Database Library

*** 
## The goals of this project are: 
         1) To determine the features that are the biggest predictors of "tax_value", aka property value.
         2) Once features are determined as being related to the property value, they will be used in a model.
         3) The goal of the model(s) will be to perform better than a baseline model

## The steps in this project are:
        1) Aquired and cleaned Zillow data from the Codeup database. Post cleaning, each observation represented a single unit property from three counties in Los Angeles, which had a transaction between May and August 2017.
        2) Explored data via individual distributions and correlated distributions. Hypothesis testing was also done during the explore phase. The explore phase allowed us to confidently move forward to modeling using three features:  total_sqft, bathrooms and bedrooms.
        3) A baseline prediction model was created, as well as two linear regression models.  Both the OLS and LassoLars models were created and fit using a train dataset. They were also both used on a validate dataset to see how the models performed with unseen data. It was determined that both the OLS model and the LassoLars models performed better than baseline and had value, and that the overwhelming majority of variance could be explained. 
        4) The OLS model was used on a final unseen test dataset, and again performed better than the baseline prediction.

## The findings of this project are:
         1) After exploring the data, through visuals and hypothesis testing, it was determined that the best features for modeling are:  total_sqft, bathrooms, and bedrooms
         2) After creating models, both the OLS linear regression model and the LassoLars model performed nearly identically, and both were better than our baseline.  Both models had value.
         3) After evaluating the OLS linear regression model with unseen test data, it was determined that it still performed better than our baseline.
    
## The summary and next steps for this project are:    
         1) In summary, we are confident that total_sqft, bathrooms and bedrooms are the best predictors of tax_value.
         2) With more time, I would like the next steps to be to explore further into more feature engineering to see if there is more value using new/different features

# Some Acquire methodolodgy and notes:
****
### The goal of this project is to determine the features that are the biggest predictors of 'taxvaluedollarcnt', aka home value.

#### Several columns were NOT brought in from the database due to redundancy
##### Columns not brought in intially: 
    -'buildingclasstypeid' since all properties are classified as single unit
    -'buildingqualitytypeid' since this is a feature regarding structure that is already regulated by residential properties
    -'decktypeid' not included since decktype key not included in Codeup db
    -'totalcalculatedsqft' only sqft feature needed 
    -'calculatedbathnbr', 'fullbathcnt', 'threequarterbathnbr' are redundant
    -'garagetotalsqft' is redundant with 'garagecarcnt'
    -'latitude', 'longitude', 'regionidcity', 'regionidcounty', 'regionidzip' not included since 'fips' code and 'regionidneighboorhood' suffice
    -'lotsizesqft' unneccesary in addition to total sqft- this may be brought in later
    -'poolcnt' is only pool feature needed
    -'propertyzoningdesc' and 'rawcensustractandblock' redundant with 'propertylandusetypes'
    -'yardbuildingsqft' not necessary for residential properties
    -'fireplaceflag' redundant with 'fireplacecnt'
    -'structuretaxvaluedollarcnt' and 'landtaxvaluedollarcnt' not necessary with residential properties
    -'assessmentyear' redundant with db table name
    -'taxdelinquency' columns not necessary for homevalue prediction
***
### Fips Codes found on: https://www.nrcs.usda.gov/wps/portal/nrcs/detail/national/home/?cid=nrcs143_013697

***
### Data Dictionary:
####  A Dictionary for the Zillow Data can be found here: https://docs.google.com/spreadsheets/d/1xOJt3pT0Gecl_bBpicCCj7JbX5ghYPQs5FFEMsnAOKY/edit?usp=sharing

