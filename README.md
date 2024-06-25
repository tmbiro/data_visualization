# Matplotlib Challenge

## Background
For this challenge, I've joined Pymaceuticals, Inc., a new pharmaceutical company that specializes in anti-cancer medications. Recently, it began screening for potential treatments for squamous cell carcinoma (SCC), a commonly occurring form of skin cancer.

As a senior data analyst at the company, I've been given access to the complete data from their most recent animal study. In this study, 249 mice who were identified with SCC tumors received treatment with a range of drug regimens. Over the course of 45 days, tumor development was observed and measured. The purpose of this study was to compare the performance of Pymaceuticals’ drug of interest, Capomulin, against the other treatment regimens.

The executive team tasked me with generating all of the tables and figures needed for the technical report of the clinical study. They also asked me for a top-level summary of the study results

## Approach

First, I inspected the dataset. It looked like this:

<img width="774" alt="image" src="https://github.com/tmbiro/data_visualization/assets/26468137/b72cc015-1091-4420-a63b-544257bcdc04">

I generated a summary statistics table of mean, median, variance, standard deviation, and standard error of the mean (SEM) of the tumor volume for each regimen, which resulted in:

<img width="891" alt="image" src="https://github.com/tmbiro/data_visualization/assets/26468137/4143855c-85fa-4c6a-ad43-58c51c20050c">

Next, I generated a bar plot showing the total number of time points for all mice tested for each drug regimen throughout the study. Here is what the plot looked like when generated with pyplot (using pandas DataFrame.plot() method produces a similar result):

![image](https://github.com/tmbiro/data_visualization/assets/26468137/283e6490-888f-44a9-9d8c-ddb106633fbb)

I also generated a pie plot showing the distribution of female versus male mice using both pandas and pyplot. It looked like this using both methods:

![image](https://github.com/tmbiro/data_visualization/assets/26468137/355de9d7-9e7d-4f9a-beb2-5fc2f4933ad4)

I generated a box plot that shows the distrubution of the tumor volume for each treatment group:

![image](https://github.com/tmbiro/data_visualization/assets/26468137/a87a6f5a-6e24-410a-8906-33212198814b)

I then created a line plot of tumor volume vs. time point for a mouse treated with Capomulin:

![image](https://github.com/tmbiro/data_visualization/assets/26468137/4c4479f6-45c4-4ba7-ae01-bdffeb2cf75b)

I generated a scatter plot of average tumor volume vs. mouse weight for the Capomulin regimen:

![image](https://github.com/tmbiro/data_visualization/assets/26468137/e268ecd7-5d1e-4e9b-807e-95502ec1b379)

Lastly, I calculated the correlation coefficient and linear regression model for mouse weight and average tumor volume for the Capomulin regimen:

![image](https://github.com/tmbiro/data_visualization/assets/26468137/a68ec701-69ea-4259-98bb-aa95a2257199)

## Analysis

Here is what I observed:
* Capomulin and Remicane appear to be more effective at reducing tumor volume compared to Ceftamin and Infubinol. However, Capomulin and Remicane also have data at more timepoints compared to Ceftamin and Infubinol, thus, this relationship could be due to the availability of data across treatment groups.
* For mice on Capomulin, every gram increase in mouse weight was associated with a .95 mm3 increase in tumor volume according to our analysis. This was confirmed using Person's R (r = 0.84).




