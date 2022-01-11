# _WeRateDogs_ Twitter Data from 2015 to 2017
#### [_Udacity - Data Analyst Nanodegree:_](https://www.udacity.com/course/data-analyst-nanodegree--nd002) _Project 4 - Wrangle and Analyze Data_
## Table of Contents

1. [Introduction](#introduction)
2. [Project Overview](#project)
3. [Requirements](#requirements)
4. [Project Movitivation](#motivation)
5. [Key Files](#files)
6. [Results](#results)
7. [Acknowledgements](#acknowledgements)

### 1. Introduction<a id="introduction"></a>
Real-world data rarely comes clean. Using Python and its libraries, I gathered data from a variety of sources and in a variety of formats, assessed its quality and tidiness, then cleaned it. This is called data wrangling. I documented my wrangling efforts in a Jupyter Notebook, then showcased them through analyses and visualizations using Python and its libraries.

The dataset that I wrangled (and analyzing and visualizing) was the tweet archive of Twitter user @dog_rates, also known as WeRateDogs. WeRateDogs is a Twitter account that rates people's dogs with a humorous comment about the dog. These ratings almost always have a denominator of 10. The numerators, though? Almost always greater than 10. 11/10, 12/10, 13/10, etc. Why? Because "they're good dogs Brent." WeRateDogs has over 4 million followers and has received international media coverage.

WeRateDogs downloaded their Twitter archive and sent it to Udacity via email to use in this project. This archive contains basic tweet data (tweet ID, timestamp, text, etc.) for all 5000+ of their tweets as they stood on August 1, 2017.

<p align="center">
  <img width="482" alt="WRD_twitter_banner" src="https://user-images.githubusercontent.com/68494141/148898814-5c45e176-f36e-4895-be21-9cde60124cd0.png">
</p>

### 2. Project Overview<a id="project"></a>
The flow of the project was as follows:

* Step 1: Gathering data
* Step 2: Assessing data
* Step 3: Cleaning data
* Step 4: Storing data
* Step 5: Analyzing, and visualizing data
* Step 6: Reporting
  - My data wrangling efforts
  - My data analyses and visualizations

### 3. Requirements<a id="requirements"></a>

This project was created in a Jupyter Notebook made available via Anaconda and written in python.\ 
The following versions of languages and libraries were used in creating this project:
- python==2.7.18
- ipython==7.31.0
- matplotlib==3.5.1
- numpy==1.22.0
- pandas==1.3.5
- requests==2.27.1
- scipy==1.7.3
- seaborn==0.11.2
- tweepy==4.4.0

### 4. Project Motivation<a id="motivation"></a>

The goal: wrangle WeRateDogs Twitter data to create interesting and trustworthy analyses and visualizations. The Twitter archive is great, but it only contains very basic tweet information. Additional gathering, then assessing and cleaning is required for "Wow!"-worthy analyses and visualizations.

The overall purpose of this Udacity project was to refine our data wrangling skills with secondary importance on delivering multiple polished visualzations and tell a story or solve a problem. In other words, the journey was more important than the destination. 

## 5. Key Files<a id="files"></a>
- `twitter_archive_enhanced.csv`\
The WeRateDogs Twitter archive contains basic tweet data for all 5000+ of their tweets, but not everything. One column the archive does contain though: each tweet's text, which Udacity used to extract rating, dog name, and dog "stage" (i.e. doggo, floofer, pupper, and puppo) to make this Twitter archive "enhanced." Of the 5000+ tweets, only those tweets with ratings were filtered.
The data was extracted programmatically by Udacity, but the data was left messy on purpose. The ratings aren't all correct. Same goes for the dog names and probably dog stages (see below for more information on these) too. I had to assess and clean these columns to use them for analysis and visualization.

- `tweet_json.txt`\
Resulting data queried using Twitter's API. It was necessary to gather the retweet count and favorite count which were omitted from the basic `twitter_archive_enhanced.csv`. 

- `image-predictions.tsv`\
Udacity ran every image in the WeRateDogs Twitter archive was through a neural network that can classify breeds of dogs. The results: a table full of image predictions (the top three only) alongside each tweet ID, image URL, and the image number that corresponded to the most confident prediction (numbered 1 to 4 since tweets can have up to four images).

- `wrangle_act.ipynb`\
This contains the bulk of the project. This notebook contains all code for gathering, assessing, cleaning, analyzing, and visualizing data.

- `wrangle_report.pdf`\
This was a report for documenting the data wrangling process: gather, assess, and clean.

- `act_report.pdf`\
Documentation of analysis and insights

- `twitter_archive_master.csv`\
Cleaned and merged dataset containing data from the 3 source data sets


### 6. Results<a id="results"></a>
As said in the project motivation, the data wrangling process itself was more relevant than uncovering insights. At any rate, I was able to answer the following 4 questions:
1. **What is the most retweeted tweet?**\
From the data I had from 2015 to 2017, [this gem was the most retweeted tweet](https://twitter.com/dog_rates/status/744234799360020481).
2. **What is the most common rating?**\
12/10
3. **What are the most common breeds found by the neural network?**\
The top 5, from less to most common, were Pug, Chihuahua, Welsh Corgi, Labrador Retriever, then finally Golden Retriever. 
4. **What is the average retweet count for each rating?**

<p align="center">
  <img width="605" alt="Screen Shot 2022-01-11 at 21 22 39" src="https://user-images.githubusercontent.com/68494141/148941805-da0b6ab3-cc4f-4eab-8ef4-55d1c06fa630.png">\
</p>

I saw a general positive correlation between dog rating and retweet count (i.e. popularity). 13/10 and 14/10 tweets had the most retweets on average.\ 
Further details of the results can be seen in the [`act_report.pdf`](https://github.com/keenan-cooper/WeRateDogs-Twitter-Data-from-2015-to-2017/blob/main/03_act_report.pdf) file.

### 7. Acknowledgements<a id="acknowledgements"></a>
This project wa completed as part of the [Data Analyst Nanodegree[nd002-syllabus_2018-June_v9.pdf](https://github.com/keenan-cooper/WeRateDogs-Twitter-Data-from-2015-to-2017/files/7847764/nd002-syllabus_2018-June_v9.pdf)
]All data provided and sourced by [Udacity](https://www.udacity.com). 
