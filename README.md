# Exoplanet-Habitability-Prediction
> ML model to predict habitability of an exoplanet

## Overview: https://www.nasa.gov/mission_pages/kepler/overview/index.html
> The Kepler Mission is specifically designed to survey our region of the Milky Way galaxy to discover hundreds of Earth-size 
and smaller planets in or near the habitable zone and determine the fraction of the hundreds of billions of stars in our galaxy that might have such planets.
### Kepler Science
The scientific objective of the Kepler Mission is to explore the structure and diversity of planetary systems. This is achieved by surveying a large sample of stars to:
1. Determine the percentage of terrestrial and larger planets that are in or near the habitable zone of a wide variety of stars
2. Determine the distribution of sizes and shapes of the orbits of these planets
3. Estimate how many planets there are in multiple-star systems
4. Determine the variety of orbit sizes and planet reflectivities, sizes, masses and densities of short-period giant planets
5. Identify additional members of each discovered planetary system using other techniques
6. Determine the properties of those stars that harbor planetary systems.

## `1.` Problem:
> Create a model to predict whether or not a planet is in the habitable zone of its host star.

## `2.` Data:
> The data is taken from -> http://exoplanet.eu/catalog/

## `3`. Exploratory Data Analysis:
1. Most of the planets were discovered:

![alt text](https://github.com/vbgupta/Exoplanet-Habitability-Prediction/blob/main/Img/1.png?raw=true)

2. Which detection method detected the most number of planets:

![alt text](https://github.com/vbgupta/Exoplanet-Habitability-Prediction/blob/main/Img/2.png?raw=true)

3. Molecules and the number of planets:

![alt text](https://github.com/vbgupta/Exoplanet-Habitability-Prediction/blob/main/Img/3.png?raw=true)

## `4.` Feature Engineering
1. Orbital Radius using the formula from: https://www.sfu.ca/colloquium/PDC_Top/astrobiology/discovering-exoplanets/calculating-exoplanet-properties.html
2. Assigning Correction Values Based on Star Type
3. Calculating the absolute visual magnitude
4. Calculate bolometric magnitude
5. Calculate absolute luminosity
6. Approximate the boundaries of the habitable zone for this star

## `5.` Model -> svm & DecisionTreeClassifier

## `6.` Model Evaluation:
> Cross Validation test our model on 5 different variations on our testing and training dataset. Based on our cv scores, we observe that 4/5 versions give 
us a perfect score for accuracy, while 1 gives a nearly perfect socre. This can be account for by lack of enough exoplanets that are Earth-like, i.e; 
lack of data indicating a target score of 1.

> **Hence, the model predicts the one record of Earth-like planet(Earth itself) incorrectly based on our model.**
