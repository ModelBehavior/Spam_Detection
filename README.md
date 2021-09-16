# [Project 4: Wait Thats Spam!](https://github.com/ModelBehavior/Spam_Detection/blob/main/Spam%20Prediction.Rmd)

## Sentiment Analysis and Prediction of SMS Messages

# Questions:
+ Can we use this data to predict if a SMS message is spam?
+ What are the most common positive words?
+ What are the most common negative words?
+ What are the most important positive and negative words as described by the model? 

# Data
The dataset can be found [here](https://www.kaggle.com/uciml/sms-spam-collection-dataset). The SMS Spam Collection Dataset is a set of SMS tagged messages that have been collected for SMS Spam research. It contains one set of SMS messages in English of 5,574 messages, tagged acording being ham (legitimate) or spam.

# Methods
I used comparison word cloud for the most common positive and negative words. The size of a word's text is in proportion to its frequency within its sentiment. I used bing word bank for the sentiment analysis. I chose a lasso logistic model. This model does well on text data. I used single word tokens, convert tokens into weights using tfidf, only kept 500 tokens after removing stop words. The model is sensitive to centering and scaling, so I normalized the data. I used grid search to find the best penalty. I used bootstrap resampling to test the model before running the final model on the test set. It's easier to detect non-spam SMS messages than it is to detect spam SMS messages. Our overall accuracy rate is good at 96%

# Results
![](/images/project4_img1)
![](/images/project4_img2)

# Limitations and Next Steps
Things we can do to get better results: include not only unigrams but bi-grams, tri-grams, what stopwords make the most sense for my data, include more words in the word bank (I only included 500), we could choose a different weighting other than tfidf, we could try other types of models such as SVM or Naive Bayes.
