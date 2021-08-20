# Restaurant Customer Reviews NLP

Hernan Trujillo


## Abstract

The purpose of this project is to analyze a dataset with 1000 restaurant reviews based on topic modeling and sentiment analysis of the reviews. Reviews sentiment can be directionally positive or negative, and in various magnitudes. By understanding the relationship between reviews and sentiment, we will be able to understand better how a restaurant can improve their customer satisfaction based on the feedback of their customers.


## Design
The project’s design was centered around unsupervised learning. I also performed topic modeling and sentiment analysis as part of the analytical framework. Together, these tools allowed me to gather insights around reviews and the overall impact on reataurant business.


## Data

1.  Data source: Kaggle.com https://www.kaggle.com/vigneshwarsofficial/reviews 
2.	Data size: 1000 documents, 2 columns  

## Methodology

*Text Preprocessing*

1.	remove digits, punctations, urls
2.	stem and tokenize - PorterStemmer
3.  remove stopwords by CountVectorizer and generate word_matrix and topic_matrix.

*Topic Modeling*

1. I used Non-Negative Matrix Factorization(NMF) to generate a word matrix and a topic matrix. The reason I chose this method over LSA is because I'm analysing a relatively small document (1000 reviews).
2.	Firstable, I set n_components=30, reducing down the components to 10, 7,5,4,3,2 respectively. 
3.	After filtering out noises, I ended up with 4 main topics for my final result. 

*Filter Out Noises*

1.	The purpose is to clean the reviews (Lower, punctuation)
2.	Used stopwords(max=1500) to filter out the number of words to reduce dimensionality. The remaining words shouldn't be too relevant.
3.	After filtering, the dataset still has 999 reviews so it’s still a decent amount.


## Tools

1. Pandas

2. Numpy

3. Sklearn  
- from sklearn.feature_extraction.text import CountVectorizer
- from sklearn.feature_extraction.text import TfidfVectorizer
- from sklearn.decomposition import NMF

4. NLTK 
- from vaderSentiment.vaderSentiment import SentimentIntensityAnalyzer

6. Plotting
- import matplotlib.pyplot as plt
- %matplotlib inline
- import seaborn as sns


## Summary

### 1. Topic Modeling Results (10 topics)

- topic_0 : food quality 
- topic_1 : place approval
- topic_2 : food quality 
- topic_3 : fidelity
- topic_4:  service
- topic_5:  food quality 
- topic_6:  fidelity
- topic_7:  place approval
- topic_8:  service
- topic_9:  food quality  

### 2. Top Modeling Results after filtering/cleaning noises (4 topics)


- topic_0: food quality 
- topic_1: place approval                                                  
- topic_2: fidelity
- topic_3: service


### 3. Sentiment Analysis 

Sentiment analysis result showed us 69% positive reviews vs 31% negative ones which compared with the initial "Liked" insight gathered in the dataset it was a big difference where it started on 50% Positive vs 50% Negative. 

This can tell us that the weight of the words after the cleaning preprocess as well as the number of times this words were repeated on each document was impactful on the results.

**Top Words**

A plot with the most repeated words make sense with the results which tellus that it can be considered on the context of the results.


 

