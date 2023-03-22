# The Power of Plots

What good is data without a good plot to tell the story?

## Background

I've just  joined Pymaceuticals Inc., a new pharmaceutical company that specializes in anti-cancer pharmaceuticals. Recently, it began screening for potential treatments for squamous cell carcinoma (SCC), a commonly occurring form of skin cancer.

As a senior data analyst at the company, I have been given access to the complete data from their most recent animal study. In this study, 249 mice identified with SCC tumor growth were treated with a variety of drug regimens. Over the course of 45 days, tumor development was observed and measured. The purpose of this study was to compare the performance of Pymaceuticals' drug of interest, Capomulin, versus the other treatment regimens. 

![image](https://user-images.githubusercontent.com/100399092/212573550-dd36c71c-a1d2-4d38-9cd0-31652be4ffea.png)

The executive team has tasked me with generating all of the tables and figures needed for the technical report of the study. They have also asked for a top-level summary of the study results.

## Instructions

My tasks are to do the following:

* Prepare the data.

* Generate summary statistics.

* Create bar charts and pie charts.

* Calculate quartiles, find outliers, and create a box plot.

* Create a line plot and a scatter plot.

* Calculate correlation and regression. 

* Submit your final analysis. 

### Prepare the Data

1. Run the provided package dependency and data imports, and then merge the `mouse_metadata` and `study_results` DataFrames into a single DataFrame.

2. Display the number of unique mice IDs in the data, and then check for any mouse ID with duplicate time points. Display the data associated with that mouse ID, and then create a new DataFrame where this data is removed. Use this cleaned DataFrame for the remaining step.

3. Display the updated number of unique mice IDs.

### Generate Summary Statistics

Create two summary statistics DataFrames:

    * For the first table, use the `groupby` method to generate the mean, median, variance, standard deviation, and SEM of the tumor volume for each drug regimen. This should result in five unique series objects. Combine these objects into a single summary statistics DataFrames.

    * For the second table, use the `agg` method to produce the same summary statistics table by using a single line of code.

### Create Bar Charts and a Pie Charts

1. Generate two bar plots. Both plots should be identical and show the total number of timepoints for all mice tested for each drug regimen throughout the course of the study.

    * Create the first bar plot by using Pandas's `DataFrame.plot()` method.

    * Create the second bar plot by using Matplotlib's `pyplot` methods.

2. Generate two pie plots. Both plots should be identical and show the distribution of female or male mice in the study.

    * Create the first pie plot by using both Pandas's `DataFrame.plot()`.

    * Create the second pie plot by using Matplotlib's `pyplot` methods.

### Calculate Quartiles, Find Outliers, and Create a Box Plot 

1. Calculate the final tumor volume of each mouse across four of the most promising treatment regimens: Capomulin, Ramicane, Infubinol, and Ceftamin. Then, calculate the quartiles and IQR and determine if there are any potential outliers across all four treatment regimens. Follow these substeps:

    * Create a grouped DataFrame that shows the last (greatest) time point for each mouse. Merge this grouped DataFrame with the original cleaned DataFrame.

    * Create a list that holds the treatment names, as well as a second, empty list to hold the tumor volume data.

    * Loop through each drug in the treatment list, locating the rows in the merged DataFrame that correspond to each treatment. Append the resulting final tumor volumes for each drug to the empty list. 

    * Determine outliers by using the upper and lower bounds, and then print the results.
    
2. Using Matplotlib, generate a box plot of the final tumor volume for all four treatment regimens. Highlight any potential outliers in the plot by changing their color and style.

 ### Create a Line Plot and a Scatter Plot

1. Select a mouse that was treated with Capomulin and generate a line plot of tumor volume vs. time point for that mouse.

2. Generate a scatter plot of tumor volume versus mouse weight for the Capomulin treatment regimen.

### Calculate Correlation and Regression

1. Calculate the correlation coefficient and linear regression model between mouse weight and average tumor volume for the Capomulin treatment. 

2. Plot the linear regression model on top of the previous scatter plot.

### Final Analysis

Review all the figures and tables that were generated in this project. Write at least three observations or inferences that can be made from the data. 

## Technologies used
Matplotlib, VS Code, Python, Pandas, Jupyter Notebook, Stack Overflow

