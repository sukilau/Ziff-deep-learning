# Tweets Sentiment Analysis using VADER, linear SVM and NLP techniques (AUC=0.806)

Tweets Sentiment Analysis (positive or negative) using NLTK VADER Sentiment Intensity Analyzer and scikit-learn in Python 3.6.0.


## What is in this repo

*sentiment-analysis.py*  

* An implementation of NLTK VADER Sentiment Analyzer, CounterVectorizer, TfidfTransformer, SVC are trained against 2001 labeled tweets using 10-fold cross validation.

* NLTK VADER Sentiment Analyzer works well to identify polarity of sentiments expressed in social media contexts, thus it is used to compute the polarity scores (positive, negative, netural) for each tweet (without text preprocessing) in the study. This step creates a feature vector (dim = 3) for each tweet.

* Next, text preporcessing (eg. remove html tag, @tag, numbers and symbols) is done for each tweet before feeding into CountVectorizer to tokenize the tweets and create Bag of Words. TfidfTransformer is then applied to normalize the count matrix to tf-idf representation. This step creates a feature vector (max_features = 5000) for each tweet.

* The two feature vectors created above are combined to form a new feature vector. The new feature vectors are used to train SVC model.

* Grid search is used to find the best parameter set of SVC. Best parameter set : {'C': 0.5, 'kernel': 'linear'}.

* Evaluation on area under ROC curve is made using 10-fold cross validation.  Best AUC score = 0.806 (+/-0.062) for the parameter set {'C': 0.5, 'kernel': 'linear'}.


*model-comparison-01.py, model-comparison-02.py, model-comparison-03-word2vec.py*

* The dataset is also tested against other methods, eg. with or without VADER, using different classifiers, Word2Vec.

* Among all other methods in the study, VADER + CountVectorizer + TfidfTransformer + SVC (linear kernel) / SGDClassifier (linear SVM) achieves the best AUC score so far.


## Model Evaluation
 
| Classifiers                                                            |  AUC   |
| -----------------------------------------------------------------------|-------:|
| VADER + SVC                                                            |  74.7% |
| CountVectorizer + MultinomialNB                                        |  76.7% |
| CountVectorizer + TfidfTransformer + MultinomialNB                     |  77.9% |
| VADER + CountVectorizer + TfidfTransformer + SVC                       |  80.6% |
| VADER + CountVectorizer + TfidfTransformer + LinearSVC                 |  80.4% |
| VADER + CountVectorizer + TfidfTransformer + SGDClassifier             |  80.6% |
| VADER + CountVectorizer + TfidfTransformer + RandomForestClassifier    |  79.5% |
| Word2Vec + RandomForestClassifier                                      |  65.8% |

