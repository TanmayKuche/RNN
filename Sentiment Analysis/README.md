# Sentiment Analysis on IMDB Movie Reviews using RNN

This project demonstrates sentiment analysis on the IMDB movie review dataset using a Recurrent Neural Network (RNN) with Keras. The model classifies movie reviews into positive or negative based on the text.

## 🎯 Project Overview
This project uses the IMDB dataset of movie reviews, which consists of 25,000 training samples and 25,000 testing samples. Each review is associated with a label (`1` for positive and `0` for negative sentiment).

The task is to train a Recurrent Neural Network (RNN) to predict the sentiment of a review based on its text. We will utilize the Keras API to build and train the model, which consists of an embedding layer followed by a Simple RNN layer and a dense output layer.

## Architecture

### EMBEDDING <br>
The **Embedding layer** is used to convert the input words into dense vectors of fixed size. This is an essential part of processing text data. <br>
- **input_dim=10000**: The vocabulary size (top 10,000 most frequent words). <br>
- **output_dim=32**: The dimension of the dense vector for each word. <br>
- **input_shape=(100,)**: Each review is represented by 100 words, and each word is mapped to a vector of size 32. <br>

### SIMPLE RNN <br>
The **Simple RNN layer** processes the sequence data and captures temporal dependencies in the data. In this case, we have two **LSTM** layers instead of a simple RNN, but if you want to use a simple RNN, here's how it would work: <br>
- This layer will take the embedding layer output and process the sequence of words. <br>
- The **Simple RNN** layer will capture the patterns in the sequence. <br>
- In the model you provided, **LSTM** layers are used, which are more efficient than simple RNN layers for long sequences. <br>

### DENSE <br>
The **Dense layer** is a fully connected layer and is typically used at the end of the model for prediction. In this case, it outputs the final classification. <br>
- The **output_dim=1**: The output of the model is a single value that classifies whether a review is positive or negative. <br>
- The **activation** is typically **sigmoid** for binary classification tasks, which maps the output to a value between 0 and 1. <br>

## Accuracy
#### Validation Accurcy: ~80
