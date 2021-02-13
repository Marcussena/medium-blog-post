# medium-blog-post
Addtional information regarding a medium blog post

# Write a Data Science blog post on Medium
This project is part of the Data Science nano degree program from Udacity. The post can be found here: https://marcusmvls-vinicius.medium.com/5-thoughts-about-airbnb-in-seattle-1de5dc9b2a73

# Introduction
As motivation to write my post I used a dataset about AirBNB of Seattle available on Kaggle here: https://www.kaggle.com/airbnb/seattle/data. The objective was to answer the following 5 questions by analyzing, cleaning, modeling and creating visualizations to back hypothesis and reach conclusions.

 #### Q1 — What season is less/more available?
 #### Q2 — Which neighbourhoods are more/less expensive?
 #### Q3 — What locations have the best ratings?
 #### Q4 — What is the relationship between prices and review scores?
 #### Q5 — What season is more expensive?
 
 # Environment
 I used Python 3 in a Jupyter notebook to coding, modeling, cleaning and creating plots that lead me to the conclusions of my post. The libraries that I used were:
 
   1. Pandas
   2. Numpy
   3. Matplotlib
   4. Statsmodels
   
 # File description
   a. archive.zip - zipped folder containing three datasets used in this work (calendar.csv, listings.csv, reviews.csv)
   b. seattledataset.ipynb - jupyter notebook explaining the code used to achieve the result and visualizations showed in the post
   
 # Methodology
 ## CRISP-DM process
In order to assess the questions raised, I will be using the Cross Industry Standard Process for Data Mining (CRISP-DM). This process will guide me through the phases needed to find useful answers and involves the following 6 steps:

- Business Understanding
- Data Understanding
- Data Preparation
- Modeling
- Evaluation
- Deployment

As follows, it will be presented more details about each step and how it will be used along the process of answering the questions.

## Business Understanding
Acording to Business Model Toolbox website:

*Airbnb is a community-based, two-sided online platform that facilitates the process of booking private living spaces for travelers. On the one side it enables owners to list their space and earn rental money. On the other side it provides travelers easy access to renting private homes. With over 1,500,000 listings in 34,000 cities and 190 countries, its wide coverage enables travelers to rent private homes all over the world. Personal profiles as well as a rating and reviewing system provide information about the host and what is on offer. Vice versa, hosts can choose on their own who to rent out their space to.*

Understending the relations between the two parts that benefit from the platform (owners and travelers) helped me to raise hypothesis like the relation between prices, availability and review scores, for example

## Data Understanding
The dataset available is composed by three files about homestays of AirBNB of Seattle, WA:

- listings: including full descriptions and average review score
- calendar: including listing id and the price and availability for that day
- reviews: including unique id for each reviewer and detailed comments

## Data Preparation
After the different table of the dataset are identified, it was possible determine the actions needed to prepare the data for modeling. The preparation actions performed are as follows:
- Replacing 't' and 'f' values on the available column of the calendar table
- Dropping the "$" sign on the price column of the listings table
- Changing the format of prices from '1,250.00' to '1250.00' and changing its type to float
- Dropping missing values of the review_score_values column of the listings table
- Drop some outliers prices and review_scores of the listings table
The reason of each data preparation action will be explained in the answer of each question.

## Modelling and Evaluation
To answer the questions it was used the pandas library to group the data by each attribute of interest after cleaned and prepared. After, the resulting groupby was used to create visualizations that, after interpretation, helped me to draw conclusions. 
In question 1, for example, after the graph of availability along the year was plotted, I consulted a Seattle travel guide to understand possible reasons for the sudden drops in availability.
For question 4, I used the statsmodel package to draw a line through the data using the Ordinary Least Squares method to find the relationship between prices and review scores.
Each groupby and the linear regression model performed was backed with graphs to help explaining my conclusions.

## Deployment
seattledataset.ipynb - jupyter notebook explaining the code used to achieve the result and visualizations showed in the post

   
 # Reference
   1. Tips and reference for the general structure of the post: https://medium.com/@AbdulazizKTA/write-a-data-science-blog-post-f8c5e1ece761
   2. Insight for how to clean and model the data to answer my questions: https://www.kaggle.com/ikhlaszineddine2103/airbnb-project
   3. Writing tips and techniques: https://towardsdatascience.com/how-i-write-a-data-science-blog-62e4108fe478
   4. Source and details about the datasets used on the analysis: https://www.kaggle.com/airbnb/seattle
   5. Holidays, Celebrations and travel guide of Seattle, WA: https://santorinidave.com/best-time-to-visit-seattle
   
 
