# Used-Car-Price-Prediction

I have used the dataset of used cars from the German market which I got from Kaggle. The data is scraped from popular European online car marketplace AutoScout24.The dataset includes used cars from 1995 to 2023. The dataset has information about approximately 250,000 automobiles.  The dataset has the following features:
➢	Brand: The brand or manufacturer of the car.
➢	Model: The specific model of the car.
➢	Color: The color of the car's exterior.
➢	Registration Date: The date when the car was registered (Month/Year).
➢	Year of Production: The year in which the car was manufactured.
➢	Price in Euro: The price of the car in Euros.
➢	Power: The power of the car in kilowatts (kW) and horsepower (ps).
➢	Transmission Type: The type of transmission (e.g., automatic, manual).
➢	Fuel Type: The type of fuel the car requires (Petrol, Diesel , Electric) .
➢	Fuel Consumption: Information about the car's fuel consumption in L/100km and g/km.
➢	Mileage: The total distance traveled by the car in km.
➢	Offer Description: Additional description provided in the car offer.

I have only used quantitative columns for regression in my model for simplicity though I can even use categorical features like color, transmission type, etc. I only used petrol and diesel cars in my model to ensure consistency of units (mpg, power). 
The data cleaning and transformation process is as follows:
➢	I dropped unnecessary columns in the dataset
➢	Coverted quantitative values from string to float.
➢	Replace the null values with the mean or median values for that feature. Since the distribution for all the features with null values was skewed, I replaced the null values with the median.
➢	Look for infinity values and replace with median.
➢	Converted the features from metric to imperial units. (l/100km to mpg for fuel consumption, km to miles for mileage and kw to hp for power).

Challenges in the project :
I had a huge challenge with more than 10% of null values in the dataset. I solved this with the use of median imputation process and thus did not lose any valuable data due to null values. 

I split the dataset into 80% training and 20% testing sets. I applied linear regression model on the dataset with year, mileage, mpg and power as predictor variables and price in euro as the response variable. 
One key takeaway from this project was that I got to learn the process of mean/median imputation which helped us to fill the null values instead of dropping them altogether from the dataset and maintaining the value of the data. 
