# EDA-on-Airbnb-Germany
<!-- TABLE OF CONTENTS -->
## Table of Contents

* [Introduction](#introduction)
* [Data Source](#data-source)
* [Tools](#tools)
* [Data Preprocessing](#data-preprocessing) 
  * Feature selection
  * Missing value treatment
  * Outlier detection
  * Correlation Analysis
* [Visualizations](#visualizations)
  * Graphical visualizations
  * Geo-sptaial visulizations
* [Conclusion](#conclusion)
* [Recommendations and Future Work](#recommendations-and-future-work)

<!-- INTRODUCTION -->
## Introduction

Peer-to-peer sharing has changed the way of working in many industries in the last decade. Airbnb is an innovation in the tourism industry, both in terms of tourist experience and ease of adoption. Airbnb’s profits rely on the dynamic pricing market that they participate in. Airbnb hosts can set their own price based on the market prices. This project focuses on performing an Exploratory Data Analysis on the Airbnb data of Germany mainly Munich and Berlin to draw important insights about their Airbnb listings.


<!--DATA SOURCE-->
## Data Source

The data has been downloaded from [Inside Airbnb](http://insideairbnb.com/get-the-data.html) website on 22 February 2021.
we have total number of 25104 rows and 74 columns in our dataset.

<!--TOOLS-->
## Tools
* Jupyter notebook has been used to perform the entire EDA process for this project
* Following python libraries were used for performing EDA:
  * numpy
  * pandas 
  * matplotlib
  * geopandas 
  * missingno 
  * datetime 
  * seaborn 
  * pywaffle 
* To enable geospatial visualizations, we will have to create a geo_env in our jupyter notebook which can be done by following the steps in this [article](https://medium.com/analytics-vidhya/fastest-way-to-install-geopandas-in-jupyter-notebook-on-windows-8f734e11fa2b).


<!--DATA PREPROCESSING-->
## Data Preprocessing
* **Feature selection:**
  A total of 74 features were available, unnecessary and unusable features were first dropped. Necessary transformation of column values has been done to get started with        preproceesing of data. Extra Tree Regressor technique has been used to extract important amenities avaiable in the Airbnb listings. One hot encoding has been used to encode categorical features.
* **Missing value treatment:**
  Missing values were visualized using a heatmap of feature values. The distribution of various features were plotted on histograms and missing value was imputed based on their distributions and data types. Mostly, the numerical features were imputed with mean value and median value and the categorical features were imputed with the mode value.
* **Outlier detection:**
 Outliers were visualized using boxplots. Since, the outliers were mainly leverage points and contained useful information, they weren't removed but the price outliers were transforemd using the quartile range technique to prevent any loss of useful information.
 * **Correlation Analysis:**
  Correlation matrix was visualized to analyse existence of correlation. Since no major value of correlation coefficient existed between the features, no features were removed.

<!-- VISUALIZATIONS-->
## Visualizations
* **Graphical visualizations:** Bar graphs, histograms, heatmap, line chart, boxplots, pie, waffle and donut charts have been used to draw important inferences about the data.
* **Geospatial visualizations:** The density of presence of listings and relative median prices of the neighbourhoods were plotted on the geographical maps of Berlin and Munich to get insights about the geographical density and price distribution of the listings.

<!--CONCLUSION-->
## Conclusion
* Effect of values of various features can be seen on the price of the listing.
* Sharp difference amongst the frequency of particular column values of the features can be noted by examining the visualizations.
* The presence of Airbnb listings is more dense in the centre of Berlin while in Munich the presence of listings is more dense towards the north western side.
* Customers mainly prefer listings hosted by verified hosts and certified superhosts.
* High ratings suggest the presence huge number of fine quality of hostings listed in Airbnb Germany. 

<!--RECOMMENDATION AND FUTURE WORK-->
## Recommendations and Future Work
* The presence of various amenities such as restaurants, hospitals, departmental stores etc. around the listings can also be analysed as it can be a major predictor of price of the listing.
* Appropriate Machine Learning techniques can be used to model a price recommendation system for the host.
