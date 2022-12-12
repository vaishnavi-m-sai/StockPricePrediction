# Stock Price Prediction Using NLP

# NLP-stock-price-prediction

This package applies natural language processing on real time tweets to analyze how sentiment changes the stock prices.

## Data

We have scrapped the tweets real time and Appletweets.csv file for training and testing the model. The datasets are all attached in this git.
For LSTM model we have used the kaggle(https://www.kaggle.com/datasets/berkayalan/apple-stock-data-between-2015-and-2022?resource=download%5C) which consists of opening,closing,volume and date features. the sentiment and the stocks data are merged and 
used as combine.csv file.



## Model

The model predicts the daily movement of the Dow Jones Industrial Average (DJIA).  The task is formulated as a binary classification task:
- `0` when DJIA Adj Close value decreased
- `1` when DJIA Adj Close value rose or stayed as the same

The model was found to have ~95% accuracy when analyzing news from the same day. When forecasting tomorrows market movements, accuracy fall to under 60%

## Architecture

The majority of model accuracy can be attributed to NLP processing of r/worldnews. Lemmatizing was used on a feature set of 20,000 words, accuracy was seen to improve dramatically with word count.

Analysis of text sentiment and subjectivity also contributed positively. Interpolation and Principal Component Analysis were both found to be useful when cleaning and engineering the Yahoo Finance dataset.

## How to use

The model is executed as a series of bash scripts.

First, the two datasets are cleaned are processed:

```
python3 news.py
python3 number.py
```

Next, the two resultant cleaned datasets are merged:

```
python3 merge.py
```

Finally, the merged dataset is processed to train a logistic regression model:

```
python3 model.py
