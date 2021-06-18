# Amazon_Vine_Analysis

The Amazon Vine program is a service that allows manufacturers and publishers to receive reviews for their products. Companies like SellBy pay a small fee to Amazon and provide products to Amazon Vine members, who are then required to publish a review.
We need to use PySpark, Pandas or SQl to determine if there is any bias toward favorable reviews from Vine members is the selected dataset.

### The task at hand is to:

1.	Pick a dataset and use PySpark to extract and load into a dataframe.
2.	Filter the df for total_votes >= 20 which are most likely to be helpful.
3.	Filter the df further to retrieve rows where the percentage of helpful_votes is >= 50%.
4.	 Create new dfs for where the reviews were written as part of the Vine program or not.
5.	Calculate: number of reviews, number of 5-star reviews and persentage of reviews for paid and unpaid reviews.

# Results

#### The Vine DataFrame:
##### Taken from the Home Improvement Dataset: https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Home_Improvement_v1_00.tsv.gz

![vine_df](https://user-images.githubusercontent.com/78666055/122581308-e982de00-d024-11eb-8556-ef23cbe98c0c.png)

#### The Calculations and Results as shown below:
##### 1. There were a total of 39,095 reviews filtered from the dataset based on total_votes >= 20 and percentage of helpful_votes >= 50%.
##### 2. Of this, there were 266 Vine reviews and 38,829 non-Vine reviews.
##### 3. These were further filtered to show 125 of the 266 Vine reviews were 5-star rating and 18,246 of 38,829 were 5-star rating.
<br>
<br>
![Del2_results_1](https://user-images.githubusercontent.com/78666055/122584169-0a006780-d028-11eb-9737-365b23e13131.png)

#### The Percentages:
##### As can be seen below, there seem to be no bias in the reviews as the percentages are almost identical.
<br>
<br>
![Del2_results_2](https://user-images.githubusercontent.com/78666055/122581256-db34c200-d024-11eb-93fe-7099b85d47e1.png)


# Summary

The percentages of Vine reviews that were 5-stars and the percentage of non-Vine reviews that were 5-stars are almost identical, suggesting there is NO BIAS in the reviews. However the number of Vine reviews is low and may be different over a larger number of reviews.

Lowering the percentage of helpful_votes filtered (>= 50%) to maybe 40% and lowering the total_votes filter (>= 20) to maybe 15 would use more rows from the dataset and produce a different result.
This test was performed and as can be seen there is starting to be some separation in the two percentages, showing some bias on the Vine reviews.

![Summary](https://user-images.githubusercontent.com/78666055/122580909-79745800-d024-11eb-832f-f32407af72ac.png)
