# CrimePredictionChicago
A machine learning model to predict criminal activity in the city Chicago.

Data:

[Chicago crime data](https://data.cityofchicago.org/Public-Safety/Crimes-One-year-prior-to-present/x2n5-8w5q/data)

[Light intensity map](https://www.nasa.gov/sites/default/files/thumbnails/image/26247384716_9281df96cc_o.jpg)

[Street lights](https://data.cityofchicago.org/Service-Requests/311-Service-Requests-Street-Lights-One-Out-No-Dupl/idsv-mf2w)
[Alley lights](https://data.cityofchicago.org/Service-Requests/311-Service-Requests-Alley-Lights-Out-No-Duplicate/up7z-t43p)

[Weather data](https://www.visualcrossing.com/weather/weather-data-services)

[Shapefile](https://data.cityofchicago.org/Facilities-Geographic-Boundaries/Boundaries-Neighborhoods/bbvz-uum9)

[Police Station Locations](https://data.cityofchicago.org/Public-Safety/Police-Stations/z8bn-74gv)

[Crime severity](https://www.ons.gov.uk/peoplepopulationandcommunity/crimeandjustice/datasets/crimeseverityscoreexperimentalstatistics)

Roadmap:
- [ ] Recreate the model for crime prediction in Chicago
- [ ] Add and preprocess only a subset (most important) data
    - ~~[ ] Align sattelite image with shapefile~~
    - [x] create mask to delete predictions outside of Chicago.
    - [ ] Use the last 10 years (2011-2021)
    - [ ] determine grid cell coordinate precizer
    - [ ] (wtf) de prediction predict niks op de kustlijn
- [ ] Evaluate the model: MSE & RMSE
    - [ ] Baseline historical average
- [ ] Add more data that might improve accuracy

# Log
30-11-2022 21:11:
In photoshop de raw sattelite image bewerken en alignen met google maps screenshot:
    - perspective warp 
    - rotatie
    - breedte kleiner met stretch
    - lengte iets kleiner met stretch.
Mislukt so far, word op zijspoor gezet

5-12-2022 13:00
LSTM inputs proberen goed te krijgen als time series met de juiste shape en size.

5-12-2022 20:04
train set:  2011 - 2020
test set:   2021
Baseline: historical average elke dag in het hele test set jaar hetzelfde.