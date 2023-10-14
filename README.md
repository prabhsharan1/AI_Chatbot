# AI Chatbot

This repository contains the code for an AI chatbot implemented in Python using TensorFlow and NLTK. The chatbot is designed to provide responses to user queries related to a specific domain, such as college inquiries. This README provides an overview of the code and instructions for setting up and using the chatbot.

## Prerequisites

Before using this AI chatbot, ensure you have the following dependencies installed on your system:

- Python 3.x
- TensorFlow
- NLTK (Natural Language Toolkit)
- Numpy

You can install these dependencies using pip: pip install tensorflow nltk numpy

## Code Overview

The chatbot consists of two main Python scripts: train_chatbot.py and chatbot.py. Here's a brief overview of each script:

## train_chatbot.py
This script is responsible for training the chatbot. It performs the following tasks:

- Imports required libraries and loads the intents from a JSON file (intents.json).
- Processes and tokenizes the intent patterns, lemmatizes words, and prepares data for training.
- Creates a model using TensorFlow and trains it using the provided training data.
- Saves the trained model to a file (chatbotmodel.h5).
- Saves necessary data structures (words.pkl and classes.pkl) for later use in the chatbot.

## chatbot.py
This script is the main chatbot implementation that interacts with users. It performs the following tasks:

- Imports the required libraries and loads the intents, words, and classes.
- Defines functions for cleaning up user input and predicting the intent of the input.
- Implements the chat loop, where the chatbot listens to user input and provides responses based on the trained model.
- The chatbot continues to respond to user input until the user enters "bye" or "Goodbye," at which point it exits the conversation.

## Setup

- Clone or download this repository to your local machine.

- Ensure that you have the necessary dependencies installed, as mentioned in the "Prerequisites" section.

- Prepare your training data:

- Create a JSON file named intents.json that defines the intents and responses for your chatbot. An example format is provided in the code.
- Define the patterns, responses, and tags for different intents in this JSON file.
- Run the training script to train the chatbot: python train_chatbot.py
This script will preprocess your training data and create a model. The trained model will be saved as chatbotmodel.h5, and data structures (words.pkl and classes.pkl) will be generated for use by the chatbot.

- After training, you can run the chatbot script to interact with it: python chatbot.py

## Usage
Once the chatbot script is running, you can interact with the chatbot by entering your queries. The chatbot will respond based on the patterns and responses defined in intents.json. To exit the conversation, simply enter "bye" or "Goodbye."

Feel free to modify the intents.json file to customize the chatbot's responses and add more intents as needed for your specific use case.

Please note that the chatbot's responses are based on the training data, so the accuracy of responses may vary depending on the quality and quantity of the training data.
