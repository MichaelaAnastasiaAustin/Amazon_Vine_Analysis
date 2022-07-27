# Amazon_Vine_Analysis

## Overview

The purpose of this assignment was to analyze Amazon reviews written by members of the paid Amazon Vine program. The Amazon Vine program is a service that allows manufacturers and publishers to receive reviews for their products. Companies like SellBy pay a small fee to Amazon and provide products to Amazon Vine members, who are then required to publish a review.After choosing to assess the apparel dataset, we completed the following technical deliverables:

1) Use PySpark to perform the ETL process to extract the dataset, transform the data, connect to an AWS RDS instance, and load the transformed data into pgAdmin. 

2) Use PySpark to determine if there was any bias toward favorable reviews from Vine members in the dataset. 

## Resources
- Data Source: [Amazon Reviews](https://s3.amazonaws.com/amazon-reviews-pds/tsv/index.txt)
- Software: Google Colab Notebook, PostgreSQL, pgAdmin 4, AWS


## Results

How many Vine reviews and non-Vine reviews were there?
- Vine Reviews
![vine_reviews](https://github.com/MichaelaAnastasiaAustin/Amazon_Vine_Analysis/blob/main/images/total_paid_reviews.png)
- non_Vine Reviews
![non_vine_reviews](https://github.com/MichaelaAnastasiaAustin/Amazon_Vine_Analysis/blob/main/images/total_unpaid_reviews.png)

How many Vine reviews were 5 stars? How many non-Vine reviews were 5 stars?
- 5 star Vine reviews
![paid_5star](https://github.com/MichaelaAnastasiaAustin/Amazon_Vine_Analysis/blob/main/images/paid_5star.png)

- 5 star non-Vine reviews
![unpaid_5star](https://github.com/MichaelaAnastasiaAustin/Amazon_Vine_Analysis/blob/main/images/unpaid_5star.png)

What percentage of Vine reviews were 5 stars? What percentage of non-Vine reviews were 5 stars?
- percentage of Vine reviews that were 5 stars:
![percent_paid_5star](https://github.com/MichaelaAnastasiaAustin/Amazon_Vine_Analysis/blob/main/images/percentage_paid_5star.png)
- percentage of non-Vine reviews were 5 stars
![percent_unpaid_5star](https://github.com/MichaelaAnastasiaAustin/Amazon_Vine_Analysis/blob/main/images/percentage_unpaid_5star.png)

## Summary
All in all, there does not appear to be positivity bias for reviews in the Vine program. For the apparel dataset, less than half of Vine reviews were five stars -- 45%. In comparison, 52% of non-Vine reviews were five stars. To further assess the potential of any positivity bias for reviews in the Vine program, I would recommend pulling in the "review_headline" and/or "review_body" columns from the original dataset table into our vine_table. Then, we would be able to assess the length of reviews or whether certain positive words were used more frequently in Vine program reviews.

