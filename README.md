# LSTM-based-Language-Model

This project implements a Language Model that can predict the next Word using a Long Short-Term Memory (LSTM) neural network. The predictor takes a sequence of words as input and predicts the most likely next word. This can be useful for applications such as text auto-completion and language modeling.

## Table of Contents
1. [Introduction](#1-introduction)
2. [Features](#2-features)
3. [Installation](#3-installation)
4. [Usage](#4-usage)
5. [Evaluation](#5-evaluation)
6. [Contribution](#6-contribution)

## 1. Introduction
This project focuses on developing a next-word prediction model using an LSTM network. The model is trained on a large corpus of text data to understand and predict the sequence of words. LSTM networks are a type of Recurrent Neural Network (RNN) that are particularly well-suited for sequence prediction tasks.

## 2. Features
- Preprocesses text data for training the model.
- Uses LSTM neural network for sequence prediction.
- Evaluate model performance using accuracy metrics.
- Provides functionality to predict the next word given a sequence of words.

## 3. Installation
To install and run this project, follow these steps:

1. Clone the repository:
   ```bash
   git clone https://github.com/rajatbutola/LSTM-based-Language-Model.git
   cd Next-Word-Predictor

## 4. Usage
To use the next word predictor:

### 4.1. Prepare the Data:
- Ensure you have a dataset of text for training.
- Modify the data preprocessing script if necessary.

### 4.2. Train the Model:
- Run the training script to train the model on your dataset.

### 4.3. Predict the Next Word:
- Use the trained model to predict the next word in a sequence.

   ```python

    text = "Advanced biology research also"
    
    for i in range(10):
      # tokenize
      token_text = tokenizer.texts_to_sequences([text])[0]
      # padding
      padded_token_text = pad_sequences([token_text], maxlen=27, padding='pre')
      # predict
      pos = np.argmax(model.predict(padded_token_text))
   ```

## 5. Evaluation
Output: A word-by-word output of up to 10 words is predicted for the above-given sentence. This length can be varied. The evaluation script provides a detailed analysis of the model's prediction capabilities.

```bash
1/1 [==============================] - 0s 35ms/step
Advanced biology research also was
1/1 [==============================] - 0s 29ms/step
Advanced biology research also was underway
.
.
.
.
.
.
1/1 [==============================] - 0s 46ms/step
Advanced biology research also was underway aboard the orbiting lab on thursday with
1/1 [==============================] - 0s 29ms/step
Advanced biology research also was underway aboard the orbiting lab on thursday with astronauts
```


## 6. Contribution

Contributions are welcome! Please submit a pull request or open an issue for any feature requests or bug report. For major changes, please open an issue first to discuss what you would like to change.
