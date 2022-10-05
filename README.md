# We-Rate-Dogs-Twitter-Archive-Data-Wrangling
# Introduction

-  The dataset I have wrangled is the tweet archive of Twitter account called @dog_rates_(https://twitter.com/dog_rates), also known as WeRateDogs (https://twitter.com/dog_rates). WeRateDogs is a Twitter account that rates people's dogs with a humorous comment about the dog.


-  In this report I will briefly describe my Wrangling efforts done on the data associated with WeRateDogs Twitter account

![dog image](https://user-images.githubusercontent.com/89153467/194123382-ba936287-f74a-44fd-8158-f22c362c839c.jpg)

# Project Details

For this project, we only wanted original ratings (no retweets) that have images. Not all of the original tweets in the dataset are dog ratings and some are retweets.

Fully assessing and cleaning the entire dataset would require exceptional effort so only a subset of its issues (eight quality issues and two tidiness issues at minimum) needed to be assessed and cleaned.

The tasks for this project were:

- Data wrangling, which consisted of:
- Gathering data
- Assessing data
- Cleaning data
- Storing, analyzing, and visualizing the wrangled data
- Reporting on my data analyses and visualizations (act_report.pdf)

# The Data
WeRateDogs provided their Twitter archive (which included tweets through August 1, 2017) of basic tweet data (tweet ID, timestamp, text, etc.) for use with this project. The "enhanced" csv file (twitter_archive_enhanced.csv) also contains columns which were extracted programatically: the rating numerator, rating denominator, dog's name, and dog stages (doggo, floofer, pupper, and puppo). These columns needed to be assessed and cleaned as the extraction process wasn't perfect.

The provided Twitter archive lacked some useful information: retweet count and favorite count. I used the tweet IDs to query the Twitter API for each tweet's JSON data using Python's Tweepy library and stored each tweet's entire set of JSON data in a file called tweet_json.txt. I then read the txt file line by line into a pandas DataFrame only including the desired variables; retweet count and favorite count.

Udacity also provided a link to image_predictions.tsv which I downloaded programatically using the Requests library.
