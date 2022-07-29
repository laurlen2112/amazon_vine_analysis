# Amazon Vine Analysis

## Overview:
Some companies, like SellBy, provide products to Amazon Vine members in exchange for a review of the product.  The purpose of this analysis is to determine if Amazon Vine members favorably rate products based on this practice.  The "toys" Amazon review set was choosen for this analysis.  The ETL process was conducted in [Google Colaboratory using Pyspark](https://github.com/laurlen2112/amazon_vine_analysis/blob/main/challenge/Amazon_Reviews_ETL.ipynb) to interact with the dataset and AWS to store it.  The cleaned data was sent to PG Admin in the form of 4 tables.  The analysis on the Vine dataset was performed in [Jupyter Notebook](https://github.com/laurlen2112/amazon_vine_analysis/blob/main/challenge/Vine_Review_Analysis.ipynb) using Pandas.
![etl diagram](https://github.com/laurlen2112/amazon_vine_analysis/blob/main/resources/etl%202.png)

## Results:
* There were a total of 1266 paid Vine reviews and a total of 62,028 unpaid reviews.  The unpaid review set is almost 50 times larger than the Vine review set.  
![bullet 1](https://github.com/laurlen2112/amazon_vine_analysis/blob/main/resources/bullet%201.png)

* The Vine review set has a total of 432 five star reviews and the unpaid review set has a total of 29,982 reviews.  The unpaid review set has about 70 times more five star reviews than the Vine review set.  
![bullet 2](https://github.com/laurlen2112/amazon_vine_analysis/blob/main/resources/bullet%202.png)

* 34.12% of the Vine review set is comprised of five star reviews and 48.34% of the unpaid review set is comprised of five star reviews.  
![bullet 3](https://github.com/laurlen2112/amazon_vine_analysis/blob/main/resources/bullet%203.png)

## Summary
Based on this analysis the Vine reviews do not seem have a positivity bias because only 34.12% of that dataset is comprised of five star reviews.  By comparason, the composition of the unpaid review dataset is nearly 50% five star reviews.  However, evaluating five star reviews is not the only method to determine bias.  A similar analysis should be run on the other review levels to determine their percetage of the dataset.  Additionally, he three to five star review levels shoud be aggregated to compare 
