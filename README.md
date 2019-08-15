# NLP Task: Legal Text Classification   

There are two parts of this project:

1. **[Text classification](https://github.com/FFFlora/nlp-area-of-law-classification/blob/master/Classifier.ipynb)**: The dataset contains ~1000 legal text documents and 900 of them are labeled with the corresponding area of law ( i.e., `LNIND_1993_DEL_112`  has been labeled as `Criminal Laws` ), the goal is to predict the rest of the 100 files with the correct area of laws. 
2. **[Topic Modeling](https://github.com/FFFlora/nlp-area-of-law-classification/blob/master/topic-modeling.ipynb)**: with some specific area of law selected, the goal is to extract the topics from the documents,  therefore analysis the correlation within the same area of law.



Still in progress to achieve higher accuracy. 

## Introduction

#### In this project I accomplished the following things:

- Text preprocessing
- Feature extraction and evaluation
- Model selection, training, and result comparison 
- Setup pipeline and hyperparameter tuning 
- Topic modeling
- [Data Visualization](https://kyso.io/FFFlora/nlp-area-of-law-classification/file/topic-modeling.ipynb)

------

#### Process:

###### Load Data

###### Text Cleaning and Preprocessing

Tools/Libraries used: `NLTK` ,`Lexnlp`

Used `WordNetLemmatizer ` to do lemmatization

Remove punctuations and stopwords

###### Feature Extraction

- first attempt: `TF-IDF`

>term frequency–inverse document frequency, is a 
>numerical statistic that is intended to reflect how important a word is to a document in a collection or corpus.

- second attempt: combination of `bag of words` first then `TF-IDF`

###### Fit Models

`Naive Bayes` worst performance: `32.9%`

`Logistic Regression`: 63.1% 

- Use binary classifier to solve multivariate problems

`SVM`: `57.3%`

- Decomposition first: SVD
- Standardize the data 
- Before Standardize, the performance for SVM was `18.2%`

`XGBoost`: 61.3%

*All performance scores above were in terms of test set accurary.*

###### Prediction

###### Build Pipeline and tune Hyperparameters

`GridSearchCV`

I bulit the pipeline specifically for `Logistic Regression` and `XGBoost` models since they had higher accuracy in the first place.

###### Topic Modeling

Any document seems to be a mixture of topics, especially in legal documents. Essencially, topic modeling is a text clustering problem.

Here I used `LDA`

I realize that 'to guess' how many topics in a file/ area of law is difficult.

###### Data Visualization

I used[`mglearn* ](https://github.com/amueller/mglearn) library to display the top 10 words within each specific topic model.

And  [*PyldaVis* ](https://github.com/bmabey/pyLDAvis)library was used to visualize the topic models.

The last but not least I uesd [wordcloud ](https://github.com/amueller/word_cloud)to generate the entire legal document for the selected area of law to note the most recurrent terms.

------

## Problems:

1. After some models built in the project, I realized that legal documents in the Natural Language Processing area is a very special topic that requires different techniques and tools than regular text data. I plan to do Information Extraction on these text project first and then see will that improve the accuracy. 
2. I realize that 'to guess' how many topics in a file/ area of law is difficult.

*I notice there are some powerful packages, such as [LexNLP](https://github.com/LexPredict/lexpredict-lexnlp), which deals with the NLP problems with legal documents.*

## Conclusion(s)/Discussion.

##### In Progress:

- Information Extraction

#### Appendix:

##### Some Useful Links:

[Complete Guide to Parameter Tuning in XGBoost (with codes in Python)](https://www.analyticsvidhya.com/blog/2016/03/complete-guide-parameter-tuning-xgboost-with-codes-python/)

[Approaching (Almost) Any Machine Learning Problem | Abhishek Thakur](http://blog.kaggle.com/2016/07/21/approaching-almost-any-machine-learning-problem-abhishek-thakur/ )

[LexNLP: Natural language processing and information extraction for legal   and regulatory texts](https://www.groundai.com/project/lexnlp-natural-language-processing-and-information-extraction-for-legal-and-regulatory-texts/)

[approaching almost any machine learning problem](http://blog.kaggle.com/2016/07/21/approaching-almost-any-machine-learning-problem-abhishek-thakur/ )

