# Stock Price Prediction Using NLP

# NLP-stock-price-prediction

This package applies natural language processing on real time tweets to analyze how sentiment changes the stock prices.

## Data

We have scrapped the tweets real time and Appletweets.csv file for training and testing the model. The datasets are all attached in this git.
For LSTM model we have used the kaggle(https://www.kaggle.com/datasets/berkayalan/apple-stock-data-between-2015-and-2022?resource=download%5C) which consists of opening,closing,volume and date features. the sentiment and the stocks data are merged and 
used as combine.csv file.

## Model

We have fine-tuned the BERT model with live tweets and Kaggle data to predict positive, negative or neutral sentiment. The model was able to achieve 72% accuracy. The LSTM model takes two inputs from both Bert and dataset set provided and data without sentiments predicts the output based on sentiment and without sentiment.

All the necessary files need to be uploaded and executed. The libraries required are already imported in this project.

##Conclusion

The project

