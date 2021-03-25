# Game App Analysis

## Presentation

-Selected topic:

Our group decided to look at phone app data, targeting specifically on games and see what features are drivers to success.

-Reason for selected the topic:

The reason we chose this topic is because we were interested to utilize the things we learned into real life application and were generally interested in how ratings for phone apps come about.

-Description of the source of data:

Our data is from Kaggle, where the source was obtained through scraping of millions of Android smartphone logs & app metadata.

Source data: https://www.kaggle.com/kboghe/android-apps-metadata

-Questions hope to be answered with the data:

Through this project, we are hoping to find out what are the main features that cause a game app to succeed/fail which can be approximated by its ratings by users. We will first preprocess the given dataset that will then be put through a machine learning algorithim to help build a model that will determine a game app's rating. A successful model will allow for real life application where mobile game creators can use this to tune their game for greater chance of success e.g. if having games free is a factor in determining higher game rating, then creators should reconsider their pricing strategies.

-Progress so far:

To date, we have successfully preprocessed the given dataset and able to run a simple machine learning algorithim to predict game app rating based on various features as defined.

## Database/Pre-Processing

Progress so far:

-Removed extra columns that we felt weren't necessary
-Transformed a number of rows on number reviews column, where some numerical values are objects and were transformed accordingly
-Removed erroneous rows on numer reviews columns i.e. objects
-Removed rows where number reviews is less than 1,000, as ratings may not be reflective with lower reviews (still debating about)
-Export file as csv

Plans:

-On main table, group metrics into a discrete variable from 0 to 5... may need to round ratings data
-Create separate table grouped by company
	-count of # of unique games made 
		-> make variable of experienced (1<) vs unexperienced (1)
	-count of total downloads 
		-> use clustering to figure out best fit groups for size i.e. small/med/larg
	-Export as separate csv
	-Normalization of data
	-Export tables to sql, use query to join the two tables	

## Machine Learning

Progress so far:

-Removed extra columns that are not needed for machine learning
-Encoded categorical columns
-Ran linear regression analysis and obtained r^2 accuracy
-Ran p-values off linear regression


Plans:

-Add additional features and run model
-Should run logistical instead of linear model
-Use supervised learning to compute produce model e.g. random forest
-Use neural network to produce better model due to complexity of features

## GitHub Structure/Communication Protocol

Main Branch 
	-Only merged with development folders that have been reviewed and acts as a 'final' submission
	-Is updated by by different development folders

Development Branch
	-Merged from sub-branches as defined by drawing, intended to be compiled work prior to review
	-Develop branch can be also updated from segment related changes (if any)
	-Contains all planning/notes made during the development
	-Create separate development branches based on weekly submissions

Preprocessing Branch
	-Contains all preprocessing & query related code for analysis/cleaning done on dataset 
	-Completion of branch is merged to development branch upon collaborative review
	-Can be merged from feature branches pending collaborative review

Analysis Branch
	-Contains all machine learning related analysis code done given preprocessed data given from latest development update
	-Completion of branch is merged to development branch upon collaborative review
	-Can be merged from feature branches pending collaborative review

Presentation/Planning Branch
	-Contains all presentation related material including tableau presentation, google slides, and project explanations
	-Completion of branch is merged to development branch
	
Feature Branch
	-Contains any additional features members would like to add to existing code prior to collaboration session
	-These features will be reviewed collaboratively during session and merged with their respective branches

A drawing of GitHub structure shown below:

<img src='GitHub Structure.png'>

