# High Movie's Revinues on Boxoffice

<img src='images/2222.png'>

## Project Overview

This project analyzes data needs by Microsoft Company inorder to help them to create a movie studio and produce a movie that hits the box office.

Descriptive analysis of some movies had achieved high Box office earnings. The outcome data shows three recommandations,Microsoft Company can use this analysis to decide how to produce a successful movie.

### Business Problem

Microsoft has decided to create a movie studio. Microsoft needs to know what factors might impact movie's revenues on the box office.

I am tring to investigate films were doing the best on the box office. 
And find out what factors might impact the movie revinues .
To help Microsoft to produce a movie hits box office.

### The Data Source and Data Exploration

In this project, I work with a Dataset, which can be found in the folder `zippedData` are movie datasets from:

* [Box Office Mojo](https://www.boxofficemojo.com/)
* [IMDB](https://www.imdb.com/)
* [Rotten Tomatoes](https://www.rottentomatoes.com/)
* [TheMovieDB](https://www.themoviedb.org/)
* [The Numbers](https://www.the-numbers.com/)

The dataset which I used inxluded variables about :

1-Movie's Genre and avarage rating per each genre.

2-The production budget and how it can affects the movie's gross.

3- The month which the movie released on and how it impacts the Box office revinues.

Because it was collected from various locations, the different files have different formats. Some are compressed CSV (comma-separated values) or TSV (tab-separated values) files that can be opened using spreadsheet software or `pd.read_csv`, while the data from IMDB is located in a SQLite database.

Methods
We will be able to:

1.Practice connecting to database by using Sqlite3

2.Practice using GROUP BY statements in SQL to apply aggregate functions like COUNT, MAX, MIN, and SUM

3.Practice using the HAVING clause to compare different aggregates

4.Opening and inspecting the contents of CSVs using pandas dataframes

5.Practice identifying and handling missing values

6.Practice joining multiple dataframes

7.Make visualizations using Matplotlib library

Requirements
Load the Data with sqlite3
Load the Data from csv and tvs files and read it as pandas data frame
Create dataframes represent the data.
Use pandas methods to inspect the shape and other attributes of these dataframes.
Perform Data Cleaning (Identify and handle missing values)
Perform Data Aggregation and Join the dataframes together .Identify and handle invalid values
Make visualizations using Matplotlip.


## The first question is: What is the distribution of movie rating by genres?


### Connecting to the Database
Import the necessary libraries, pandas and sqlite3

Establish a connection to the database data.sqlite, called conn

### Viewing the List of Tables

Let's use the cursor to find out what tables are contained in this database. create a cursor.

A cursor object is what can actually execute SQL commands. You create it by calling .cursor() on the connection.
We displayed all the tables that are included in our data base
![movie data erd](https://raw.githubusercontent.com/learn-co-curriculum/dsc-phase-1-project-v2-4/master/movie_data_erd.jpeg)

Note that the above diagram shows ONLY the IMDB data. You will need to look carefully at the features to figure out how the IMDB data relates to the other provided data files.
 we recommend you use only the following data files:

* `im.db.zip`
  * Zipped SQLite database (you will need to unzip then query using SQLite)
  * `movie_basics` and `movie_ratings` tables are most relevant
* `bom.movie_gross.csv.gz`
  * Compressed CSV file (you can open without expanding the file using `pd.read_csv`)
 Acoording to the schema there is a relationship between movie_basics and movie rating ....let us view them. 

### Three Key Factors
Throughout this project, 3 key factors were focused on that can help determine if a movie does well in the box office:

1. Genre of movie
2. Production budget of film
3. The month which the movie released on .

### 1.Genre of movie
The first question is: What is the distribution of movie rating by genres?
For the first factor, I looked at what kind of movie genres were most popular. I used data from an IMDB database which contained over 85,000 movies along with their ratings.
 I looked at which genre had the most movies produced, and which genres had the highest average rating.
The most produced type of movie was in the Documantary ,The highest average movie ratings for a genre belongs to the Game_show.
### 2. Production Budget
The second question is: What is the distribution of Total gross baed on Production gross?
I took a dataset from The Numbers, which contained various movies,their production budget and their domestic and foreign_gross.
Testing correlation between production budget and sumation of both (domestic and foreign_gross) , found a strong positive relationship between them, which suggests that when you pay more on production budget you can earn more on  box office .
### 3. The month that the movie released on
The third question is: What is the distribution of Box_office baed on release time depends on the movie released month?
To answer this question, I examined a data from Box Office Mojo which contained informations about the released date and box office earnings avarage based on spesific month.
I found that the highest box office revinues achived on December during the Chrastmas holiday seasons.



 


### Methods
This project uses descriptive and visual analysis, including description of trends over time. This provides a useful overview of film industry trends, specifically the factors that contribute to increased worldwide gross.

### Results

1. Genre,Rating,Production Budget,and Month of Release are all impact the Box office            revinues posativally.

2. The Game show genre achived highest rating among other genres ,That means this type of       movies can gain more on the box office.

3. The Standard deviation of the observations shows that data are more spread out
   When production budget is high the Std refears that the data sperate above the mean.
   that means the movie with high production budget saparats widly and hits the box office.
4. The month which the movie released on , I noticed that the highest box office revinues 
   reported on the month of December during the Chritmas holiday seasons.   


### Conclusions
This analysis leads to three recommendations for helping Microsoft company to understand the process of producing movies and the factors are affected thier profets.

1.Better prediction of the movie's genres that are likely to have gain more profets.This       modeling could use already available data, such as the avarage of rate per each movie's     genre.

2.The budget needed to produce a sucssussful movie. This modeling could predict the avarage   amount of money need for producing a movie can achieve more profets.

3.Better prediction of the movie's release time at the theaters.This modeling could use       already available data, such as the avarage of box office profets depends on release         month.

### Next Step
1.The movie should contain one of the following genres:
  Game show ,Short ,Reality Tv thos are the movies with  top rate .

2.Pay more attaintion on the Production budget. when the production cost increases the movie
  can sperate widly.

3.Released the movie during the Holiday seasons such like ( Christmas,Easter) holidays on 
  (December,April).

###  Thank you!
Email: mays802004@gmail.com

GitHub: @maysasaad      