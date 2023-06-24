# Fifa-22-Players-Dataset-Analysis
Importing the necessary libraries: The code imports pandas, numpy, matplotlib, seaborn, and missingno libraries.

Setting options and styles: The code sets display options for pandas dataframes, sets the style for matplotlib plots, and ignores warnings.

Importing the dataset: The code reads a CSV file named 'players_22.csv' into a pandas DataFrame called 'df'.

Data cleaning and manipulation: The code performs several data cleaning and manipulation tasks on the DataFrame 'df'.

Dropping useless columns: It creates a list of columns to drop and removes them from the DataFrame, creating a new DataFrame called 'new_df'.

Adding BMI column: It calculates the BMI (Body Mass Index) for each player using their weight and height and adds it as a new column 'BMI' to 'new_df'.

Checking null values: It selects a list of important columns and checks the number of null values in those columns.

Creating new columns from player positions: It uses the 'player_positions' column to create new columns for each position using one-hot encoding (get_dummies() function). These columns indicate whether a player plays in a particular position or not.

Dropping unnecessary columns: It drops the 'player_positions' column from 'new_df' since the position information has been encoded into separate columns.

Manipulating columns with values like '89+3', '90+2', etc.: It splits the values in columns like 'ls', 'st', 'rs', etc., at the '+' sign and keeps only the first part of the split value using the str.split() method. This operation removes the extra values after the '+' sign.

Filling null values: It fills the null values in columns 'dribbling', 'defending', 'physic', 'passing', 'shooting', and 'pace' with the median value of each column.

Visualizing null values: It uses the missingno library to create a matrix plot and bar graph to visualize the missing values in the DataFrame.

Data analysis: The code performs some data analysis tasks on the DataFrame.

Comparison of traits for defenders: It selects the columns 'overall', 'potential', 'pace', 'shooting', 'passing', 'dribbling', 'defending', and 'physic' for defenders and compares the values for players Sergio Ramos and Virgil van Dijk.

Data of Ramos and Van Dijk: It extracts the values for Sergio Ramos and Virgil van Dijk from the selected traits and stores them in a list called 'values'.

Overall, the code performs various data cleaning, manipulation, and analysis tasks on a dataset using pandas.
