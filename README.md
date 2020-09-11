Team-17-Azubi-Africa-Hackathon
# DOCUMENTATION
This project is solely about using some specific and environmental indicators to predict the percentage of an area that will get burnt in the case of a fire outbreak.
The various steps we used are elaborated more in the Team-17-Report.docx. The various processes used in the .ipynb file is commented to give an overview of all that was involved in the process. The main process used in the .ipynb file are: 
1. Understanding The Data
2. Cleaning The Data
3. Featurization
4. Azure
## Understanding The Data
The whole idea of this process is to get an overview of the data and all that it entails. This was done uses various python libraries such as Pandas, Numpy, MissingNo, and many others. The various methods used in this particular broad process includes the following:
1. Imported the need libraries which are;  numpy as np, pandas as pd, collections, matplotlib.pyplot as plt, missingno as msno, and scipy.stats as st. 
2. Read the data with the read_csv method of pandas which loaded the csv file of our train dataset into a Pandas Dataframe and stored it in the variable train.
3. Showed the first 5 road by calling the head method on the Pandas Dataframe we named train. 
4. Called the describe method on train to give description of the data.
5. Called the info function on train to give an information about the data.
6. Used the isnull().sum() on train to check the total count of null values availabe.
7. 
