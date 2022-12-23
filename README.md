# Amazon_Review_Analysis

Welcome to the Amazon Review Sentiment Analysis project! In this project, we will be using natural language processing techniques to analyze the sentiment of Amazon product reviews.

## Table of Contents
- [Project Overview](#project-overview)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
  - [Usage](#usage)
- [Project Details](#project-details)
  - [Data Collection](#data-collection)
  - [Data Preprocessing](#data-preprocessing)
  - [Sentiment Analysis](#sentiment-analysis)
  - [Evaluation](#evaluation)
- [Conclusion](#conclusion)
- [References](#references)

## Project Overview

The goal of this project is to perform sentiment analysis on Amazon product reviews in order to understand the overall sentiment of the reviews and how it changes over time. We will be using the Python Natural Language Toolkit (nltk) library to perform the sentiment analysis.

## Getting Started

### Prerequisites

In order to run the code in this repository, you will need to have the following software installed on your machine:

- Python 3
- Jupyter Notebook

You will also need to install the following Python libraries:

- nltk
- pandas
- matplotlib

### Installation

To install the required libraries, open a terminal window and run the following command:

```bash
pip install nltk pandas matplotlib
```
Once the libraries are installed, clone or download this repository to your local machine.

### Usage
To use this repository, open the Jupyter notebook file `amazon_review_sentiment_analysis.ipynb` in your local machine. Follow the instructions in the notebook to scrape Amazon reviews for a specific product and perform sentiment analysis on the reviews.

## Project Deatials
The project is divided into the following sections:

### Data Collection
In this section, we will scrape Amazon reviews for a specific product using the Beautiful Soup library. We will start by importing the necessary libraries and setting up the request headers to mimic a web browser request. Next, we will define a function to scrape the reviews for a given product. The function will take the product URL and the number of pages of reviews to scrape as inputs and return a list of dictionaries, where each dictionary represents a single review and contains the following information:
- `user_id` : The uniue id of the user
- `product_name` : The product name whic is reviewed
- `Score` : The score/star given by the user on a particular product 
- `Time` : The time when the review was been made in seconds
- `Summary` : The reduced or the lemmatized form of the review
- `Text` : The review which the user makes on the product

### [DataSet](https://drive.google.com/file/d/1Q60hjwFgOtvAtbfdwXE--A7lflDfZ0WT/view?usp=sharing)

### Data Preprocessing
In this section, we will preprocess the data by performing the following tasks:
- Removing HTML tags and special characters from the review text
- Tokenizing the review text
- Removing stop words
- Stemming the tokens

### Sentiment Analysis
In this section, we will use the nltk library to perform sentiment analysis on the preprocessed review text. We will use the nltk **`SentimentIntensityAnalyzer`** to calculate the sentiment scores for each review and classify the review as positive, negative,

or neutral based on the scores. We will also use the **`TextBlob`** library to perform sentiment analysis and compare the results with those obtained using the **`SentimentIntensityAnalyzer`**.

### Evaluation
In this section, we will evaluate the performance of the sentiment analysis model. We will calculate the following evaluation metrics:

- Accuracy: the proportion of correctly classified reviews
- Precision: the proportion of correctly classified positive reviews among all classified positive reviews
- Recall: the proportion of correctly classified positive reviews among all actual positive reviews
- F1 Score: the harmonic mean of precision and recall

We will also plot the distribution of the review ratings to visualize the overall sentiment of the reviews.

## Conclusion
In this project, we have demonstrated how to perform sentiment analysis on Amazon product reviews using the nltk library. We have also shown how to evaluate the performance of the sentiment analysis model.

## References
- Natural Language Toolkit (nltk): **[https://www.nltk.org/](https://www.nltk.org/)**
- Beautiful Soup: **[https://pypi.org/project/beautifulsoup4/](https://pypi.org/project/beautifulsoup4/)**
- Pandas: **[https://pandas.pydata.org/](https://pandas.pydata.org/)**
- Matplotlib: **[https://matplotlib.org/](https://matplotlib.org/)**
- TextBlob: **[https://textblob.readthedocs.io/](https://textblob.readthedocs.io/)**
