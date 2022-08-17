# MPCS 53113 NLP Project
# Stock Movement Prediction from Twitter Sentiment Analysis

# Project Report
Project report can be found at ```doc/proect-report.pdf'''

### Steps to run the project:
1) Download the [Sentiment140 Dataset](https://www.kaggle.com/datasets/kazanova/sentiment140) and place `training.1600000.processed.noemoticon.csv` in `./data` directory.
2) Run the cells in the notebook `sentiment-classifiers.ipynb`. This will train sentiment classifier models and save them in `./data/models/sentiment-clfs/` directory.
3) Download the [market tweet dataset](https://ieee-dataport.org/open-access/stock-market-tweets-data) and place `tweets_remaining_09042020_16072020.csv` in `./data/tweets/` directory.
4) Run the cells in the notebook `sentiment-annotator.ipynb`. This will clean up the dataset and save it to `/data/tweets/dated_unnannotated_tweets.csv`. And then it will use the saved model from step 2 to annotate all the example with sentiment and save them to `./data/tweets/dated_annotated_tweets.csv`.
5) Run the cells in the notebook `stock-price-dataset.ipynb`. This will populate the dataset from step 4 with the stock price attributes for those particular organizations on those particular dates.
6) Finally run the cells in notebooks `delta-regression.ipynb` and `movement-classification.ipynb` to train stock price models.
