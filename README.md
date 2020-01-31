ETL Brief


Project name: ETL
Team: Joao Costa, Kate Vnuk


Purpose of this Document:

This document is intended to provide Instructors with an overview of the Soccer TMS and players ratings. 
An integral part of this project  is to pull, clean and merge the multiple databases for FIFA in order to learn on how we can manipulate with the data and clean it using the following tools:

Tools:
Jupyter
PgAdmin
Datasets
Pandas



Scope:

We decided to pull the data for the National Soccer in order to compare a few data sets for the International transfers costs and  players rating.
The years we are looking at are the 2019-2020.

It also outlines the strategies and technologies  and datasets used as part of the overall ETL project.



Project Plan:

1.	Ratings comparison using the soccer Wiki
2.	Add/merge  the market value of the players to the dataset above (choose top 10)
3.	FIFA rating based on top 10 most highly rated players. (SCRAPING)
4.	Compare the value on the specific game with the TSA values
5.	To identify if the game values are matching or affecting anyhow the TSA values



Datasets:
FIFA 2020 (csv)  https://www.kaggle.com/stefanoleone992/fifa-20-complete-player-dataset
Soccer Wiki data (json) https://en.soccerwiki.org/download.php
TSA (scrape): https://www.transfermarkt.co.uk/
PRACTICAL PART


METHODS DESCRIPTION:
 
 
Using the ETL processes, the following tasks were done:
 
Extract:
 

1)	Extracted  and  scrapped 2020  FIFA datasets
2)	The data were formatted as csv file

Source:

FIFA 2020 (csv)  https://www.kaggle.com/stefanoleone992/fifa-20-complete-player-dataset
Soccer Wiki data (json) https://en.soccerwiki.org/download.php
TSA (scrape): https://www.transfermarkt.co.uk/



        	 
Transform:
1)     Clean Data
a. Used Python Pandas library to load and read the  .csv files.
c. Stored addresses by selecting location 2 column and putting it in a list
 
2)     Merged tables
a. Used fuzzywuzzy library for strings comparison purpose and for the scores for the matching % of the strings in the dataset.
 b.Results were saved as DataFrame
c. Used Python pandas library to convert lists to DataFrame and export it to a csv file
d. Convert the player Market Value from string into integer in order to proceed with data analysis using seaborn plotting.
3)     Build plots
a. The following plots were build using seaborn library:
●	 Preferred players position
●	Market Value vs 1 game value
●	Correlation
●	Regression
●	Potential vs Market Value
●	Market value of players per nation for the top 30 nations
●	Average Rating by Nationality
●	Potential for the top 25 clubs
●	





 
Load:
1) Created SQL connection
2) Exported to MySQL. Since the final output is a DataFrame, we decided to load the data into a relational database.
3) The final database column are as following: 
●	id INT PRIMARY KEY,
●	 name Text,
●	 age INT,
●	 club Text,
●	 overall INT,
●	 potential INT,
●	 game_value INT,
●	 nationality Text,
●	 positionText,
●	 market_value INT


























































