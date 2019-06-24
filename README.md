# Recommendations with IBM Project

### Table of Contents

1. [Project Overview](#overview)
2. [Project Tasks](#tasks)
3. [Installation](#installation)
4. [File Descriptions](#files)
5. [Results](#results)
6. [Licensing, Authors, and Acknowledgements](#licensing)

## Project Overview<a name="overview"></a>

IBM Watson Studio platform has an online data science community where members can post tutorials, notebooks, articles, and datasets. In this project, we will build a recommendation engine based on user behavior and community network data, to surface content most likely to be relevant to a user.

For this project, we will analyze the interactions that users have with articles on the [IBM Watson Studio platform](https://dataplatform.cloud.ibm.com/), and make recommendations to them about new articles we think they will like. Below we can see an example of what the dashboard could look like displaying articles on the IBM Watson Platform.

<img src="IBM Watson Recommendations sample snapshot.png">

Though the above dashboard is just showing the newest articles, you could imagine having a recommendation board available here that shows the articles that are most pertinent to a specific user.

In order to determine which articles to show to each user, you will be performing a study of the data available on the IBM Watson Studio platform. You can create your own account to become a part of their community, and get a better understanding of their data [by creating an account on the platform here](https://dataplatform.cloud.ibm.com/).

## Project Tasks<a name="tasks"></a>

The Project is divided in the following tasks:

1. Exploratory Data Analysis - Before making recommendations of any kind, we will need to explore the data we are working with for the project. Dive in to see what we can find. There are some basic, required questions to be answered about the data we are working with throughout the rest of the notebook. Use this space to explore, before we dive into the details of our recommendation system in the later sections.

2. Rank Based Recommendations - To get started in building recommendations, we will first find the most popular articles simply based on the most interactions. Since there are no ratings for any of the articles, it is easy to assume the articles with the most interactions are the most popular. These are then the articles we might recommend to new users (or anyone depending on what we know about them).

3. User-User Based Collaborative Filtering - In order to build better recommendations for the users of IBM's platform, we could look at users that are similar in terms of the items they have interacted with. These items could then be recommended to the similar users. This would be a step in the right direction towards more personal recommendations for the users. We will implement this next.

4. Content Based Recommendations - Given the amount of content available for each article, there are a number of different ways in which someone might choose to implement a content based recommendations system. Using our NLP skills, we might come up with some extremely creative ways to develop a content based recommendation system. We are encouraged to complete a content based recommendation system.

5. Matrix Factorization(user-item collaborative filtering with SVD without regularization) - Finally, we will complete a machine learning approach to building recommendations. Using the user-item interactions, we will build out a matrix decomposition. Using our decomposition, we will get an idea of how well we can predict new articles an individual might interact with (spoiler alert - it isn't great). We will finally discuss which methods we might use moving forward, and how we might test how well our recommendations are working for engaging users.

## Installation<a name="installation"></a>

* Python 3.5+ (I used Python 3.6)
* Data Processing & Machine Learning Libraries: NumPy, Pandas, Sciki-Learn 
* Natural Language Process Libraries: NLTK
* Data Visualization: Matplotlib

The following packages also need to be installed for nltk:

  - punkt
  - wordnet
  - averaged_perceptron_tagger
  - stopwords

## File Descriptions<a name="files"></a>

1. data(folder)
    - articles_community.csv: dataset including artciles detailed information
    - user-item-interactions.csv: dataset including all the user-item interactions
2. code files
    - Recommendations_with_IBM.ipynb: jupyter notebook containing all the code for recommendations
    - project_tests.py: test file to test the solutions to the questions in jupyter notebook
3. pickle files
    - top_5.p, top_10.p, top_20.p: pickle files containing top_5, top_10 & top_20 recommendations respectively
    - user_item_matrix: pickle file containig user_item matrix
4. html file
    - Recommendations_with_IBM.html: html version of the jupyter notebook(html file produced at the end of jupyter notebook)

## Results <a name="results"></a>
* [Project Notebook: Recommendations-with-IBM](https://nbviewer.jupyter.org/github/gauravansal/Recommendations-with-IBM/blob/master/Recommendations_with_IBM.ipynb) 

## Licensing, Authors, and Acknowledgements<a name="licensing"></a>

<a name="license"></a>
### License
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

<a name="acknowledgement"></a>
### Acknowledgements

This app was completed as part of the [Udacity Data Scientist Nanodegree](https://www.udacity.com/course/data-scientist-nanodegree--nd025). Starter code templates and data were provided by Udacity. The data was originally sourced by Udacity from [IBM Watson Studio platform](https://dataplatform.cloud.ibm.com/).