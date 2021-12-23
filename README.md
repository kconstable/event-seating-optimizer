# Event Seating Optimizer
This project uses linear programming in pyhton to optimze event seating.  It supports multiple tables of different sizes. The seating arrangements are optimized based on pair-wise happinesss scores assigned to pairs of event attendees. 

## Happiness Scores
A csv file is used to score pairs of attendees.  Every possible combination of pairs are listed in the pairs column. Set large negative values for undesirable combinations (-200), in this case we don't want anyone seated at a table alone.  Partners that you want at the same table should be assigned a large positive score (+200).  People that know each other can be given a small positive score (+50) and people that don't know each other can have a neutral score of zero or slightly negative. 

![image](https://user-images.githubusercontent.com/1649676/147284140-04ddf6e1-0dde-48a1-a7bc-44d2dc301512.png)





