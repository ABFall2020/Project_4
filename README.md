# Project 4:  
For this project, we were tasked with finding a problem worth solving, analyzing or visualizing
using machine learning with the technologies we have learned.

# Project Proposal

Project Title:

Predictive Model of Student Dropout Rates

Team Members:

Esteban Quintanilla, Karina Gonzalez, Adriana Pizana, Mallory Olajide

Project Description:

The goal of this project is to use certain variables that can contribute towards the likelihood of
that student dropping out of their undergraduate degree plans. Some of these variables will
include Gender, Marital Status, Nationality, Scholarship holder, Age at enrollment, etc

Rough Breakdown of Tasks:

 * Clean up of dataset
 * Create graphs for the following:
   * Students by country
   * Students martital status (Married, Single)
   * Students age
   * Students by gender
   * Total of students (Dropout, Enrolled and Graduated)

# Process

Our group leveraged the activites we have learned so far throughout the boot camp.  From reading csv file, data clean up, to visualization using bar charts, pie charts, chart and map, handling missing values, encoding categorical variables, normalizing numerical features and splitting the data into training and testing sets.  Dependencies leveraged for code:  Python, Pandas, numpy, pathlib, seaborn, matplotlib.pyplot, tensorflow, StandardScaler, train_test_split, os, balanced_accuracy_score, confusion_matrix, keras_tuner, Classification_report.

Our first task was to clean up the data.  Python code utilized to read in DATA_SET/Raw_Dataset.csv file as pandas dataframe for cleaning before moving to the analysis and graphing process.  Python code was utilized to correct miss pell columns and to rename columns with apostrophe and removed unnecesary columns then save to a new csv file DATA_SET/Cleaned_data.csv.  We also created a second file by reading the new DATA_SET/Cleaned_data.csv to add the countries latitude and longitude using https://api.geoapify.com/v1/geocode/search? into a location data frame.  We merge the location data frame with the new dataframe and save it to DATA_SET/CleanedDataWithLocation.csv file.

# Analysis
We had to review the new data frame, data types, unique values and check the category for our Targets column. We had to convert the target columns from graduate, enroll and dropout to numeric with get dummies, checked the balance of out target values

# Models

We will use Keras-Tuner for predictive modeling in this project.


# Visulizations

We will use Tableau's extensive library of visuals to create the visuals for this project.


# Tools Utilized

* Python
* Tableau
* Pandas for data cleanup

# Data Source

https://www.kaggle.com/datasets/thedevastator/higher-education-predictors-of-student-retention
