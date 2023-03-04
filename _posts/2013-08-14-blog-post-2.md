---
title: 'Explanatory Data Analysis - Airbnb Data.'
date: 2022-12-26
<!-- permalink: /posts/2013/08/blog-post-2/ -->
tags:
  - Data Analytics
  - Python
  - Airbnb
---

### Problem Formulation

What are the factors, features and amenities that make an Airbnb listing more expensive?

### Motivation

Airbnb has provided many travelers and digital nomads with an easy and convenient way to find a place to stay during their travels. It has also allowed homeowners referred to as hosts., who have listed their properties for the travelers to stay. Given so many listings and varying prices from a wide range. This Analysis aims to find how an aspiring homeowner to know what property facilities to invest in such that he can list on Airbnb and earn a rental income. Many features influence the price of a listing, which is why we aim to find the most important factors that affect the price and list the features that are most common among expensive listings. This will allow an aspiring Airbnb host to ensure that his listing is equipped with the most important features such that he will able to charge the right price with driving away customers. We focus on the physical features and facilities of the property.

### Data Collection

The dataset for this analysis is taken from Kaggle. The dataset is the Airbnb dataset for San Francisco. 
The dataset can be obtained here[]. Data is as of 12/25/2022.

### Data Preparation and Cleaning

Firstly we do a bit of data analysis, to get to know about the data, make changes in the format and also remove the column not necessary for our analysis.

Convert the prices of listings from string to float and remove the '$' sign.

Fill all the Nan values to 0.

Removing the unwanted columns such as listing_url, scrape_id etc.

Cleaning textual data - Amenities to form a textual analysis.

Explanatory Analysis.

We can analyze price concerning 4 different factors.

Room Type

Property Type

Number of Bedrooms

Amenities

Analyzing the listings based on Room Type

As we can observe from the count plot, most of the listings are entire Homes/Apartments. There are almost twice as many Entire Home/Apartments listings as compared to Private rooms. This gives a small insight into the type of Rooms listings available and the number of those for each type.

Analyzing the listings based on Property Type.

From the above plot, we can observe that there are lot more listings of Apartments and houses, compared to other listings of property types in San Francisco. So, with the earlier analysis and this, we can make an inference that hosts prefer to list full property than having just a room or shared room.

Analyzing Prices for different Room and Property types.

From the above heatmap, darker color represents a lower price and a lighter represents a higher price. We can see that shared rooms have a darker color, hence the cheapest. Private rooms have slightly lighter colors so they are in middle, and the entire house is the lightest hence they are expensive listings. We can observe that the highest number of listings which are houses and apartments have similar prices. Hence, we can infer that room_type and property_type both play important roles in the final price of the listing.

Analyses the listings based on the Number of Bedrooms.

From the above plot, we can observe that as the number of listings decreases the number of Bedrooms increases. We can observe that the prices increase as the number of Bedrooms increases. Except for one listing which has 14 rooms. Let's find out why this is the case.

No. Bedrooms : Listings
1.0     3801
2.0     1153
3.0      592
4.0      162
5.0       30
6.0        8
7.0        1
14.0       1
Name: bedrooms, dtype: int64

On further analysis, we observe that there is only 1 listing having 14 bedrooms, so this can be seen as an anomaly and ignored for this analysis. So far, we have observed that room type, property type, and the number of bedrooms have some effect on the price of the listing.

Analysis of listings with specific amenities results in higher prices

We are going to analyze textual data of amenities by finding the words that appear most frequently. We performed the analysis for the top 100 most expensive listings.

From the above wordcload, we can see that the listings with the highest prices have amenities such as Essentials Shampoo, Friendly Workspace, Parking, Laptop Friendly, Hair Dryer and Wifi. Since the data used is from 2020, during the pandemic we can observe amenities having workspaces have high prices.

From the Analysis above, we can infer a few things.

The type of room for listing has a greater influence on the price. Most hosts list their entire property. The entire property is on the most expensive list.

Property type also influences the price. As mentioned in the previous one, listing the entire property fetches a higher price for the hosts.

The number of Bedrooms in the listing has a trend with the price of the listing. More the rooms, the higher the price for that listing.

We also observe that type of Amenities plays an important role in the listing price. Essentials Shampoo, Friendly Workspace, Parking, Laptop Friendly, Hair Dryer and Wifi are the amenities most, expensive listings provide.

Technology and Packages Used.

Python

Pandas

Plotly

Python NLTK

You can find the code here

I plan to do further analysis on how particular Location influences the price, that another blog post. Stay Tuned.

Copyright of the Airbnb logo belongs to Airbnb. This is just an educational project.
