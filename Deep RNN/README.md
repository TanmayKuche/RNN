# Deep RNN Architecture for Sentiment Analysis

This project implements a **deep Recurrent Neural Network (RNN)** for sentiment analysis on text data. The model consists of an **Embedding** layer followed by two stacked **SimpleRNN** layers and a **Dense** output layer with a sigmoid activation for binary classification.

## Model Architecture

### Overview:
1. **Embedding Layer**: Transforms the input integer sequences into dense vectors of fixed size.
2. **First SimpleRNN Layer**: A recurrent layer that returns sequences for the next RNN layer to process. Regularized with L2 penalty.
3. **Second SimpleRNN Layer**: A second RNN layer that processes the output from the previous layer. Regularized with L2 penalty.
4. **Dense Layer**: A fully connected layer that outputs a probability (0 or 1) for binary classification.


### Validation Accuracy -- 81.54
