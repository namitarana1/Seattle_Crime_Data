# Seattle Crime ForeCasting
![image](https://user-images.githubusercontent.com/3522782/157556522-073b4709-15f7-4813-97a8-13d800a6e9cf.jpeg)



### Project Name

Seattle Crime Forecasting using ARIMA,SARIMAX.

Author           : Namita Rana


## Data Understanding:

### Dataset Details

## Dataset Name : Seattle Police Department Crime Data: 2008-Present

* Source: [https://data.seattle.gov/Public-Safety/SPD-Crime-Data-2008-Present/tazs-3rd5]
* Steps to retrieve dataset:
* Step1: Click on the link provided.
* Step2: Click on export,the file can be save as csv.
* Step3: Read the csv with pandas.

* The data were collected from Seattle Police Department. The data covered the reported offenses and offense categorization coded to simulate the standard reported to the FBI under the National Incident Based Reporting System (NIBRS) in Seattle from February 2010 to February, 2020. In its original form, it had detailed variables including offense ID, sector,offense Parent Group,Precinct, Sector,Offense, and so on. Each row contains the record of a unique event where at least one criminal offense was reported by a member of the community or detected by an officer in the field.

### What's in this Dataset? : 

* Total : 962145 rows × 17 columns

!![image](https://user-images.githubusercontent.com/3522782/157574324-0c3a0311-a42b-4e59-aebe-c1c18114c4b9.png)
### Columns:

* Column Name : Description
* Report Number: Primary key/UID for the overall report. One report can contain multiple offenses, as denoted by the Offense ID.
* Offense ID: Distinct identifier to denote when there are multiple offenses associated with a single report.
* Offense Start DateTime: Start date and time the offense(s) occurred.
* Offense End DateTime: End date and time the offense(s) occurred, when applicable.
* Report DateTime: Date and time the offense(s) was reported. (Can differ from date of occurrence)
* Group A B: Corresponding offense group.
* Crime Against Category: Corresponding offense crime against category.
* Offense Parent Group: Offense_Parent_Group
* Offense: Corresponding offense.
* Offense Code: Corresponding offense code.
* Precinct: Designated police precinct boundary where offense(s) occurred.
* Sector: Designated police sector boundary where offense(s) occurred.
* Beat: Designated police sector boundary where offense(s) occurred.
* MCPP: Designated Micro-Community Policing Plans (MCPP) boundary where offense(s) occurred.
* 100 Block Address: Offense(s) address location blurred to the one hundred block.
* Longitude: Offense(s) spatial coordinate blurred to the one hundred block.
* Latitude: Offense(s) spatial coordinate blurred to the one hundred block.

## Business Understanding
## Business Problem:

The goal of this modelling is to forecast the crime rates,to figure out which crimes are more frequent,and to make predictions for the number of monthly violent crimes that will occur in future months.

Stakeholder: Seattle Police Department.

### Questions that we want to understand.
* Question1: Does the monthly crimes in Seattle from 2008 to 2020 has an increasing trend?
* Question2: Does the monthly crimes in Seattle from 2008 to 2020 has any time-related patterns that could be explained by ARIMA or SARIMA models?

### Background:

Seattle is the home place of grunge music, a tech hub and a city that prides itself in progress and innovation. It is a beautiful city that is surrounded by lush landscapes and deserves a place on your itinerary.

According to the most recent data from the FBI, the total crime rate in Seattle is 5,081.0 per 100,000 people. That's 105.15% higher than the national rate of 2,476.7 per 100,000 people and 70.75% higher than the Washington total crime rate of 2,975.8 per 100,000 people.

Seattle saw substantial spikes in the number of aggravated assaults and robberies last year, which were largely responsible for the 20% overall increase in violent crime the city experienced in 2021, according to the Seattle Police Department’s year-end crime report.

That report,said the number of aggravated assaults that occurred in Seattle last year — 3,925 — is the most the city has seen in 10 years. It also represents a 24% increase over 2020 totals.

### Methods
### Cleaning and Feature Engineering
This project uses data cleaning and feature engineering to also addressed the non-stationarity,trend,seasonality in the time series.

Since, the time series was nonstationary which means the status of a time series whose statistical properties are changing through time.
We used Statistical test like: Augmented Dickey-Fuller test to check if our series is stationary or not.

Also,we tried to make time series stationary by Differencing.


## Models Development
We have implemented ARIMA,SARIMAX model's with different parameters,with automated parameters generated using auto_arima  to see how results varies with each change in the parameters.Also performed a gridSeach to find the best paramters with low AIC scores.

We are focussed on finding the best model for our time series in terms of lowest Mean Absolute Percentage as it is unit-free and is safe to use for comparing performances of time series forecast values with different units. 

### Metrics used:
MAPE(Mean Absolute Percentage Error)
MAE(Mean Absolute Error)

Import Packages and Functions
We'll make use of the following packages:

numpy and pandas,sklearn is what we'll use to manipulate our data.

matplotlib.pyplot and seaborn will be used to produce plots for visualization.


#### Results
Best MOdel: SARIMA(1,1,1)(1,1,1,12) 
![image](https://user-images.githubusercontent.com/3522782/157556730-cbfea181-8aa1-4cb6-949a-c5adff43f86c.png)

## Sample Output:


#### Future Work
Advanced models like Prophet can be implemented.

## For More Information
Please review my full analysis in !![my Jupyter Notebook](https://github.com/namitarana1/Seattle_Crime_Data/blob/master/Seattle_Crime_Forecasting.ipynb).


For any additional questions, please contact:
## Namita Rana 
### email:namitarana21@gmail.com


## Repository Structure                    

├── Image               #Result Images           
├── NotBook
├── PDF
├── PPt
├── README.md
├── Seattle_Crime_Forecasting.ipynb
└── Project_presentation.pdf

