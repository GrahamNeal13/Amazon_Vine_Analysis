# Amazon_Vine_Analysis
Module_16

## Overview:
Using one of 50 datasets and PySpark to perform the ETL process to extract the dataset, transform the data, connect to an AWS RDS instance, and load the transformed data into pgAdmin. Next, you’ll use PySpark and Pandas to determine if there is any bias toward favorable reviews from Vine members in your dataset.

### Tools used:
  + Pyspark
  + PGAdmin
  + Pandas
  + Jupyter Notebook
  + Google Colab
  + Amazon Web Services(AWS)

### Background:
"Since your work with Jennifer on the SellBy project was so successful, you’ve been tasked with another, larger project: analyzing Amazon reviews written by members of the paid Amazon Vine program. The Amazon Vine program is a service that allows manufacturers and publishers to receive reviews for their products. Companies like SellBy pay a small fee to Amazon and provide products to Amazon Vine members, who are then required to publish a review."

## Results:
By using Pyspark and Google Colab I was able to use the dataset for watches to create a dataframe and begin filtering the data for the number of reviews that the vine program produced.  Within this process I was able to make four tables that would filter the data into PGAdmin tables.  

  + The first table was the Customers Table:

![customers_table.png](https://github.com/GrahamNeal13/Amazon_Vine_Analysis/blob/main/resources/customers_table.png)

  + The second table was for the Products Table:
  
![products_table.png](https://github.com/GrahamNeal13/Amazon_Vine_Analysis/blob/main/resources/products_table.png)
  
  + The third table was for the Review ID Table:

![rename_id_table.png](https://github.com/GrahamNeal13/Amazon_Vine_Analysis/blob/main/resources/rename_id_table.png)

  + The fourth table was for the Vine Table:

![vine_table.png](https://github.com/GrahamNeal13/Amazon_Vine_Analysis/blob/main/resources/vine_table.png)

Now that the data was sorted I could begin filtering the data for analysis.  I was hoping to see that the vine program was the leading source of 5 star reviews and that by allowing people to try and then endorse the products we would see an increase in sales of those products.  But there was only a total of 15 Vine reivews that were 5 stars.  

![vine_percent.png](https://github.com/GrahamNeal13/Amazon_Vine_Analysis/blob/main/resources/vine_percent.png)

However I found that the percentage of 5 star reviews of the vine promoters was actually quite small.  This leads me to believe that perhaps there just was not a lot of 5 star reviews in the collected dataset.  But on close inspection I found that too, to not be the case with a sample total of 4,531 5 star reviews.

![5star_percent.png](https://github.com/GrahamNeal13/Amazon_Vine_Analysis/blob/main/resources/5star_percent.png)

Now this made me look at the non-vine group to see if the general public was producing such a low percentage of the 5 star reviews.  Surprisingly there were 4,332 5 star reviews from the non-vine group.  

![nonvine_percent.png](https://github.com/GrahamNeal13/Amazon_Vine_Analysis/blob/main/resources/nonvine_percent.png)


## Summary: It's just not worth it.

After seeing the large percentage of 5 star reviews coming from non-vine promoters it did bring the conclusion that a small promotional group could in fact have such a large following that the public could be following the promoted reviews and purchasing the watches on their own.  Though we did a bit of filtering on the original dataset, taking the original CSV and making it a dataframe then creating a new dataframe with the rows that had equal to or greater than 20 pick reviews.  Then filtering that dataframe for rows where the number of helpful votes was divided by the total votes is equal to or greater than 50%.  So the original data had been filtered quite a bit.  So upon inspection of seeing how small the sample was of the total population we see that our selection was only 1% of the original dataset.  

![add_summary.png](https://github.com/GrahamNeal13/Amazon_Vine_Analysis/blob/main/resources/add_summary.png)

Now we can see that while the vine program may produce a small increase in sales, with a large consumer group base it is just not producing enough 5 star reviews for the program to be worthwhile.  Which is a disappointment as these particular customers have received special treatment and are not generating enough 5 star reviews to make it worth the while of the seller to continue this program.  
I recommend ending this program for watches as the product itself is such a well selling product it does not need a promotional program like the Amazon Vine program.  


