 Verve Group Data Science Case Study 
==============================


Table of contents
* [Introduction](#introduction)
* [Problem-1](#problem-1)
* [Problem-2](#problem-2)


## Introduction
According to the given JSON data, the required analysis is processed to find a solution for problems. 
Outcomes; 
- The data sizes is: (20, 4)
- The type of data as seen below:

| #  | col     |   non-null count |   dtype | 
|---:|:--------|-----------------:|--------:|
|  0 | app     |   20 non-null    |  object |
|  1 |bid_price|   20 non-null    | float64 |      
|  2 | win     |   20 non-null    |  int64  |       
|  3 | events  |   20 non-null    |  int64  |        

- There is only one app which is A.
- The 'bid_price' column has 10 different pricess which are more than 0.
- The maximum event is 8000000 which belongs to 0.2 in bid_price.


## Problem-1

For the first problem the calculateWinRate is created to calculated the  win_rate, and it is calculated as seen below:
The calculated value is plotted in the jupyter notebook.

| #  | app     |   bid_price |   win_rate | 
|---:|:--------|------------:|-----------:|
|  0 | A       |   0.01      |      0.0   |
|  1 | A       |   0.10      |      0.3   |    
|  2 | A       |   0.20      |      0.2   |     
|  3 | A       |   0.40      |      0.3   |    
|  4 | A       |   0.50      |      0.2   |
|  5 | A       |   0.75      |      0.3   |    
|  6 | A       |   1.00      |      0.6   |     
|  7 | A       |   2.00      |      0.7   |    
|  8 | A       |   5.00      |      0.8   |
|  9 | A       |   9.00      |      1.0   |    
 

## Problem-2 

For the first problem the calculateRevenue is created to calculated the  revenue, and it is calculated as seen below:

| #  | bidPrice | totalEvent |  revenue   |   
|---:|:---------|-----------:|-----------:|
|  0 |   0.01   |    100000  |       0.0  |
|  1 |   0.10   |     10000  |    1200.0  |  
|  2 |   0.20   |  10000000  |  600000.0  |
|  3 |   0.40   |   1000000  |   30000.0  |
|  4 |   0.50   |    100000  |       0.0  |
|  5 |   0.75   |     10000  |    -750.0  |
|  6 |   1.00   |      1000  |    -300.0  |
|  7 |   2.00   |       100  |    -105.0  |
|  8 |   5.00   |        10  |     -36.0  |
|  9 |   9.00   |         1  |      -8.5  |

In the calculation of revenue below formula is used:
 
*revenue = (revenuePerWin - bidPrice) * (eventForWin1 / totalEvent) * totalEvent*


*revenuePerWin=0.5 -> since it is already mentioned in the problem-2 definition*

*bidPrice -> this value is available in the table*

*eventForWin1 -> events value in the table according to bidPrice value for the succesfull events*

*totalEvent -> total events in the table according to bidPrice*


The max revenue with max event min bid_price is observed for bidPrice = 0.2. That will give us the optimum number for bid_price to earn max revenue.
