# Amazon-Vine-Analysis
This project conducts ETL using AWS cloud services and analyzes for bias in PySpark.

## Overview ##
This project used several tools to manage "big data" - as my primary dataset had 3 million rows. For this reason, I used AWS (specifically RDS and S3) to store my dataset in the cloud. PySpark and SQL allowed me to analyze this dataset for potential biased reviews among sponsored and unsponsored purchasers. 

## Analysis ##

The "Vine" program sends merchandise to subscribers, who are then encouraged to post reviews. The company wants to determine whether these reviews skewed positive - that is to say, are subscribers who receive free merchandise more likely to post positive reviews?

### Results

<img width="742" alt="Screen Shot 2022-03-31 at 9 50 32 PM" src="https://user-images.githubusercontent.com/95657458/161179001-5bca7e01-1906-4405-92a1-589e03b32fb7.png">

(Vine Reviews vs. Non-Vine Reviews)
* There were a total of 2 vine reviews and 3,105,513 non-vine reviews in this dataset. 
* There were 0 5-star vine reviews and 403,807 5-star non-vine reviews in this dataset. 
* 13% of Vine reviews were 5-stars

<img width="714" alt="Screen Shot 2022-03-31 at 9 56 48 PM" src="https://user-images.githubusercontent.com/95657458/161179592-8b231e5c-9408-426c-a847-7a2919191cee.png">

### Summary

I chose a dataset of book reviews, and this had only 2 paid subscribers in this subsection of merchandise. This is an expected outcome, because book content can vary widely and is not guaranteed to provide a positive review. Whether or not a customer will enjoy a book is contingent upon too many factors to control. Additionally, it's possible that the customer may not even read the book, let alone leave any review. 


<img width="825" alt="Screen Shot 2022-03-31 at 9 50 59 PM" src="https://user-images.githubusercontent.com/95657458/161179066-7c7aba11-b304-4819-814e-93000a2b6b45.png">

However, I still wanted to determine whether the book reviews from customers who purchased it themselves still skewed positive. And unsurprisingly, it did not. Only 13% of reviewers left a 5-star review on their purchase, so I concluded that there was little to no bias present in these reviews. This is unfortunate for the authors of these texts - and likely also confirms that Amazon can continue to avoid sending books to random subscribers (unnless they are willing to collect more data to ensure that the subscriber is more likely to enjoy the content of the book).

