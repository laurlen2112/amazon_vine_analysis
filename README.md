# Amazon Vine Analysis

## Overview:

This analysis was conducted to investigate if Amazon Vine members tend to give higher ratings to products they received for free in exchange for a review. The dataset used for this analysis was the "toys" Amazon review set. To interact with the dataset, an ETL process was conducted in [Google Colaboratory using PySpark](https://github.com/laurlen2112/amazon_vine_analysis/blob/main/challenge/Amazon_Reviews_ETL.ipynb), and the cleaned data was stored in AWS and transferred to PG Admin in the form of 4 tables. The analysis of the Vine dataset was performed in [Jupyter Notebook](https://github.com/laurlen2112/amazon_vine_analysis/blob/main/challenge/Vine_Review_Analysis.ipynb) using Pandas. As someone who loves to delve into data and explore patterns, I found it exciting to conduct this analysis and draw meaningful conclusions from the data.

![etl diagram](https://github.com/laurlen2112/amazon_vine_analysis/blob/main/resources/etl%202.png)


## Results:
* There were a total of 1266 paid Vine reviews and a total of 62,028 unpaid reviews.  The unpaid review set is almost 50 times larger than the Vine review set.  

![bullet 1](https://github.com/laurlen2112/amazon_vine_analysis/blob/main/resources/bullet%201%20h.png)

* The Vine review set has a total of 432 five star reviews and the unpaid review set has a total of 29,982 reviews.  The unpaid review set has about 70 times more five star reviews than the Vine review set.  

![bullet 2](https://github.com/laurlen2112/amazon_vine_analysis/blob/main/resources/bullet%202.png)

* 34.12% of the Vine review set is comprised of five star reviews and 48.34% of the unpaid review set is comprised of five star reviews.  

![bullet 3](https://github.com/laurlen2112/amazon_vine_analysis/blob/main/resources/bullet%203.png)


## Summary
Based on this analysis the Vine reviews do not seem have a positivity bias because only 34.12% of that dataset is comprised of five star reviews.  By comparison, the composition of the unpaid review dataset contains nearly 50% five star reviews.  Therefore, this analysis indicates a positivity bias in the unpaid dataset. 

However, evaluating only the percentage of five star reviews may not provide the full picture of bias in the Vine program. It is important to also consider the distribution of reviews across different star ratings. As demonstrated in [the code](https://github.com/laurlen2112/amazon_vine_analysis/blob/main/challenge/Vine_Review_Analysis.ipynb), a similar analysis should be run on other review levels of each dataset to determine their percentages. Additionally, the results should be aggregated to determine the percentage of overall favorable reviews to the percentage of overall unfavorable reviews. Evaluating the distribution of reviews across different star ratings is important because if the majority of Vine reviews are concentrated in the higher star ratings (e.g., 4 or 5 stars), then there could still be a bias towards positive reviews even if the percentage of 5-star reviews is lower.

![summary](https://github.com/laurlen2112/amazon_vine_analysis/blob/main/resources/summary.png)

The aggregated overall favorable Vine reviews is about 90%.  By contrast, the aggregated overall favorable unpaid reviews is about 75%.  Based on this comparison, the Vine dataset may demonstrate bias toward a favorable review compared with the unpaid dataset.
