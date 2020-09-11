Team-17-Azubi-Africa-Hackathon
# DOCUMENTATION
This project is solely about using some specific and environmental indicators to predict the percentage of an area that will get burnt in the case of a fire outbreak.
The various steps we used are elaborated more in the Team-17-Report.docx which is the main report. The various processes used in the .ipynb file is commented to give an overview of all that was involved in the process. The main process used in the .ipynb file are: 
1. Understanding The Data
2. Cleaning The Data
3. Featurization
4. Azure
## Understanding The Data
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
33. 







