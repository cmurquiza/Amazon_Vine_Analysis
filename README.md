# Amazon_Vine_Analysis - Big Data/AWS

For this part of the Challenge, you’ll write a report that summarizes the analysis you performed in Deliverable 2.
The report should contain the following:
Overview of the analysis: Explain the purpose of this analysis.
Results: Using bulleted lists and images of DataFrames as support, address the following questions:
How many Vine reviews and non-Vine reviews were there?
How many Vine reviews were 5 stars? How many non-Vine reviews were 5 stars?
What percentage of Vine reviews were 5 stars? What percentage of non-Vine reviews were 5 stars?
Summary: In your summary, state if there is any positivity bias for reviews in the Vine program. Use the results of your analysis to support your statement. Then, provide one additional analysis that you could do with the dataset to support your statement.

## Overview of the analysis:
The purpose of this analysis was to look over reviews from products from amazon, and to analyze and determine if there is any bias or relationship between participating in Amazon's Vine program and 5-star reviews given to a product. 

We chose a data set, and the one for this analysis can be found here: https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Health_Personal_Care_v1_00.tsv.gz

The data was put into a Google colab notebook which was downloaded as a ipynb file and can be found here: https://github.com/cmurquiza/Amazon_Vine_Analysis/blob/main/Amazon_Reviews_ETL.ipynb 

It was processed using Spark to load it into a database. Data at first was put into a raw dataframe. It was put into 4 separate tables consisting of the Costumer table, the Reviews ID table, the Products table, and then Vine table. The Vine table contained the information needed for the next part of the analysis. It was then stored into tables in the database in SQL with all of the data. 

## Results

<img width="753" alt="Screen Shot 2023-02-09 at 1 55 51 PM" src="https://user-images.githubusercontent.com/109998935/217910372-3a05573a-3176-47ff-ba17-edc5f1410f03.png">

As you can see, there were:
- Total number of reviews: 121360
- Total number of  paid reviews: 497
- Total number of paid five star reviews: 220
- Total number of unpaid reviews: 120863
- Number of 5 star unpaid reviews: 74470
- Percentage of paid five star reviews out of total number reviews: 0.181279
- Percentage of unpaid five star reviews out of total number reviews: 61.362887

With this, there does not seem to be much of a positivity bias when looking at the percentage of paid 5 star reviews out of total number of reviews being only 18%. 

# Further Analysis: 
Additional Analysis

In the future, we can further assess and do the same analysis for the star_ratings and see if there is bias there. If there was, you'd be able to look into to see if the vine_reviews would be significantly higher than the non-vine reviews.
