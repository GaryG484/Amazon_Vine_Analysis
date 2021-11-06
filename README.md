# Amazon_Vine_Analysis
### Overview
##### I was tasked with determining if there was a bias created by Amazon’s vine paid review service.
##### Using [Google Colab]( https://colab.research.google.com) and PGAdmin I downloaded a dataset using [video game review data]( https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Video_Games_v1_00.tsv.gz) provided by amazon. With PG Admin I separated the cvs file into four separate tables: customers_table, products_table, review_id_table, and vine_table. I then used google colab with spark to read the data from a server and count how many vine reviews out of total five star reviews there were, and determine if there is a bias caused by the paid review program. 
#### Results
##### The results of my analysis follow:
•	There were 4, 291 vine reviews in the data set and 40,471 non-vine reviews. Vine reviews make up roughly 10% of the reviews.
•	![Alttext]( https://github.com/GaryG484/Amazon_Vine_Analysis/blob/main/images/vine5starreviews.JPG)

•	Of the dataset, 15,711 were 5-star reviews. This makes up about 38.2% of the dataset.
•	![Alttext]( https://github.com/GaryG484/Amazon_Vine_Analysis/blob/main/images/Total5starreviews.JPG)

•	Of the 15711 5-star reviews, 15,663 were non-vine. This makes up about 38.9% of the dataset

![Alttext]( https://github.com/GaryG484/Amazon_Vine_Analysis/blob/main/images/percentagenonvine5starreviews.JPG)

•	Of the 15711 5-star reviews, 48 were vine reviews, which is lower than 1% of the 5-star reviews.
•	![Alttext]( https://github.com/GaryG484/Amazon_Vine_Analysis/blob/main/images/percentagevine5starreviews.JPG)

#### Summary
##### Vine reviews make up a roughly one tenth of all reviews, but only one percent of the 5-star reviews. This shows that there may be a negative bias for paid reviews, and that vine reviewers review products more harshly than their unpaid counterparts. With the data provided we could run a regression to confirm a correlation between vine reviewers and the number of stars they give a product. Also, we should look at what rating a vine reviewer is likely to give compared to their unpaid counterparts. 
