# ProgrammingProjectNOV2019
Repository for the Project for the programming for data analytics November 2019.

## Introduction
The aim of the Programming for data analytics project for 2019 is to:

1. create a dataset by simulating a real-world phenomenon which
        *must be able to be measured
        *have collected >100 data points over 4 variables
        *investigate type of variables, distributions, relationships with each other
2. Model and synthesise data using the Python numpy.random package
3. synthesise/simulate dataset matching their properties as possible
4. Detail research and implement the simulation in this notebook
For this project I will use my experience in the pharmaceutical industry to investigate a real-life dataset for the distribution types and relationships between the variables. I will then use this knowledge to simulate a data with five variables with specific specification ranges, distributions and shapes. This data will be outputted as a dataframe which can create plots. A number of Python libraries will be used in this project.

## Conclusion
The aim if this project was to generate a dataset of at least 4 different variables. I decided to work on a real-life example of data I am currently working on based on the QBD principle which is important in the pharmaceutical industry.

I began by understanding the key variables of the real-life data set including the specification ranges, mean and standard deviations, and the distribution of the data. There were five key variables all were normally distributed except for one variable which was Poisson distributed.

I was able to develop code which would generate random data based on my specific requirements (e.g. mean, standard deviation, specification range and distribution). This was proven when displayed as histograms.

I tried to combine these codes into a dataframe but was not successful. I made numerous attempts which I detail in this report after many research attempts. Unfortunately, I was not successful in time to complete this assignment.


## Commit History and Explanation

### 1. 30November2019
Creation of the Jupyter notebook and began preparing for the project.

### 2. 01Dec2019
Introduction to the QBD concept. Understanding which parameters will be simulated for the project.

### 3. 02Dec2019
Explanation of my real-life dataset. Imported required Python libraries.

### 4. 03Dec
Quick overview of project

### 5. 04DEC
Explained the theory of Cream consistency measurement and hte various inputs which impact cream consistency result. References were added. 

### 6. 05 Dec 1
Provide more of a background on my required dataset inclduing the distribution types.

### 7. 05Dec 2
Discussed some code to develop normally distributed data of a specific mean and standard deviation. I also tried to write code to make the data more accurate eg having a long tail or truncated tail as per this reference: https://machinelearningmastery.com/how-to-transform-data-to-fit-the-normal-distribution/

### 8. 07Dec
Continued working on the code to create long tail code for the LOD data. Devloped code to create a tail of 10 values. Need to look at ensuring it appends at the 1.0% which is the specification limit for this raw material.

### 9. 08Dec
adjusted LOD results to ensure data was below the NMT 1% specification limit. Remaining datasets were created using similar code.

### 10. 08Dec2
Finalised Poisson distribution for number of pH adjustments per batch ensuring specification limit of no more than 5 pH adjustments are performed per batch.

### 11. 08Dec3
Finalised all datasets and some formatting of the notebook. Researched how to create interactions between the simulated data.

### 12. 09Dec19
Performed some web research on characteristic relationships

### 13. 11Dec2019
Looked into sqlite to combine random variables into one table. Was able to create a dataframe for two variables. Will look and continuing this for other variables.

### 14. 11Dec2019 1
Used dataframe code to create a dataframe using all variables which worked. But i wasn't able to to create plots of the data frame. i will also look more in depth into using the SQlite library. After this i can look at the relationship of the variables using KNN (lecture notes week 6).

### 15. 12Dec2019 
Realised that the dataframe is code i'm using creates the data =frame with one row rather than 150 as resquired. ie 
     df = pd.DataFrame({
             'pH': [np.random.normal(5.9, 0.16, 150)],
             'assay' : [np.random.normal(13.9, 0.525, 150)],
             'visc': [np.random.normal(15671, 590.325, 150)], 
             'pHevents': [np.random.poisson(1, 150)],
             'LOD': [append(LOD, tail)],
            })
     print(df)
     df
this is probably due to how i've written the code. It might be easier to name them in the df code rather than write them like this. That will be next attempt.

### 16. 13Dec2019
Tried a few more things to fix the code. Another web search pulled up some more options to pursue. I'll start these tomorrow.
https://www.mssqltips.com/sqlservertip/6120/data-exploration-with-python-and-sql-server-using-jupyter-notebooks/
https://jakevdp.github.io/PythonDataScienceHandbook/03.07-merge-and-join.html
https://www.learndatasci.com/tutorials/python-pandas-tutorial-complete-introduction-for-beginners/

### 17. 14Dec2019
Tried again to fix codes. I was able to create the index as dates. Wheni put it into the code it gives me 150 data points for each date index. Perhaps i have the number of random number to create as one then look at creating this 150 times it might work?
 
### 18. 14DEC2019 1
looked at the relationships and distributions in my real data via histogram and scatterplots.
Confirmed my dataset is giving 150 datapoints per row using <df.tail()>, <df.head()> and <len(df)>. I tried again with the code below (https://www.learndatasci.com/tutorials/python-pandas-tutorial-complete-introduction-for-beginners/):
     data = {
         'LOD': [LOD], 
         'pH': [pH]
     }
     purchases = pd.DataFrame(data)
     purchases

### 19. 15Dec2019
Tidied up the notebook, Added more explanation of my real-life data including the relationships between the variables and the distributions. I also discussed my issues creating the dataset from the generated simulated variables and the different codes i have tried. 

### 20. 16Dec2019
Tried another route to creating the dataset. Unfortunately it did not work again. I wrote the conclusion and finalised the report with all my many attempts.
     
     
     









