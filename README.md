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

### The Vine DataFrame:
![vine_df](https://user-images.githubusercontent.com/78666055/122581308-e982de00-d024-11eb-8556-ef23cbe98c0c.png)

### The Calculations:
![Del2_results_1](https://user-images.githubusercontent.com/78666055/122581245-d8d26800-d024-11eb-97c0-befc90679704.png)

### The Percentages:
#### There seem to be no bias in the reviews as the percentages are almost identical.
![Del2_results_2](https://user-images.githubusercontent.com/78666055/122581256-db34c200-d024-11eb-93fe-7099b85d47e1.png)


# Summary

The percentages of Vine reviews that were 5-stars and the percentage of non-Vine reviews that were 5-stars are almost identical, suggesting there is NO BIAS in the reviews. However the number of Vine reviews is low and may be different over a larger number of reviews.

Lowering the percentage of helpful_votes filtered (>= 50%) to maybe 40% and lowering the total_votes filter (>= 20) to maybe 15 would use more rows from the dataset and produce a different result.
This test was performed and as can be seen there is starting to be some separation in the two percentages, showing some bias on the Vine reviews.

![Summary](https://user-images.githubusercontent.com/78666055/122580909-79745800-d024-11eb-832f-f32407af72ac.png)
