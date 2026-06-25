# Internship Full Stack Projects Report

## 1.  Smart Spam Detection System

Overview
As part of the internship, two full-stack web applications were developed that combine machine learning with interactive web interfaces. Both projects demonstrate the integration of Python-based backends with frontend interfaces to deliver intelligent, real-time predictions.

## Smart Spam Detection System

Objective
To build an intelligent spam detection system that accurately identifies unwanted messages using natural language processing and machine learning, deployed as an interactive web application.
Technologies Used
ComponentTechnologyProgramming LanguagePython 3.11Web FrameworkFlaskMachine LearningScikit-learnText VectorizationTF-IDF VectorizerFrontendHTML5, CSS3DatasetSMS Spam Collection (spam.csv)
System Architecture
The application follows a client-server architecture:

The frontend provides a clean user interface where users enter a message and submit it for analysis.
The backend (Flask) receives the input, preprocesses it using a saved TF-IDF vectorizer, and passes it to the trained classification model.
The model returns a prediction displayed to the user as either SPAM or HAM.

Implementation
1. Model Training (train_model.py)

A machine learning model was trained on a labeled SMS dataset containing spam and ham messages. The text data was converted into numerical features using TF-IDF vectorization. The trained model and vectorizer were serialized and saved as model.pkl and vectorizer.pkl for reuse during prediction.
2. Web Application (app.py)

A Flask web server was developed to handle HTTP requests. On form submission, the user's message is vectorized using the saved vectorizer and passed to the model for prediction. The result is rendered back to the user on the same page.
3. Frontend (index.html, style.css)

A simple and intuitive HTML form was designed for user interaction, styled with CSS for a clean appearance.
How It Works

User enters a message in the web interface.
The message is sent to the Flask backend via a POST request.
The backend transforms the text using the TF-IDF vectorizer.
The trained model predicts whether the message is spam or ham.
The result is displayed as SPAM or HAM.

Key Learnings

Building and deploying a machine learning model as a web application.
Understanding text preprocessing and feature extraction using TF-IDF.
Integrating Python ML models with a Flask backend.
Developing a complete full-stack application from data to deployment.


##  Sentiment Analysis Web Application
Objective
To develop a web application that analyzes the emotional tone of any text input and classifies it as positive, negative, or neutral in real time.
Technologies Used
ComponentTechnologyProgramming LanguagePython 3.11Web FrameworkFlaskSentiment LogicKeyword-based analysisFrontendHTML5, CSS3
System Architecture
The application follows a lightweight client-server architecture:

The frontend provides a text input form where users enter any sentence or paragraph.
The backend (Flask) processes the text using a custom keyword-based sentiment analyzer.
The result is returned and displayed on the page with an emoji indicator.

Implementation
1. Sentiment Analysis Logic (app.py)

A rule-based sentiment analyzer was implemented using two predefined word sets — positive words (e.g. good, great, love, amazing) and negative words (e.g. bad, terrible, hate, worst). The input text is tokenized, cleaned of punctuation, and each word is checked against both sets. The sentiment is determined by whichever count is higher.
2. Web Application (app.py)

A Flask route handles both GET and POST requests. On form submission, the text is passed through the sentiment analyzer and the result is rendered back to the same page using Jinja2 templating.
3. Frontend (index.html)

A clean HTML form allows users to type or paste any text. The result is displayed dynamically with emoji feedback — 😊 Positive, 😞 Negative, or 😐 Neutral.
How It Works

User enters a sentence or paragraph in the web interface.
The text is submitted to the Flask backend via a POST request.
The backend tokenizes the text and counts positive and negative keywords.
The sentiment is determined based on which count is higher.
The result is displayed as Positive 😊, Negative 😞, or Neutral 😐.

Key Learnings

Implementing rule-based natural language processing logic in Python.
Building dynamic web pages using Flask and Jinja2 templating.
Designing user-friendly interfaces for text-based applications.
Understanding the foundations of sentiment analysis before moving to ML-based approaches.
