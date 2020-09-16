Team-17-Azubi-Africa-Hackathon
# DOCUMENTATION ON DR CONGO FIRES
Main aim of our predictive module is to find the percentage area that will get burnt in case of a fire outbreak. This project is solely about using some specific and environmental indicators to predict the percentage of an area that will get burnt in the case of a fire outbreak. The various steps we used are elaborated more in the Team-17-Report.docx which is the main report. The various processes used in the .ipynb file is commented to give an overview of all that was involved in the process. The main process used in the .ipynb file are: 
1. Understanding The Data And Cleaning
2. Feature Engineering And Vizualizations
3. Azure
## Understanding The Data And Cleaning
The whole idea of this process is to get an overview of the data and all that it entails. This was done uses various python libraries such as Pandas, Numpy, MissingNo, and many others. The various methods used in this particular broad process includes the following:
1. Imported the need libraries which are;  numpy as np, pandas as pd, collections, matplotlib.pyplot as plt, missingno as msno, and scipy.stats as st. 
2. Read the data with the read_csv method of pandas which loaded the csv file of our train dataset into a Pandas Dataframe and stored it in the variable train.
3. Showed the first 5 rows by calling the head method on the Pandas Dataframe we named train. 
4. Called the describe method on train to give description of the data.
5. Called the info function on train to give an information about the data.
6. Used the isnull().sum() on train to check the total count of null values availabe.
7. The shape method on train was used to get the dimensions of the dataset.
8. The index method on train used to the start and end of the rows of the train dataset
9. The skew function on train to check the skewness of the dataset
10. The kurt function on train to check the kurtosis of the dataset.
11. Run a for loop of all the columns of the dataset and found the mean of it and printed it as a percentage
12. Called the bar function of msno and sampled 626644 to give a graph of the missing values of each column which was only population_density
13. Checked for duplication by calling the drop method on the train dataset in order to drop the ID column to check for duplications
14. Called the mean, median, max and isnull function on the population density column of the train dataset
15. Read the test dataset by calling the read_csv method of pandas and stored the data in a variable called test
16. Called the describe method on test to show the description
17. Called the shape method to see the dimensionality of the dataset.
18. Called the index to see the start and end of the test dataset
19. Called the head method to see the first 5 rows of the test dataset
20. Called the tail method to see the first 5 rows of the test dataset
21. Called the info function on the test dataset to get information on the dataset.
22. Called the isnull().sum() function to known the total counts on null values in each column which was the population_density column only
23. Run a for loop of all the columns of the test dataset and found the mean of it and printed it as a percentage
24. The skew function on test to check the skewness of the dataset
25. The kurt function on train to check the kurtosis of the dataset.
26. Called the bar function of msno and sampled 10000 to give a graph of the missing values of each column which was only population_density
27. Checked for duplication by calling the drop method on the test dataset in order to drop the ID column to check for duplications
28. Added new columns(month, year) to both train and test dataset
29. Showed the first 5 rows by calling the head method on train dataset.
30. Showed the last 5 rows by calling the head method on train dataset.
31. Showed the first 5 rows by calling the head method on test dataset.
32. Showed the first 5 rows by calling the head method on test dataset.
33. Called the value_counts on the year column of the train dataset to give the total number of counts of each year.
34. Called the value_counts on the year column of the test dataset to give the total number of counts of each year.
35. Called the loc function on train data to find the total number of actual fires by setting burn_area to be greater than 0
36. Found the total of actual fires in train by running the function values_counts
37. Called the loc function on test data to find the total number of no fires by setting burn_area equal to 0
38. Found the total of no fires in test by running the function values_counts

## Feature Engineering And Visualization
Feature engineering helps the predictive model to predict better. It seeks to establish a relationship between the various columns of the data to facilitate a higher predictive power. The various methods used include:
1. Created a new column called burnt which determines whether an area gets burnt on not based on the burn_area column which gives the percentage of area burnt. So run a for loop so that if i > 0 then area got burnt hence 1 else 0 for the train dataset.
2. Showed the first 5 rows by calling the head method of the train dataset.
3. Created a new column called burnt which determines whether an area gets burnt on not based on the burn_area column which gives the percentage of area burnt. So run a for loop so that if i > 0 then area got burnt hence 1 else 0 for the test dataset.
4. Showed the first 5 rows by calling the head method of the test dataset.
5. Showed the last 5 rows by calling the tail method of the test dataset.
6. Added new columns known as dry_and_windy, hot_and_dry, low_pres_and_rain_def, and pres_def_and_windy using arithmetic operations on some particular columns.
7. Checked the correlation between the various columns and the target column known as burn_area for train dataset
8. Showed the first 5 rows by calling the head method on train dataset.
9. Showed the last 5 rows by calling the head method on train dataset.
10. Called the shape method on train to see the new number of rows and columns
11. Called the shape method on test to see the new number of rows and columns
12. Showed the total counts for each year in train dataset in ascending order.
13. Checked actual fires of the feature engineered train by running the loc function and setting burnt to be greater than 0
14. Run the shape function on actual fires to see the dimenstionality
15. Visualized a horizontal graph of the actual fires in each year in ascending order by running value_counts().sort_values().plot() function on it.
16. Run value_counts().sort_values() on the year column of the actual fires data to see how much that occur in each year.
17. Visualized a bar graph of the total counts of the train month column in ascending order by running value_counts().sort_values().plot() function on it.
18. Combined the test and train dataset by and gave each row from each dataset a unique indentifier. 0 for train and 1 for test in a column called separator. 
19. Called the loc function on train data to find the total number of rows were climate_swe was 0. 
20. Showed the first 5 rows by calling the head method on the Pandas Dataframe we named train. 
21. Called the drop function to now drop the separator column added to the feature engineered dataset
22. Created a CSV file called new_train using the feature engineered train dataset. This dataset was sent to Azure for further analysis. 
23. Run the describe method on all the distinct values of the year column of the train set for further analysis
24. Created a CSV file called new_test using the feature engineered test dataset. This dataset was sent to Azure for further analysis and inferencing

## Azure
1. The new_train data was sent to Microsoft Azure to be used to train the Decision Forest Regression Model.
2. The new_test was used inferencing after the pipeline of the model was deploy.



