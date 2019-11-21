# Valencia Airbnb listings Analysis
## by Eduardo Burgoa

## Table of Contents

1. [Project Motivation](#project-motivation)
2. [Installation](#installation)
3. [File Descriptions](#file-descriptions)
4. [Results](#results)
5. [Acknowledgements](#acknowledgements)


## Project Motivation

The purpose of the analysis is to gain more understanding of the characteristics of Airbnb offer in the city of Valencia and how price listings are affected for companies acting as hosts in Airbnb in the city of Valencia. I am focusing on answering the following questions:

- What neighbourhoods have highest average Airbnb price listings in the city of Valencia?
- What neighbourhoods have greater proportion of listings with multiple listing-owners?
- What factors are related to price of Airbnb listings?

The dataset analysed includes 7233 Airbnb houses in the city of Valencia (Spain) updated on September 30th of 2019. This dataset has been colleted by Murray Cox from public information in Airbnb web page anonimazing any personal data. The purpose of this data collection work is adding data to key metrics so anyone can analyse how Airbnb is being used to compete with the residential housing market.


## Installation

To run this project you have to use an instance of Jupyter Notebook with python 3. 
The python libraries used in this project are:

- numpy
- pandas
- matplotlib
- sklearn


## File Descriptions

- **README.md**. This is the file you are reading at his moment. Its purpose is explaining the motivation of the project and helping to use it.
- **airbnb_valencia_analysis.ipynb**. This file is the notebook where the analyis is implemented. The notebook is oganised as follows: Business understanding, Data understanding, Data preparation, Model, Evaluation adn Deplotment.
- **listings.csv**. This is the main csv file which includes 7233 Airbnb houses in Valencia and has 106 columns describing them.
- **neighbourhoods.csv**. This csv file contains the relation between neighbourhoods and neighbourhoods groups for the city of Valencia.
- **utils.py**. This file includes all helper functions to help clean the data and show analysis results.


## Results

These are the main findings of the analysis:

- The Airbnb listings in the the neighbourghood group CIUTAT VELLA (historical city center) have the highest average price. The second one is POBLATS MARITIMS (next to the beach) and is half the average price of CIUTAT VELLA.

- A 73.8% of listings of CIUTAT VELLA are from hosts with more than one Airbnb listing on the city. EL PLA DEL REAL is the second neighbourhood group with a 68.9% of listings from hosts with more than one Airbnb listing on the city.

- I have created a Random Forest regressor model for predicting listings price achieving a r squared score of 0.69. The features with most importance in the predictions are: `host_total_listings_count`, `host_listings_count`, `host_response_rate`, `availability_90`, `calculated_host_listings_count`, `review_scores_rating`, `calculated_host_listings_count_entire_homes`, `minimum_nights_avg_ntm`, `extra_people`, `availability_60`, `availability_30`, `reviews_per_month`, `neighbourhood_cleansed_EL CARME` and `accommodates`.

A blog post explaining these findings could be found [here](https://medium.com/@eduardo.burgoa/how-companies-acting-as-hosts-in-airbnb-are-affecting-prices-in-your-city-e123dfc9bfc9)


## Acknowledgements
- The dataset has been collected and made accessible publicly by Murray Cox through his site http://insideairbnb.com. The data is provided under a Creative Commons CC0 1.0 Universal (CC0 1.0) "Public Domain Dedication" license.

- The author of function `coef_weights` is Udacity(r) and is found as material in the Udacity Data Science Nanodegree Program(r). This function has been used to show coefficients of the fitted model in order of importance for the prediction.

