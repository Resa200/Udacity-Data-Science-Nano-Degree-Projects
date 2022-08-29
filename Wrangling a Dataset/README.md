## Wrangling a Dataset - WeRateDogs 

WeRateDogs is a Twitter account that rates people's dogs with a humorous comment about the dog. These ratings almost always have a denominator of 10. The twitter account has garnered over 9 million followers and has been active since November 2015.
With over 2000+ tweets from the Twitter account, we have answered popular questions from what makes a tweet get high likes to what breed gets the most liked!!

### Datasets

##### Enhanced Twitter Archive:
Udacity provided this data which contains basic tweet data for all 5000+ of the WeRateDogs tweets, but not everything. One column the archive does contain though: each tweet's text, which was used to extract rating, dog name, and dog "stage" (i.e. doggo, floofer, pupper, and puppo) to make this Twitter archive "enhanced." Of the 5000+ tweets, Udacity has filtered for tweets with ratings only (there are 2356).

##### Additional Data via the Twitter API
retweet count and favorite count are two of the notable column omissions. Fortunately, this additional data can be gathered by anyone from Twitter's API. Well, "anyone" who has access to data for the 3000 most recent tweets, at least.I didn't get access to to developer account so I used a json file provided by Udacity for this project.

##### Image Predictions File
Udacity provided an image predictions file which is the end result of running every image in the WeRateDogs Twitter archive through a neural network that can classify breeds of dogs*. The results: a table full of image predictions (the top three only) alongside each tweet ID, image URL, and the image number that corresponded to the most confident prediction (numbered 1 to 4 since tweets can have up to four images).


### Data Wrangling

**Data Gathering**: The three different datasets were gathered using different formats. The enhanced_twitter-archive.csv was downloaded and read into a pandas data frame for assessment. The image predictions file was downloaded programmatically using the requests library. The third dataset should have been queried from twitter but due to issues with getting a twitter developer account, I read a downloaded json file containing data on retweet and favorite count into a data frame. 

**Data Assessing**: The next stage after gathering the data was to assess for tidiness and quality. I had to use visual and programmatic assessment that was taught during the course to correctly identify issues with the data’s quality and tidiness. I had to use the 
.info(),.head(),.sample() and so on to identify at least 8 quality issues and 2 tidiness issues.

**Data Cleaning**: This had to be the hardest part of the process for me, I had to learn new pandas functions to manipulate data and clean data. Melting 4 columns into one had to be the greatest challenge for this project. All highlighted issues were cleaned perfectly in the 
jupyter notebook. The cleaned dataset was stored in a new csv file which would be used for analysis. 


### Summary of Findings

This can be found in the **act_report.pdf** [link](https://github.com/Resa200/Udacity-Data-Science-Nano-Degree-Projects/blob/main/Wrangling%20a%20Dataset/act_report.pdf)
