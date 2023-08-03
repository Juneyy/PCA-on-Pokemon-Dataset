# PCA-on-Pokemon-Dataset
Principal component analysis improves the decision tree performance by reducing overfitting

## Motivation
Some dataset gets too large and takes plenty of time to train. Principal component analysis tries to reduce the columns by transforming them into new axis. I have been a big Pokemon fan since I was a kid. I wanted to do some analysis of the stats.

## Dataset
We are taking the base stats (attack, defense, speed, special attack, special defense) and what the type is strong or weak against to determine the Pokemon type. 

## PCA
Before taking the PCA, PCA expects a normal distribution. Every column is subtracted by the mean of each column and divided by the standard deviation of each column. 
Then using the PCA function from sklearn.decomposition to find the PCA transformed of the dataset. Graphing the explained variance and cumulative variation. 

<div align="center">
    <img alt="churn" src="PCA.png">
</div>

The first 19 columns already capture 97.6% of the original dataset. 

## Test regular dataset and PCA-transformed dataset on decision tree

Only the first 19 columns of the PCA-transformed dataset were used in the training. The dataset is split with 75% training and 25% training.

**The decision tree without PCA gave an accuracy of 85.5% and with PCA gave an accuracy of 89.6%. This shows the original decision overfitted with the remaining 2.4% of the dataset, resulting in a lower accuracy score in the original dataset.** 

