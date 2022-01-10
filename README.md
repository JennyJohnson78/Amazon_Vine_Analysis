# Amazon Vine Analysis

## Overview 

The Amazon Vine program is a service that allows manufacturers and publishers to receive reviews for their products. Books are a very popular category of product with a large dataset of reviews. PySpark will be used to perform the ETL process to extract the dataset, transform the data, connect to an AWS RDS instance, and load the transformed data into pgAdmin. Then, PySpark is used to determine if there is any bias toward favorable reviews from Vine members in the books dataset.

## Results

- There are 403,807 on Amazon for books with 20 or more votes deemed "helpful"

- Of those 403,807 reviews, 242,889 were 5 star reviews

- Of the 5 star reviews, none (0%) came from the Vine program

- All of the 5 star rewiews (100%) came from the Vine program

![image](https://user-images.githubusercontent.com/67409852/148726840-081e9784-f60e-40b7-baf8-d620084c0a18.png)

![image](https://user-images.githubusercontent.com/67409852/148726556-b5b8024f-4355-4193-b2d6-6605abefcda3.png)

![image](https://user-images.githubusercontent.com/67409852/148726724-70af08c5-3d01-4b1d-8cdb-f04d5b362009.png)

## Summary

- Due to the fact that none of the Vine program reviews have five stars, it's safe to say the "Vine" label arouses suspicion or mistrust in the review. Shoppers could think that Vine members are not organic customers, rather individuals astroturfing the reviews section in order to push the sales of certain books. This is the opposite of what Amazon intended.

- A jargon analysis could be performed to see if the same keywords are used in the Vine reviews that were not voted "helpful" and compare it to the keywords used in non-Vine reviews to see if comments with the same overall content are upvoted or downvoted based off of if it is a Vine review or not.
