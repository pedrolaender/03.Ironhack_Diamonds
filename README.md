<p align="center">
  <img src="https://github.com/pedrolaender/03.Ironhack_Diamonds/blob/main/images/00.%20diamonds.jpg?raw=true" />
</p>

# Diamonds

  Project Completed
## Abstract

  This project has the objective to make a Linear Regression Model on a diamonds features and price dataset in order to make a prediction of the price of other diamonds dataset containing only the features. The goal for this project is to achieve a Root Mean Sqarred Error (RMSE) < 900.
## Introduction

### Technologies 

  - Python

### Methods

  - Filtering
  - Grouping
  - Visualization
  - Linear Regression
  - Random Forest Regression


### Libraries

  - Pandas
  - Numpy
  - Matplotlib
  - Seaborn
  - Sklear

## Project Description

  First of all it was necessary to understand the data. We have a DataFrame where each row represents one diamond and 10 columns, 9 of them being features and 1 the price, the target variable.

  Description of the data:

| Column  | Description  |
|---|---|
| Price  | Price in US dollars (326-18,823)  |
| Carat  | Weight of the diamond (0.2--5.01)  |
| Cut  | Quality of the cut (Fair, Good, Very Good, Premium, Ideal)  |
| Color  | Diamond colour, from J (worst) to D (best)  |
| Clarity  | A measurement of how clear the diamond is (I1 (worst), SI2, SI1, VS2, VS1, VVS2, VVS1, IF (best))   |
| x  | Length in mm (0--10.74)  |
| y  | Width in mm (0--58.9)  |
| z  | Depth in mm (0--31.8)  |
| Depth  | Total depth percentage = z / mean(x, y) = 2 * z / (x + y) (43--79)  |
| Table  | Width of top of diamond relative to widest point (43--95)  |

![image](https://github.com/pedrolaender/03.Ironhack_Diamonds/blob/main/images/01.%20understanding.PNG?raw=true)

  The next step is to get some statistics about the data. We get this by using "describe()" method.

![image](https://github.com/pedrolaender/03.Ironhack_Diamonds/blob/main/images/02.%20describe().PNG?raw=true)

  Now the data must be clean. In this step we transformed the categorical data (Clarity, Color and Cut) into numerical according to specifications of the challenge. It had to be done because Linear Regression cannot work with categorical data.

![image](https://github.com/pedrolaender/03.Ironhack_Diamonds/blob/main/images/03.%20categorical.PNG?raw=true)

  To find out what are the most relevant features, we got the correlations of the features with the target variable (price). This step shown that the carat is the most relevant feature once it's correlation is the nearest to 1.
  
![image](https://github.com/pedrolaender/03.Ironhack_Diamonds/blob/main/images/04.%20correlation.PNG?raw=true)

  Using visualization methods it was possible to reveal a patter when relating Carat + Clarity with Price and Carat + Color with Price as shown in the figures below.

Carat + Clarity          |  Carat + Color
:-------------------------:|:-------------------------:
![image](https://github.com/pedrolaender/03.Ironhack_Diamonds/blob/main/images/05.%20clarity.PNG?raw=true)   |   ![image](https://github.com/pedrolaender/03.Ironhack_Diamonds/blob/main/images/06.%20color%20.PNG?raw=true)


  With this knowledge the idea now is to create 4 for each of this features (Clarity and Color). By doing this we will have 4 different coefficients (linear regressions) for each of this features and we will have to join this coefficients giving a total of 16 differente models.

  Joining all 16 models we got the results of the prediction model:
  - Test Dataset RMSE: 831,30
  - Rick's Dataset RMSE: 845,09   

## Conclusion
  There are countless possibilities when it comes to improve a predict model. With the approach followed in this project we achieved our goal by getting a RMSE of 845,09 on Rick's Diamond Dataset.
  
## Contact

  Pedro Laender
  
  Github - (https://github.com/pedrolaender)
 
