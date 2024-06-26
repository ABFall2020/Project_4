# Project 4:  

Dashboard https://public.tableau.com/app/profile/adriana.pizana/viz/Graduates_17177753789430/Dashboard1?publish=yes

Click on graph by country, marital status, female, Male or age of enrollment to navigate features.

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

Our first task was to clean up the data.  Python code utilized to read in DATA_SET/Raw_Dataset.csv file as pandas dataframe for cleaning before moving to the analysis and graphing process.  Python code was utilized to correct misspell columns and to rename columns with apostrophe and removed unnecesary columns then save to a new csv file DATA_SET/Cleaned_data.csv.  We also created a second file by reading the new DATA_SET/Cleaned_data.csv to append the countries latitude and longitude from https://api.geoapify.com/v1/geocode/search? into a mew data frame.  We merge join left the location data frame with the new dataframe and save it to DATA_SET/CleanedDataWithLocation.csv file for our map visualization.

# Models

We will use Keras-Tuner for predictive modeling in this project.


# Analysis
  1.  Separate the features from the target.

![image](https://github.com/ABFall2020/Project_4/assets/152649998/ff84a27b-2af5-413a-a71b-f75e62e19ee8)
   
  2.  Encode the categorical variable from the features data.

![image](https://github.com/ABFall2020/Project_4/assets/152649998/e9325ce6-dfaa-43ad-a364-75ed50e3bfc3)

![image](https://github.com/ABFall2020/Project_4/assets/152649998/2c1c4d6c-17f8-4ec3-a7a6-826cd885f533)

  3.  Separate the data into training and testing subsets.

![image](https://github.com/ABFall2020/Project_4/assets/152649998/6f6e9ac8-8d28-412b-b6f2-06fa9d85be7b)

  4.  Scale the data using StandardScaler.

![image](https://github.com/ABFall2020/Project_4/assets/152649998/dfc56c05-807d-4085-95ad-8371d9b263c6)

  5.  Create a method that creates a new Sequential model with hyperparameter options.

![image](https://github.com/ABFall2020/Project_4/assets/152649998/d977b8b5-bc85-4959-97b4-7e6c9c711bfc)

  6.  Allow kerastuner to decide which activation function to use in hidden layers.

![image](https://github.com/ABFall2020/Project_4/assets/152649998/0c6a2756-7e45-46b4-8b5a-d43bc0740368)
   
  7.  Allow kerastuner to decide number of hidden layers and neurons in hidden layers.

![image](https://github.com/ABFall2020/Project_4/assets/152649998/b3af6ddf-cd2d-4cb7-8a3e-8c7125875feb)
    
![image](https://github.com/ABFall2020/Project_4/assets/152649998/522d00d1-f1dc-453f-92b2-d8c520fb0bc4)
    
  8.  Compile the model.

![image](https://github.com/ABFall2020/Project_4/assets/152649998/fb1ef502-ef47-475b-8cb7-9081934369af)

  9.  Run the kerastuner search for best hyperparameters.
 
![image](https://github.com/ABFall2020/Project_4/assets/152649998/e2850615-4797-4d14-bc99-8acfb6f2416e)

   * Best hyperparameter elu
      
  10. Accuracy 0.70
  
![image](https://github.com/ABFall2020/Project_4/assets/152649998/21d9a314-dcf7-462e-b241-50029dd4994d)
   

# Visulizations

We will use Tableau's extensive library of visuals to create the visuals for this project.


![image](https://github.com/ABFall2020/Project_4/assets/152649998/767280bb-387a-4fbb-a051-0a35048ab740)

![image](https://github.com/ABFall2020/Project_4/assets/152649998/b34d0d2a-5185-4c38-8d0c-f8b30f49584c)

![image](https://github.com/ABFall2020/Project_4/assets/152649998/c521b318-e9e6-4eb6-a75c-83a64b93b03d)

![image](https://github.com/ABFall2020/Project_4/assets/152649998/7c5495b6-6eed-43b3-abbc-4033f66d0cdc)

![image](https://github.com/ABFall2020/Project_4/assets/152649998/162bb6bf-079f-47d0-925c-0049a44df28b)

![image](https://github.com/ABFall2020/Project_4/assets/152649998/008ce879-e243-48b5-a4b0-27b1037a2d03)

![image](https://github.com/ABFall2020/Project_4/assets/152649998/f8486fbe-f86e-43e0-a8d4-c50d3fb2b6a0)


# Tools Utilized

* Python
* Tableau
* Pandas for data cleanup

# Conclusion

  * Overall conclusion of our project  Single females and Males who enrolled at an average age of 26 we can predict they are at a higher risk to dropout

![image](https://github.com/ABFall2020/Project_4/assets/152649998/b42c93bb-5273-4a9b-9e23-5d81112a9fcb)


  * Limitations
      
      * We were able to find the dataset from kaggle.  However, this was rather small dataset with total of 2,209 graduate studnets, 794 enroll and 1,421 dropout.  Although it had different countries identified, the majority of students were from Portugal.



# Data Source

https://www.kaggle.com/datasets/thedevastator/higher-education-predictors-of-student-retention
