# Sentiment-Analysis


## Sentiment Analysis via Shallow Machine Learning Model performance

I have tried multiple vectorizers and models with hyperparameter tuning. Naive Bayes with TFIDF turned out to be the best model for our use case.

Preprocessing our text using stop words and lemmatizing makes it challenging for our model to perform. If we look at our data set, it is closely balanced. The maximum length of a sentence is 61 words.

I got an accuracy score of 81% for the training dataset and 78% for the test dataset. It is pretty decent for Shallow Machine Learning Model. Another observation, our shallow model is doing better for negative sentiments than positive sentiments with a little bit of margin. The highest value for recall of negative sentiment is 84%, and the lowest value for recall of positive sentiment is 79%

Showing five test instances in which our model was incorrect and why.

Five wrong predictions:

<img src="https://user-images.githubusercontent.com/94947162/228124171-f239c583-01a1-4812-a876-2b358abef668.png" style="width: 400px;">

If we look at these five predictions, it is even difficult for humans to classify them.

Removing stop words from our dataset changed the entire meaning of sentences. For example, removing the 'not' stopword from "not recommended" changes the semantics completely. These instances have both positive and negative words in a sentence which might have confused our model while making a prediction. Few statements look sarcasm, making it difficult for the Shallow model to classify them. In the case of the first example, the shallow model couldn't understand the value of the number here and hence ended up classifying them incorrectly. As a future improvement to the model, we can change numbers into words as part of preprocessing so that our model won't miss out on those instances.

## Sentiment Analysis via Deep Machine Learning Model performance

I have tried Distilbert and Roberta Deep ML Models. I got an accuracy of 94.5% for the test dataset. Only 33 predictions were wrong. 
