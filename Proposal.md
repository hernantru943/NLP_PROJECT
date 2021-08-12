# Restaurnt Customer Reviews

### Question/need:

- What is the framing question of your analysis, or the purpose of the model/system you plan to build?

How a restaurant can improve their customer satisfaction based on the reviews of their clients.

- Who benefits from exploring this question or building this model/system?

A top restaurant located in downtown Chicago.

### Data Description:

The dataset consists of 1000 rows and 2 columns. Review Column consist of customer reviews and like column consist of 0 and 1. If the review is positive, 1 and if negative, 0.

- What dataset(s) do you plan to use, and how will you obtain the data?

a Database from Kaggle https://www.kaggle.com/vigneshwarsofficial/reviews

- What is an individual sample/unit of analysis in this project? What characteristics/features do you expect to work with?

-If modeling, what will you predict as your target?

For modeling I'd use the positive or negative review identified as the column "Liked" where 1 is positive and 0 is negative.

### Tools:

- How do you intend to meet the tools requirement of the project?

* Initial EDA using Pandas
* Python text processing libraries/tools (such as NLTK, spaCy, gensim, scikit-learn)
* Visualization tools will include python libraries such as Plotly or resources outside of python such as Tableau.

- Are you planning in advance to need or use additional tools beyond those required?

Not by now

### MVP Goal:

What would a minimum viable product (MVP) look like for this project?

a minimum MVP could be a base Logistic Regression Model  with an initial F1 score.

