# MetisEDA
EDA project for Metis Bootcamp

## Abstract

The goal of this project was to explore MTA ridership data in order to a) determine where and when to poll users of the NYC mass transit system as to their degree of support for minor fare increases to generate funding for youth extracurricular programming. I used [MTA's turnstile data](http://web.mta.info/developers/turnstile.html) and [spatial data regarding boroughs and station geometry](https://opendata.cityofnewyork.us/data/), applying Pandas for cleaning and exploring the data, and Seaborn to generate plots.

## Design 

This project originates from [GrowNYC's](https://www.grownyc.org/education) ongoing initiatives to connect urban youth to the natural world. There is a lot of data to support the results of environmentally-focused restorative justice and educational programs as an effective pathway to healthier communities and reduced levels of poverty. Here, GrowNYC seeks to establish a publicly-funded program to provide underserved NYC youth with access (via MTA) to the various ecological systems found throughout New York City, as well as the staffing means to educate these children on issues of sustainability, sense of place, and belonging in outdoor spaces. Effective exploration of MTA's turnstile data will help GrowNYC to determine how to proceed with probing what support for programs of this nature currently exists in the community, as well as "back of the envelope" calculations for the funds that fee increases may make available for this purpose.

## Data

Three months (Summer, 2021) of MTA's turnstile data was used, consisting of 2,724,418 rows across 11 columns. These columns provide entry and exit counts from each station, utilizing columnar combinations of control authority, turnstile unit, scanning point, and station; the subway linename, division, date, and time (4-hour intervals) are also included.

The boroughs data includes five simple shapefiles outlining the boundaries of each city borough. Spatial data with latitude and longitude geometry for 473 stations was also used.

The vast majority of the turnstile data was grouped in such a way as to show the average entrance counts for all MTA stations across the summer of 2021; this grouping was then viewed in a variety of lenses (such as by weekday aggregations). From this grouping, the 20 busiest (on average) stations were selected for a more in-depth analysis.

## Algorithms

Data was ingested into a SQL database with the provided .py script, and explored at a high level. Utilizing Python (Pandas), a variety of methods, groupings, aggregations, and calcuations were applied to extract numerical insights from the data, in addition to creating visualizations.

## Tools

* Metis graciously provided a python script for initially gathering the massive amount of MTA data onto the local machine. This data was saved as a SQL database and imported into the project workspace with SQLAlchemy.

* Within Jupyter Notebook, small functions were used to import MTA data directly.

* Pandas was leveraged (heavily) to clean, organize, and merge datasets for the purposes of analysis and plotting.

* Seaborn and Geopandas were used to generate plots of the cleaned data.

## Communication

In addition to the live presentation (13 October 2021, 6:00pm MST) and slides, this project will be continuously available on [my GitHub](https://github.com/medrich/MetisEDA). With the conclusion of this course, I will be revisiting this project when I have more proficiency with the tools at hand, and more time in which to use them.


