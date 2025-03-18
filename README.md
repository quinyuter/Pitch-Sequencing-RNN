# Pitch-Sequencing-RNN
Can I use a Recurrent Neural Network To Automate MLB Pitch Sequences?


## Goal
I am looking to refine my Recurrent Neural Network skills by using a new library, Pytorch in Python. I am curious to see if there is a way to predict what pitch will come based on the prior pitches in an at-bat. I am going to do this with two separate pitchers: Chris Sale and Tarik Skubal. These were the two Cy Young winners from the 2024 season. Is one more predictable than the other? How do they compare?

## Hypothesis
Do I think I will be successful? Probably not. But, I think I can learn something along the way about how pitch sequences are built. Whether it is through my intial EDA, through my data cleaning and feature engineering, or my actual modeling, something new will come from this!


## Data
PyBaseball is a library in python that scrapes Baseball Reference, Baseball Savant, and FanGraphs to give the best and most in depth data available. I am using the statcast_pitcher() function to get the data from these two pitchers.

Data Dictionary: https://baseballsavant.mlb.com/csv-docs 

## Documents
- Pitch_by_Pitch_cleaning.ipynb: Code to clean the data initially. This does not include dealing with outliers, label encoding, or normalization
- sale_2024_cleaned.csv, skubal_2024_cleaned.csv: Initial cleaned data. Because the data I am using comes through a library, I wanted to save it as a csv so I didn't have to run the pitch_by_pitch_cleaning.ipynb file.
