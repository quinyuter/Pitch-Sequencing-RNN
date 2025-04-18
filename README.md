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
- sale_modeling.csv, skubal_modeling.csv: Fully cleaned data to use for modeling.
- Pitch_Sequencing_EDA.ipynb: Exploratory Data Analysis of the data.
- Pitch_Feature_Engineering.ipynb: Final Cleaning, encoding, and normalizing.
- Pitch Sequencing RNN Modeling: Hyperparameter tuning, Recurrent Neural Network Modeling
- Pitch Sequencing RNN Report - Finished: Final Report of the project, outlining methods, results, reasoning behind the project, etc.

## Order in which to view the code
1. Pitch by Pitch Cleaning
2. Pitch Sequencing EDA
3. Pitch Sequencing Feature Engineering
4. Pitch Sequencing RNN Modeling

## Results
I created a new statistic called Predictability Score, which scores a pitcher from 0 to 1, with 1 meaning a pitcher is 100% predictable and 0 meaning a pitcher is not predictable at all. Chris Sale had a predictability score of 0.350 in the 2024 season. Tarik Skubal had a 0.375 predictability score. So, in the 2024 season, Tarik Skubal was a more predictable pitcher.

## Report Abstract

This personal research project investigates whether Major League Baseball pitch sequences can be predicted using Recurrent Neural Networks (RNNs). Focusing on 2024 Cy Young winners Chris Sale and Tarik Skubal, pitch level data was gathered, cleaned, explored, and used to build GRU-based RNN models using PyTorch. While model test accuracy hovered around 50%, I developed a new metric called Predictability Score (PS) that better reflects how predictable a pitcher is, accounting for the number of pitches in their arsenal. The results suggest that Tarik Skubal is slightly more predictable than Chris Sale, with a PS of 0.375 compared to 0.350. This project not only sharpened my RNN and Pytorch skills but also yielded interesting questions about how data science can affect decision making in baseball. There is still plenty of room for this model to grow, whether it be incorporating batter tendencies, experimenting with different model types, or removing sequence length constraints, but this was a rewarding step towards building a predictive tool that could benefit hitters, pitchers, and analysts.
