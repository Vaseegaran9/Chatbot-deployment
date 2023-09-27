# Chatbot Deployment with Flask and JavaScript

In this tutorial we deploy the chatbot I created in [this](https://github.com/python-engineer/pytorch-chatbot) tutorial with Flask and JavaScript.

This gives 2 deployment options:
- Deploy within Flask app with jinja2 template
- Serve only the Flask prediction API. The used html and javascript files can be included in any Frontend application (with only a slight modification) and can run completely separate from the Flask App then.

## Initial Setup:
This repo currently contains the starter files.

Clone repo and create a virtual environment
```
$ git clone https://github.com/python-engineer/chatbot-deployment.git
$ cd chatbot-deployment
$ python3 -m venv venv
$ . venv/bin/activate
```
Install dependencies
```
$ (venv) pip install Flask torch torchvision nltk
```
Install nltk package
```
$ (venv) python
>>> import nltk
>>> nltk.download('punkt')
```
Modify `intents.json` with different intents and responses for your Chatbot

Run
```
$ (venv) python train.py
```
This will dump data.pth file. And then run
the following command to test it in the console.
```
$ (venv) python chat.py
```

Objective: The primary goal of this project was to create a user-friendly and informative chatbot specifically tailored to the needs of farmers in Tamil Nadu, India. The chatbot aimed to provide instant assistance and information related to agriculture, crops, weather, and soil conditions.

Technologies and Libraries Used:

Python Programming Language: Python served as the foundation for building the chatbot's core logic and functionality. Its versatility and robust ecosystem of libraries made it an ideal choice.

PyTorch: To enable natural language understanding and response generation, PyTorch, a powerful deep learning framework, was employed. PyTorch allowed us to design and train a neural network capable of processing and generating human-like responses to user queries.

Flask Framework: Flask, a lightweight web framework for Python, was integrated to create the chatbot's user interface. This web-based interface enabled farmers to interact with the chatbot seamlessly.

Natural Language Processing (NLP):

NLTK (Natural Language Toolkit): NLTK was utilized for critical NLP tasks such as tokenization (breaking text into words), stemming (reducing words to their root form), and other language processing tasks. These techniques improved the chatbot's ability to understand user queries effectively. JSON Data Format: The chatbot's knowledge base, including responses to various queries, was structured and stored in a JSON (JavaScript Object Notation) file. JSON's simplicity and readability made it a suitable choice for organizing and retrieving data.

Key Components and Workflow:

Neural Network Model (PyTorch): The core of the chatbot was its neural network model. This model, defined in the NeuralNet class, was responsible for processing user queries and generating appropriate responses.

Training Data: The chatbot's knowledge base was created by gathering agricultural intents and patterns. These intents encompassed common queries farmers might have, ranging from crop information to weather updates.

Bag-of-Words and One-Hot Encoding: To make sense of user input, the chatbot used techniques like bag-of-words and one-hot encoding to convert text data into a numerical format suitable for neural network processing.

Flask-Based User Interface: Farmers interacted with the chatbot through a user-friendly web interface created using Flask. They could input queries, and the chatbot provided real-time responses.

Training and Deployment:

Training Process: The neural network model was trained using the gathered training data and PyTorch's deep learning capabilities. The training process involved multiple epochs to optimize the model's performance.

Model Saving: Once the model was trained successfully, its state, along with essential parameters like input size and output size, was saved to a file for later use.

Integration with Flask: The trained model was integrated into the Flask-based web interface. This integration allowed farmers to access the chatbot through a web browser.

Usage and Benefits:

The chatbot served as a valuable resource for Tamil Nadu farmers:

It provided quick and accurate responses to a wide range of agricultural queries. Farmers could inquire about crop growth, suitable fertilizers, climatic conditions, and detailed crop descriptions. Real-time weather updates specific to different regions of Tamil Nadu were offered, enabling farmers to make informed decisions about farming practices. In conclusion, the development of the Tamil Nadu Farmer Chatbot was a multidisciplinary effort that harnessed the power of Python, PyTorch, Flask, and NLP techniques to create a highly beneficial tool for the farming community. The chatbot's ability to provide tailored agricultural information played a crucial role in improving farming practices and productivity in the region.
