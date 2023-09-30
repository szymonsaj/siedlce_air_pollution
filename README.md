# Siedlce air pollution model

## Inspiration 
Air pollution poses a considerable risk to populations in cities, whether they be substantial metropolises or smaller municipalities. 
One method to assess air quality is by measuring concentrations of PM10 and PM2.5, which are indicative of the particulate matter present in the air.
I have selected Siedlce, Poland, as a subject for creating predictive models of air quality. 
The rationale behind this choice is that in Poland, numerous predictive models and ample measuring data are readily available for larger cities like Krakow, Warsaw, and Katowice,
each equipped with multiple measuring stations. Conversely, smaller cities like Siedlce are often overlooked, despite their need for such models.
Siedlce is a city with a population of approximately 80,000 inhabitants. 
The city has one station for measuring PM2.5 and PM10 concentrations. 
Unlike many larger cities, Siedlce is not heavily industrialized, thus, the primary sources of PM10 and PM2.5 are residential heating and vehicular emissions.
Geographically, Siedlce is situated on a flat terrain, nestled within a small valley. 
This topography can lead to elevated concentrations of pollutants as it can restrict air movement, allowing pollutants to accumulate.
Given the city’s unique characteristics, I’ve decided to develop models to predict air quality in Siedlce. 
My hope is to provide this smaller city with tools comparable to those available in the larger Polish cities, ensuring that its residents have access to accurate and timely information regarding the air they breathe. 
By doing so, we can raise awareness and contribute to improving the overall air quality in Siedlce and similar cities.
This endeavor will help create a future smart city where technology and data contribute to healthier and more sustainable urban living, especially in areas where industrial activities are not the major contributors to air pollution.

## Sources
Dataset was created using: 
* https://siedlce.meteo.com.pl/hist.pl - where I found information about Temperature, Precipitation and Wind Speed,
* https://powietrze.gios.gov.pl/pjp/content/health_informations - skale.jpg - describe AQI,
* https://powietrze.gios.gov.pl/pjp/current/station_details/archive/517 - PM10 and PM2.5 concentrations from station on Konarskiego 11 Street,
* https://journalofbigdata.springeropen.com/articles/10.1186/s40537-021-00548-1 - idea to creation the models,
* Normal Calendar - for weeks and holidays.
I was used the data from January 2020 to December 2022.

## Goal
Creating 2 Machine Learning predictors of concentration PM2.5 and PM10. 
Additionally, I describe AQI for new data predicions.
In the end, I want to predict 8 months in 2023 (from January to August) with corect data.

## What I do
Machine Learning project focused on regression models. In the project, regression models (ANN) were created and used R2, MAE and RMSE parameters to determine their performance. 

## Summary
First, Siedlce is healthy city with a lot of days with Good or Very Good Air Quality Index (Around 90%). 
Unfortunatlly, it isn't good for our models, because the predictors doesn't work well for worst weather parameters. 
During analisys the Dataset, I noticed that during weekends and holidays a concentration of pollutions is highter. 
So, I decided to add this parameters to my dataset. Unfortunatlly, correlation was low. 

