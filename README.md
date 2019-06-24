# NLP Task: Text Classification   

This project is a NLP task for an online interview assignment.

Main idea of this project:

The dataset contains ~1000 legal text files and 900 of them are labeled with the area of law ( i.e., `LNIND_1993_DEL_112`  has been labeled as `Criminal Laws` ), the goal is to predict the rest of the 100 files with the correct area of laws. 

Still in progress to achieve higher accuracy. 

## Introduction

#### In this project I accomplished the following things:

- Text preprocessing
- Feature extraction and evaluation
- Model selection, training, and result comparison 
- Setup pipeline and hyperparameter tuning 



------

#### Process:

###### Text Preprocessing

Tools/Libraries used: `NLTK` 

Used `WordNetLemmatizer ` to do lemmatization

###### TF-IDF

###### Fit Modeling

###### Prediction

###### Build Pipeline and tune Hyperparameters

###### Topic Modeling

------

#### Problems:

After some models built in the project, I realized that legal documents in the Natural Language Processing area is a special topic that requires different techniques and tools than regular text data. I plan to do Information Extraction on these text project first and then see will that improve the accuracy.

#### Conclusion(s)/Discussion.

##### In Progress:

- Topic Modeling (specifically for legal documents)
- Wordcloud 
- Visualization and analysis 

#### Appendix:

- Technical descriptions of (unusual) statistical procedures

- Detailed tables or computer output

- Figures that were not central to the arguments presented in the body of the report

  

##### Some Useful Links:

[Complete Guide to Parameter Tuning in XGBoost (with codes in Python)](https://www.analyticsvidhya.com/blog/2016/03/complete-guide-parameter-tuning-xgboost-with-codes-python/)

[Approaching (Almost) Any Machine Learning Problem | Abhishek Thakur](http://blog.kaggle.com/2016/07/21/approaching-almost-any-machine-learning-problem-abhishek-thakur/ )

[LexNLP: Natural language processing and information extraction for legal   and regulatory texts](https://www.groundai.com/project/lexnlp-natural-language-processing-and-information-extraction-for-legal-and-regulatory-texts/)

[approaching almost any machine learning problem](http://blog.kaggle.com/2016/07/21/approaching-almost-any-machine-learning-problem-abhishek-thakur/ )