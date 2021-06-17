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
