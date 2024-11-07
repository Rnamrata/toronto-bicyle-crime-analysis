# Toronto Bicyle Crime Analysis
 
Bicycle theft is a widespread problem in urban areas, and Toronto, one of Canada’s largest and most lively cities, is no exception. As cycling becomes an increasingly popular mode of transportation for commuting and recreation, the frequency of bicycle thefts has risen, causing significant concern among residents, policymakers, and law enforcement agencies. The aim is to conduct an analysis of crime patterns in Toronto with a specific focus on subway stations and bike thefts. Although this is a narrow scope, we have expanded our project to explore major crime indicators such as Assault, Auto Theft, Break and Enter, Robbery, Theft Over, Homicide, Shootings, etc. Our goal is to identify trends in various types of crime across Toronto neighborhoods and extract valuable insights from the data based on location. The project investigates bicycle theft patterns in Toronto, utilizing spatial and statistical analyses to identify hotspots and influential factors, such as proximity to transit stops and population density.

# Data

To satisfy our purpose we used datasets from the open source data of Toronto Police Service.
 ### 1. Bicycle Thefts dataset:
 https://data.torontopolice.on.ca/datasets/TorontoPS::bicycle-thefts-open-data 
 ### 2. Neighborhood Crime Rates dataset:
 https://data.torontopolice.on.ca/datasets/TorontoPS::neighbourhood-crime-rates-opendata
 ### 3. Major Crime Indicators (MCI) dataset:
 https://data.torontopolice.on.ca/datasets/TorontoPS::major-crime-indicators-open-data

 # Data Pre-processing

The data was decently clean when we got it, but it was missing information we wanted which we got from OpenStreetMap. These were the bus stops, subway stations, and bike parking stands. We also had to calculate the population density of each ward. Most data was merged together based on the ward_id. The OCC_DATE contained a date string that was split into hour, day, month, year. There were a handful of rows with mostly NA values which were removed. The BIKE_COST column had some NA values which were replaced with the mean of the column. We considered replacing them with 0 as a missing value may mean that the owner did not value their bike.

# Result

To analyse the data key methods include Buffer Analysis, Bayesian inference (INLA) for seasonal trends, Kernel Density Estimation for hotspot identification, and Random Forest Classification, which achieved 85% accuracy in predicting theft likelihood based on proximity and other variables. The study highlights limitations like data quality and suggests future efforts to predict theft occurrences and create risk maps to aid resource allocation by law enforcement.