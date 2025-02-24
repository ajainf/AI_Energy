# AI_Energy

This repository holds my projects for the AI for Energy MIT IAP Class 2025.

## HW1 - Database, document and information Summarizer

For HW1 I created an Explorer of State Incentives for Renewables and Energy Efficiency. I wanted to leverage the DSIRE database which I downloaded as a json file, converted to a csv and used the Stack AI Table + Search. To query the Table, I use the GPT4 LLM which then creates a smaller queried table and I used a 2nd LLM to provide recommendations, group information and find relevant links so a user can sign up for renewable and energy efficiency programs.  
The link to the app is here:
https://www.stack-ai.com/form/ac72067d-4aef-4716-a438-e7ecdf656bda/66b4a132-af4f-41a4-9c34-e4bb8406f96f/678458d2dc11aaa4b0dc2a74

The repository holds the slides.

## HW2 - Prediction from Features

For HW2 I used google Colab and the xgboost algorithm to predict energy use (in KWh) from other features available in the public EIA Residential Energy Consumption (RECS) data for 2020. The best model had an R2 of 0.6 so it still requires improvement. The RECS data is collected every 5 years so it could be used for coarse timeseries analysis but may not be sufficient.

The repository holds the Colab notebook and data.


## HW3 - Image Classification

For HW3, I used teachable machine https://teachablemachine.withgoogle.com/models/DeZg0Fdf9/ to train a tensor flow model that could classify building facade image into those that have a window AC unit and those that do not. There are several service that can provide thousands of images of building facades, but I was not able to find ones with AC window units so I decided to get my own data. I obtained about 30 images from Google Earth's street View by virtually "strolling" through different neighborhoods and print-screening images that I then manually labelled. I used 20 images to train which means this is quite a sparse data (recommended is 50 images per class). Nonetheless, the classifier did fairly well in discerning images with and without AC, although in testing the remaining 10 images it did misclassified some images. I think this type of classifier could be coupled with other information (building age, thermal heat, energy use) to start to get a sense of the housing stock quality and energy use efficiency of homes.

The repository holds the slides.


## Capstone - Geospatial and tabular data

For the capstone, my partner and I built an AI/ML model in Google CoLab that predicts Building Energy Star Scores (a measure of energy efficiency). The building sector accounts for over a third of GHG emissions worldwide so efficiency improvements can make a difference.

Since Energy Star Score data is limited, we explored combining the available data with satellite thermal data in order to allow estimating the scores in other areas. To obtain the satellite imagery signals, we used Google Earth Engine. We combined land surface temperatures, building energy use information, and building footprints and used an ensemble gradient boosting (xgboost) regression to create a model. Although the model still needs refining, we made some progress and learned a lot about the predictive variables of Energy Star Scores.


The repository holds the codes in 3 parts, the data and the slides.

