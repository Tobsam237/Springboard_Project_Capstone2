# Springboard_Project_Capstone2_Readme
![NY accidents](https://www.nydailynews.com/resizer/ZVf7DbHF9JfJJYY7HUg-yhMCv8Q=/800x533/top/arc-anglerfish-arc2-prod-tronc.s3.amazonaws.com/public/7PB6JKNZHFGOVDNTS4OGOITRQU.jpg)

## ANALYSIS OF MOTOR COLLISIONS & CRASHES IN NEW YORK

Vehicle crashes in New York is on the rise and every month the NYPD publishes car crash data for all borough. Stationing NYPD's, EMT's and FDNY strategically before accidents occur can help prevent accidents before they occur or reduce fatalities. This Project aims to take a data oriented approach on vehicle collisions and predict accidents count by borough.

**Data**<br>
The [City of New York Datasets](https://opendata.cityofnewyork.us/) contains data of NYC vehicle collisions which is updated monthly by the FDNY. The dataset fot this project was extractd using APIs and it had 10000 rows and 18 features. Some important features are:
* Crash dates and time
* Location: borough, streetname, latitude, longitude, zipcode
* Vehichle type
* Contributing factor
* Number of casualities and fatalities

[**Data Wrangling**](https://github.com/Tobsam237/Springboard_Project_Capstone2/blob/main/Springboard_Project_Capstone2_.ipynb)<br>
At this stage we cleaned the data prepping for exporalatory analysis. The irreleveant feature to our goal was dropped while some of the missing values in important columns such as zipcode and boroughs were obtained by looking up it's longitudes and latitudes features using uszipcode library.<br>
The data types were also put in check to ensure the data serves its purpose.

[**Exploratory Data Analysis**](https://github.com/Tobsam237/Springboard_Project_Capstone2/blob/main/Springboard_Project_Capstone2_EDA.ipynb)<br>
At this stage we analysed and explored the cleaned data using univariate and bivariate plots to gain a better understanding of our data.
Some of the findings are:
* Brooklyn has the most accidents counts but Queens has the most fatal crashes
* Sedans ranked highest among type of vehicle involved in an accidents
* Driver Inattention/Distraction caused the most accidents
* The summer months and rush hours by day records the most accidents

[**Modelling**](https://github.com/Tobsam237/Springboard_Project_Capstone2/blob/main/Modelling_Springboard_Capstone_two_project.ipynb)<br>
Multiple models were attempted and the best two models were optimised using hyperparamets. The metrics used are: R^2, Root Mean Squared Error, Mean Absolute Error

Estimators attempted: FBProphet, Linear Regression, RandomForestRegressor, RidgeCV, ElasticNet, DecicionTree, Lasso, KNN, GradientBoostingRegressor.

**Take Away**<br>
Random forest performed best among all models attempted with a RMSE value of  28.73  and also supported by R^2 metric score of 0.56.
Margin of Error: The average number of accidents in NYC is 151. Thus our model’s margin of error is 11.379%.

**Future Improvements**<br>
* In the future, I would love to include a weather feature to predict the location of accidents by longitudes and latitudes in NYC. This work is applicabel in many areas.
* Analysis and development of Hospitals and Treatments Centres around accident hotspots with high severity in NYC. This work could help reduce drastically the time for accident victims to get help.
