![Header Image](https://github.com/mross715/MicrosoftProject/blob/main/images/readme%20image.png)
Source: freepik

# Microsoft Studios Movie Analysis

## August 2021

Allison Gao, Ronak Parekh, Meaghan Ross 

## General Overview 
This analysis uses historical data on movies released in the past 10 years to provide insight for Microsoft Corporation seeking to enter the movie industry. An exploratory data analysis shows that genre selection and movie release time are important factors to consider while production budget needs to be analyzed within the context of genre selection. Microsoft Corporation can use this project’s findings to inform its business decision with respect to its entry into the movie industry. 

## Business Understanding
Using return on investment (ROI) as the metric for evaluation, Microsoft needs to consider various factors relating to movie production that affect ROI. In particular, Microsoft should consider variables that can help increase ROI. Such a strategy will help minimize financial risk for the corporation who is new to the movie industry. 

## Data 

###### Data Source
This project utilized two datasets from IMDb and one dataset from the-numbers.com. After merging these datasets, they collectively contained information on movie title, genre, release date, runtime, rating, production, and domestic and worldwide gross income for movies released in the past 10 years. 

###### Data Shape
The IMDb dataset that contains movie title and genre information has 146,144 rows while the other IMDb dataset on consumer rating has 73,856 rows. Additionally, the dataset from the-numbers.com containing information on production budget and gross income has 5,782 rows. Each row represents a movie. 

###### Data Preparation
We cleaned each dataset before merging them for analysis. Our cleaning process focused on eliminating rows that contain null values, duplicated rows, and outliers. We also created additional columns that are needed for analysis. This included the profit and return on investment columns using existing information on production budget and gross income. Additionally, the original dataset combined multiple genres together for a significant amount of movies, limiting our ability to analyze movies by individual genre type. As a result, we split those containing multiple genres into individual genres. Furthermore, we also filtered our data to only look at movies that returned positive ROI, an indicator of financial success. Given that our metric for analysis is ROI, we want to base our recommendation on positive financial success. 

At the end of the cleaning and merging process, the data had 1357 movies released in the past ten years for analysis. 


## Data Analysis 

This project used exploratory data analysis to generate summary statistics of various variables in the dataset. Anchoring our analysis on potential movie genres that Microsoft should consider, we examined how Microsoft can maximize ROI with respect to other factors. In particular, we focused on the following variables: release date, production budget, and worldwide gross. 


## Results 

###### Question 1: Which genres generate the highest average ROI?

![Header Image](https://github.com/mross715/MicrosoftProject/blob/main/images/Question%201.png)

By looking at movies from 2010 on, grouping them by genre indicators, and calculating the mean return on investment, we found these results as represented by the bar chart.
The top three genres that generated the greatest ROI in descending order are horror, mystery, and thriller. 


###### Question 2: What time of year should a movie be released for the greatest mean ROI?

![Header Image](https://github.com/mross715/MicrosoftProject/blob/main/images/Question%202.png)

When examining release month with respect to the top three genres as a whole, October, May, and January had the greatest mean ROI compared to other months of the year.



###### Question 3: How much money should be spent on production budget to maximize ROI?

![Header Image](https://github.com/mross715/MicrosoftProject/blob/main/images/Question%203.png)

When looking at the relationship between the production budget and return on investment for the top three genres, it produces a weak negative correlation with a Spearman’s  correlation( ρ) of -0.53 and a Pearson’s correlation (r) of -0.30. This indicates that a higher production budget will not produce a greater return on investment. 
To gain a better understanding of the distribution of the production budgets, the box plot indicates that the middle 50% of the production budgets range from 6 million to 40 million dollars.



## Conclusion 

Results from this project’s analysis suggest the following three recommendations for Microsoft to consider:

1. Not all genres are the same. Our analysis finds that certain genres are more favorable than others and choosing the right genre to produce affects return on investment. Microsoft should consider choosing from one or a combination of the top three genres identified: horror, mystery, or thriller. 

2. Timing matters. Microsoft should consider releasing its movie in October or beginning of the year. 

3. Limit budget by genre. Our analysis finds that the relationship between production budget and the return on investment for the top three genres of horror, mystery, and thriller indicates that an increase in the production budget does not lead to a greater return on investment. For that reason, when Microsoft produces a movie from the top 3 genres, they should set a budget between 6 million and 40 million dollars as this is the interquartile range or the middle 50% of the production budgets of movies. This range for the production budget of a first movie for Microsoft Studios to make will help them set a good base for the ROI and avoid spending too much money to not get an increased rate of return.

## Next Steps

1. Further analysis on budget allocation can provide insight on ways to increase ROI. For example, can spending more to secure a high paying actor/actress or renown director increase gross income? 

2. Analyzing movie rating to assess its accuracy as a predictor for ROI. In light of the COVID-19 pandemic, it would be important to research consumer sentiment and its relationship to a movie’s financial success. 


## Additional Information

See the full analysis in the [Jupyter Notebook](https://github.com/mross715/MicrosoftProject/blob/main/Project%201%20Notebook%20Final%20Version.ipynb) or review [this presentation](https://github.com/mross715/MicrosoftProject/blob/main/MicrosoftMovieProject.pdf).

For additional info, contact

Allison Gao: allison.gao@nyu.edu

Ronak Parekh: ronakp2001@live.com

Meaghan Ross: mer423@nyu.edu

## Project Structure 

```## Project Structure

├── README.md
├── data      <-- CSV and TSV files used in analyses
├── images    <-- visualizations generated from working notebooks and external images
├── Individuals Notebooks       <--- Directory for individual workspaces
│   ├── allison
│   ├── meaghan
│   ├── ronak
│   
├── Project 1 Notebook.ipynb    <-- Jupyter Notebook containing codes detailing project's analysis 
├── MicrosoftMovieProject.pdf   <-- non-technical presentation slides
└── .gitignore
