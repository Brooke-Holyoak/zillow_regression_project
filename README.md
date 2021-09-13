
## Zillow Regression Project
###### This is a repository that will contain a modeling project using the Zillow Database from the Codeup Database Library

# Acquire methodolodgy and notes:
****
### The goal of this project is to determine the features that are the biggest predictors of 'taxvaluedollarcnt', aka home value.

#### Several columns were NOT brought in from the database due to redundancy
##### Columns not brought in: 
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