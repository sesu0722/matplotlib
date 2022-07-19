# Project: The Power of Plots

In this homework assignment, I apply Matplotlib to a real-world situation and dataset.

## Background
The dataset has 249 mice identified with SCC tumor growth were treated with a variety of drug regimens. Over the course of 45 days, tumor development was observed and measured to compare the performance of Pymaceuticals' drug of interest, Capomulin, versus the other treatment regimens.
The task is to generat all of the tables and figures needed for the technical report and summary of the study.

## Data and analysis file
In the Pymaceuticals folder- there is a Data folder and Pymaceuticals_starter.ipynb file, the mouse data and study results data are unde the Data folder, and the Pymaceuticals_starter is the analysis file.

### Prepare the Data

1. fist merge the `mouse_metadata` and `study_results` DataFrames into a single DataFrame by mouse ID.

2. Display the number of unique mice IDs in the data, and then check for any mouse ID with duplicate time points. Display the data associated with that mouse ID, and then create a new DataFrame where this data is removed. Use this cleaned DataFrame for the remaining step.

3. Display the updated number of unique mice IDs.

### Generate Summary Statistics

Create two summary statistics DataFrames:

1. For the first table, use the `groupby` method to generate the mean, median, variance, standard deviation, and SEM of the tumor volume for each drug regimen.

2. For the second table, use the `agg` method to produce the same summary statistics table by using a single line of code.

### Create Bar Charts and a Pie Charts

1. Generate two bar plots. showing the total number of timepoints for all mice tested for each drug regimen

    * Create the first bar plot by using Pandas's `DataFrame.plot()` method.

    * Create the second bar plot by using Matplotlib's `pyplot` methods.

2. Generate two pie plots. Showing the distribution of female or male mice in the study.

    * Create the first pie plot by using both Pandas's `DataFrame.plot()`.

    * Create the second pie plot by using Matplotlib's `pyplot` methods.

### Calculate Quartiles, Find Outliers, and Create a Box Plot 

1. Calculate the final tumor volume of each mouse across four of the most promising treatment regimens: Capomulin, Ramicane, Infubinol, and Ceftamin. Then, calculate the quartiles and IQR and determine if there are any potential outliers across all four treatment regimens. Follow these substeps:

    * Create a grouped DataFrame using .max to get the last (greatest) time point for each mouse. Merge this grouped DataFrame with the original cleaned DataFrame.

    * Create two lists: treatment_list to hold the drug names and tumor_vol_list for the tumor volume data.

    * Loop through each drug in the treatment_list, locating the rows in the merged DataFrame that correspond to each treatment. Append the resulting final tumor volumes for each drug to the empty list. 

    * Determine outliers by using the upper and lower bounds, and then print the results.
    
2. Using Matplotlib, generate a box plot of the final tumor volume for all four treatment regimens. 

### Create a Line Plot and a Scatter Plot

1. Select a mouse that was treated with Capomulin and generate a line plot of tumor volume vs. time point for that mouse.

2. Generate a scatter plot of tumor volume versus mouse weight for the Capomulin treatment regimen.

### Calculate Correlation and Regression

1. Calculate the correlation coefficient and linear regression model between mouse weight and average tumor volume for the Capomulin treatment. 

2. Plot the linear regression model on top of the previous scatter plot.


## Final Analysis

1.Across the ten drugs in this study, Capomulin and Ramicane yield the best results by effectivly reduceing the tumor volume over the course of 45 days.    

2.There is stong postive correlation between mouse weight and the average tumor volume, it will need further study to determine if weight increase contributes to tumor volume increased and drug effectiveness. 

3.The dataset has mouse age from 2 to 21 months that could be a factor to drug effectiveness, further analysis by age group will help to clarify the impacts.
