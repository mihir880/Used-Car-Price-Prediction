# Used-Car-Price-Prediction

I have used the dataset of used cars from the German market which I got from Kaggle. The data is scraped from popular European online car marketplace AutoScout24. The dataset includes used cars from 1995 to 2023, comprising information about approximately 250,000 automobiles. The dataset has the following features:

➢ **Brand**: The brand or manufacturer of the car.  
➢ **Model**: The specific model of the car.  
➢ **Color**: The color of the car's exterior.  
➢ **Registration Date**: The date when the car was registered (Month/Year).  
➢ **Year of Production**: The year in which the car was manufactured.  
➢ **Price in Euro**: The price of the car in Euros.  
➢ **Power**: The power of the car in kilowatts (kW) and horsepower (ps).  
➢ **Transmission Type**: The type of transmission (e.g., automatic, manual).  
➢ **Fuel Type**: The type of fuel the car requires (Petrol, Diesel, Electric).  
➢ **Fuel Consumption**: Information about the car's fuel consumption in L/100km and g/km.  
➢ **Mileage**: The total distance traveled by the car in km.  
➢ **Offer Description**: Additional description provided in the car offer.

I have only used quantitative columns for regression in my model for simplicity, though I can even use categorical features like color, transmission type, etc. I only used petrol and diesel cars in my model to ensure consistency of units (mpg, power). 

## Data Cleaning and Transformation Process
The data cleaning and transformation process is as follows:

➢ Dropped unnecessary columns in the dataset  
➢ Converted quantitative values from string to float  
➢ Replaced the null values with the mean or median values for that feature. Since the distribution for all the features with null values was skewed, I replaced the null values with the median  
➢ Looked for infinity values and replaced them with the median  
➢ Converted the features from metric to imperial units (L/100km to mpg for fuel consumption, km to miles for mileage, and kW to hp for power)

## Challenges in the Project
I faced a significant challenge with more than 10% of null values in the dataset. I addressed this with the use of median imputation process, thus preserving valuable data that would have been lost due to null values.

## Model Development
I split the dataset into 80% training and 20% testing sets. I applied a linear regression model to the dataset, using year, mileage, mpg, and power as predictor variables and price in euro as the response variable.

## Key Takeaway
One key takeaway from this project was learning the process of mean/median imputation, which helped fill the null values instead of dropping them altogether from the dataset, thereby maintaining the value of the data.
