# Amazon_Vine_Analysis
## Overview of the Module 16 Challenge

The project's objective is to analyze a dataset of Amazon reviews. The data comes from an AWS link. The dataset contains two types of reviews: the ones that come from the Amazon Vine paid program and the ones that do not come from any paid program. Using PySpark in Google Colab Notebooks, we will perform the ETL process to understand if there is any bias from the paid program reviews. 

### Files and Folders

Amazon_Reviews_ETL.ipynb

Vine_Review_Analysis.ipynb

Resources: images

## Results

After applying different functions (filter, select, sum, and count), we calculated the total count, total five starts count, and five stars percentage of paid and non-paid programs reviews.

### Summary results DataFrame

Before explaining the results, we are going to mention the considerations that were taken for filtering the data: 

-  We took out of the analysis all the review ids with less than 20 votes for ensuring we had enough votes to make calculations
- We only kept review ids that had 50% or more of helpful votes.

On one hand, there were 60 reviews that belonged to Vine's program, and 34 of them were five stars. At the same time, 14477 reviews were not from Vine's paid program and 8212 were five stars. The percentage of five stars reviews from both was 56%. Because of the similarity of the percentage, it might be inferred that the reviews are probably biased. Further analysis from this and other datasets might be needed to get a final conclusion. 

!['dataframe'](https://github.com/DylanMontemayor/Amazon_Vine_Analysis/blob/main/Resources/dataframe.png)

### Summary

In summary, because of the similarity in the percentages, there is data that proves that reviews from Vine's paid program might be biased. If the same result is found after analyzing more datasets, it will be important to check with Vine the process they follow for collecting all the reviews. 
