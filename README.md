# Event Seating Optimizer
This project uses linear programming in python to optimize event seating.  It supports multiple tables of different sizes. The seating arrangements are optimized based on pair-wise happiness scores assigned to pairs of event attendees. 

## Problem Setup
The problem uses the pulp python library to optimize the seating arrangements.  It requires a list of guests, the number and capacity of each table, and happiness scores for each pair of attendees.  Guests are provided as a space-separated string.  The table capacity is a list of tuples, with each element representing the (table capacity, number of tables).  The constraints are that each person must be seated at a table, and only one table and the number and capacity of each table are respected.

![image](https://user-images.githubusercontent.com/1649676/147284755-41900211-1dc7-4c0e-9d0f-2a0dec0cca88.png)


## Happiness Scores
A csv file is used to score pairs of attendees.  Every possible combination of pairs is listed in the pairs column. Set large negative values for undesirable combinations (-200), in this case, we don't want anyone seated at a table alone.  Partners that you want at the same table should be assigned a large positive score (+200).  People that know each other can be given a small positive score (+50) and people that don't know each other can have a neutral score of zero or slightly negative. 

![image](https://user-images.githubusercontent.com/1649676/147284140-04ddf6e1-0dde-48a1-a7bc-44d2dc301512.png)


## Optimizing the Seating Arrangements
In the example, 32 guests are seated at one of six tables of four people, or five tables of two people.  The function prints out the optimal seating based on the happiness scores and problem constraints.
![image](https://user-images.githubusercontent.com/1649676/147285261-6ccf1820-5027-4906-991c-e619917462d6.png)




