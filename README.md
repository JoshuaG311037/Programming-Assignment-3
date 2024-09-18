# Programming-Assignment-3

## In the given Programming Assignment we were tasked to create a code using pandas

# In the first part of the assignment we were tasked to:
### - Load the corresponding .csv file into a data frame named cars using pandas.
### - Display the the first five and last five rows of the resulting cars. 

# #3.1 Load the correspoding .cvs file into a data frame named cars using pandas.

In order to do this task first is to input:

## [1] import pandas as pd

So that we would be able to use the different syntaxes that it offers.

Then using the code:

## cars = pd.read_csv('cars.csv')

This would put the .csv file into a data frame in order to extracts its elements.

# #3.1 Display the first five and last five rows of the resulting pandas. 

In order to perform the task we would need to utilize the code:

## .head() and .tail()

Using the code *cars.head(10)* I was able to extract the first 10 rows of the given data frame.

Then using the code *cars.tail(10) I was able to extract, starting from the last row, the 10 last rows of the given data frame.

## What I learned

### I learned that if I want to extract the data of a .csv file then I would need to use the code .read_csv("name of the .csv"). And in order for me to extract either the first couple or last couple of rows, I would need to use the code .head("number of rows from the first row") and .tail("number of rows from the last row") in order to output the specific amount of rows that I want. 

# In the second part of the assignment we were tasked to:
## - Display the first five rows  with odd numbered columns in the given data frame cars
## - Display the row that contains the 'Model' of 'Mazda RX4'
## - Determine how many cylinders ('cyl') does the car model 'CamaroZ28' have
## - Determine how many cylinders ('cyl') and what gear type ('gear') do the car models 'Mazda RX4 Wag', 'Ford Pantera L', and 'Honda Civic' have.

# #3.2 Display the first five rows with odd numbered columns in the given data frame 'cars'

In order to do this task I used the code:

## .iloc()

So that I would be able to input the specific indexes that I want to output. Simply inputing the code:

## cars.iloc[[0,1,2,3,4],[1,3,5,7,9,11]]

With the values in the first bracket indicating the specific rows that I want to output and the second bracket has all the odd numbered columns that I want to output. I also noticed that since the code is zero based indexing, the 'Model' column which is supposed to be the first column did not output because the first index is 0.

# #3.2 Display the row that contains the 'Model' of 'Mazda RX4'

For this part of the assignment I used the code:

## .loc()

To be able to access the row containing the specific 'Model' I used the code:

## cars.loc[cars['Model']=='Mazda RX4']

This line of code would then output the location of the model by finding from the column of 'Model' the name 'Mazda RX4' and would output all of the columns associated with it.

# #3.2 Determine how many cylinders ('cyl') does the car model 'CamaroZ28' have

For this task I needed to output a specific column from a specific row, therefore I would need to use the code I used earlier "cars.loc[cars['Model']=='Mazda RX4']" and add some conditions to it so that it would output what I need.

So first is to rwrite the code to:

## cars.loc[cars['Model']=='Camaro Z28']

This code would then locate the row that contains the model 'Camaro Z28' from the 'Model' column. Then I would add another index [cyl] which would output specifically the coulumn of 'cyl'. The final code would look like this:

## cars.loc[(cars['Model']=='Camaro Z28'),['cyl']]

The output of this code was 8, therefore the number of cylinder that the model 'Camaro Z28' has is 8

# #3.2 Determine how many cylinders ('cyl') and what gear type ('gear') do the car models 'Mazda RX4 Wag', 'Ford Pantera L', and 'Honda Civic' have.

For this task I need to find the values of 'cyl' and 'gear' for the models 'Mazda RX4 Wag', 'Ford Pantera L', and 'Honda Civic'. In order to do that I just reused the code from the previous task and added more conditions to it so that it would out put the 'Model', 'cyl', and 'gear' of the specific cars. The final code looks like this:

## m = cars.loc[cars['Model'] == 'Mazda RX4 Wag', ['Model','cyl','gear']]
## f = cars.loc[cars['Model'] == 'Ford Pantera L', ['Model','cyl', 'gear']]
## h = cars.loc[cars['Model'] == 'Honda Civic',['Model','cyl','gear']]
## print (m)
## print (h)
## print (f)

With this code it was able to output the different values of the models:

###  For the 'Mazda RX4 Wag' it has 6 cylinders and 4 gears
###  For the 'Ford Pantera L' it has 8 cylinders and 5 gears
###  For the 'Honda Civic' it has 4 cylinders and 4 gears

## What I learned

### After doing this task I was able to utilize the different ways to extract the rows and columns from a given data frame. Using .iloc() I inputed the indexes that I need so that it would output what I need, and .loc() which is a more flexible way of finding specific elements as you only need the column name and element under that column to extract the data that you need from it. 




